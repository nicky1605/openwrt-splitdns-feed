# Third-Party Notices

This repository aggregates third-party OpenWrt packages via `git subtree` and pins them
to specific upstream commits for reproducibility.

Each third-party component remains under its original upstream license.
Where upstream does not provide a license file, the license status is **unknown** and
should be clarified with the author/upstream.

---

## sbwml / luci-app-mosdns (multi-package repo)

Upstream:
- Repo: https://github.com/sbwml/luci-app-mosdns
- Pinned commit: 71df20dacdb3092dcfca75904d6b9642368896a3
- Imported packages (promoted to top-level):
  - `luci-app-mosdns/`
  - `mosdns/`
  - `v2dat/`

Upstream notices:
- LICENSE: https://github.com/sbwml/luci-app-mosdns/blob/v5/LICENSE
- README:  https://github.com/sbwml/luci-app-mosdns/blob/v5/README.md

---

## sbwml / v2ray-geodata

Upstream:
- Repo: https://github.com/sbwml/v2ray-geodata
- Pinned commit: 2e3845caae172326f02b3406048c7a3613f3dee5
- Imported package:
  - `v2ray-geodata/`

Upstream notices:
- (Use upstream repo root for license/notice if present.)

---

## sbwml / luci-theme-argon (multi-package repo)

Upstream:
- Repo: https://github.com/sbwml/luci-theme-argon
- Pinned commit: 5a2ff57f301d5bfc65fea3cb40f1516e4e83190c
- Imported packages (promoted to top-level):
  - `luci-theme-argon/`
  - `luci-app-argon-config/`

Upstream notices:
- Upstream repository does not provide README/LICENSE files (per current reference).
- NOTE: Although the author is the same as `luci-app-mosdns`, **license inheritance is not guaranteed**.
  If you choose to include a license copy for visibility, keep it clearly marked as a reference and
  prefer verifying the actual license from upstream.

Reference (author-provided license example):
- LICENSE reference: https://github.com/sbwml/luci-app-mosdns/blob/v5/LICENSE

---

## bobbyunknown / luci-app-syscontrol

Upstream:
- Repo: https://github.com/bobbyunknown/luci-app-syscontrol
- Pinned commit: 6bf93c124a632b2c865aa0db8e3af3af3fd5cfba
- Imported package:
  - `luci-app-syscontrol/`

Upstream notices:
- README:  https://github.com/bobbyunknown/luci-app-syscontrol/blob/main/README.md
- LICENSE: https://github.com/bobbyunknown/luci-app-syscontrol/blob/main/LICENSE

---

## lisaac / luci-app-diskman

Upstream:
- Repo: https://github.com/lisaac/luci-app-diskman
- Pinned commit: d70d9592845a8f75de15b22a82c1ff067f9477fb
- Imported package (promoted from `applications/luci-app-diskman/`):
  - `luci-app-diskman/`

Upstream notices:
- README:  https://github.com/lisaac/luci-app-diskman/blob/master/README.md
- LICENSE: https://github.com/lisaac/luci-app-diskman/blob/master/LICENSE

---

## sirpdboy / luci-app-netwizard

Upstream:
- Repo: https://github.com/sirpdboy/luci-app-netwizard
- Pinned commit: 0eaaa5edcb3e1d27936814a30955e5838a462dea
- Imported package:
  - `luci-app-netwizard/`

Upstream notices:
- README: https://github.com/sirpdboy/luci-app-netwizard/blob/main/README.md
- LICENSE: Not provided in upstream repo (per current reference; license status unknown).

---

## sbwml / packages_lang_golang

Upstream:
- Repo: https://github.com/sbwml/packages_lang_golang
- Pinned commit: 94dd0f5793debfee007f0581509640c392de7188
- Imported package:
  - `golang/`
- Imported helper files (repo root):
  - `golang-*.mk`, `golang-build.sh` (and other Go build helpers as included upstream)

Purpose:
- Provide a Go toolchain packaging layer compatible with OpenWrt 24.10.x to satisfy
  mosdns Go version requirements.

Upstream notices:
- (Use upstream repo root for license/notice if present.)

