# openwrt-splitdns-feed

This repository is a custom OpenWrt feed for a personal OpenWrt-based system.
It **does not** fork OpenWrt or modify toolchain/targets/core feeds.
All customization is delivered via **feed/package injection** only.

## Baseline

- OpenWrt baseline repo: `nicky1605/openwrt`
- Branch: `openwrt-24.10`
- Tag: `v24.10.5`

## What’s inside

Packages are imported with **git subtree** and pinned to specific upstream commits
for reproducibility.

### Directory layout

```text
openwrt-splitdns-feed/
  luci-app-mosdns/
  mosdns/
  v2dat/
  v2ray-geodata/
  luci-theme-argon/
  luci-app-argon-config/
  luci-app-syscontrol/
  luci-app-diskman/
  luci-app-netwizard/
  golang/
  (golang-*.mk / golang-build.sh and related helper files at repo root)

Third-party sources and pinned commits
See THIRD_PARTY_NOTICES.md.

How to use this feed
Add to your OpenWrt buildroot feeds config:
src-git splitdns <GIT_URL_OF_THIS_REPO>


Then:
./scripts/feeds update splitdns
./scripts/feeds install -a -p splitdns

Development workflow
This repo uses git subtree for vendor imports.

Import:
git subtree add --prefix=<dir> <repo> <commit> --squash


Update:
git subtree pull --prefix=<dir> <repo> <commit-or-branch> --squash
