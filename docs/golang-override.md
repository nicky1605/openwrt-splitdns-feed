# Golang override note (for mosdns on OpenWrt 24.10.x)

## Why this exists

On OpenWrt v24.10.5 (baseline for this project), the default `feeds/packages/lang/golang`
provides a Go toolchain that is not new enough for `mosdns`:

- mosdns `go.mod` requires **Go >= 1.24**
- baseline OpenWrt 24.10.x packages feed typically provides **Go 1.23.x**

Therefore, building mosdns on 24.10.x requires replacing the golang packaging layer.

## What this feed provides

This feed vendors an alternative golang packaging repo:

- Upstream: https://github.com/sbwml/packages_lang_golang
- Pinned commit: 94dd0f5793debfee007f0581509640c392de7188

Imported into this feed under:

- `golang/` (package directory)
- helper files inside `golang/` (e.g. `golang-*.mk`, `golang-build.sh`, etc.)

## Recommended override method (in OpenWrt buildroot)

In your OpenWrt buildroot (not in this feed repo), after `feeds update/install`:

```sh
rm -rf feeds/packages/lang/golang
ln -sfn "$(pwd)/feeds/splitdns/golang" feeds/packages/lang/golang

./scripts/feeds update packages
./scripts/feeds install -a -p packages
Build strategy notes

Parallel builds (-j$(nproc)) are recommended for normal compilation,
especially for toolchain and golang-related packages.

Single-threaded builds (-j1 V=s) are useful only for debugging or
dependency investigation when diagnosing failures.

Notes

This project does not modify OpenWrt toolchain/targets/core logic.
The override is done by redirecting the golang package directory only.
