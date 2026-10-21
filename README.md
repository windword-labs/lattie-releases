# Lattie Releases

Lattie 测试预发布版（mac Apple 芯片，已签名 + 公证）的下载仓库。这里只放构建 workflow 与 Release 附件，不含源码。

- 下载：见 [Releases](../../releases)，选 `Lattie-<version>-arm64.dmg`
- 版本号形如 `0.1.0-beta.N`，均为 prerelease
- 校验：Release 内附 `SHA256SUMS`

## 触发构建（维护者）

```
gh workflow run build-mac-beta.yml -R windword-labs/lattie-releases
# 可选：-f source_ref=<分支/SHA> -f beta=<序号>
```
