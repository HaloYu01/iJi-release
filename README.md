# iJi-release

iJi（i记）记账 App 的安装包发布仓库。

## 用途

- 本仓库**只存放 APK**，不存放任何源代码。
- 每个版本以 GitHub Release 形式发布，最新 APK 作为 Release 附件提供下载。

## 源码

源码位于私有仓库 [HaloYu01/iJi](https://github.com/HaloYu01/iJi)。

## 应用内更新检测

1. 请求最新 Release：`GET https://api.github.com/repos/HaloYu01/iJi-release/releases/latest`
2. 读取返回 JSON 中的 `tag_name`（建议格式 `v<versionName>`）与 `assets[].browser_download_url`（APK 下载地址）。
3. 与本地 `versionCode` / `versionName` 比较，有新版本时提示下载。

## 发布约定

- tag：`v<versionName>`（例如 `v1.2.0`）
- APK 附件名：`iJi-v<versionName>.apk`
- 如需固定下载地址，也可将最新 APK 覆盖上传到仓库根目录的 `iJi-latest.apk`，通过 `https://github.com/HaloYu01/iJi-release/raw/main/iJi-latest.apk` 获取。
