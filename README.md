# Lattie Releases

Lattie 测试预发布版（mac Apple 芯片，已签名 + 公证）的下载仓库。这里只放构建 workflow 与 Release 附件，不含源码。

- 下载：见 [Releases](../../releases)，选 `Lattie-<version>-arm64.dmg`
- 版本号：`0.1.0-beta.N` 为 beta（prerelease），`0.1.0` 这类无后缀为正式版（latest）
- 校验：Release 内附 `SHA256SUMS`
- 应用内自动更新（electron-updater）读取 Release 附件中的 `beta-mac.yml` / `latest-mac.yml` 与 `.blockmap`，请勿改名或删除

## 触发构建（维护者）

```
# beta（默认，序号自动递增）
gh workflow run build-mac.yml -R windword-labs/lattie-releases
# 可选：-f source_ref=<分支/SHA> -f beta=<序号>

# stable（版本取源码 apps/desktop/package.json 的 version；tag 已存在会失败，需先改版本）
gh workflow run build-mac.yml -R windword-labs/lattie-releases -f channel=stable -f source_ref=<分支/tag/SHA>
```
