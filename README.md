# Cber Android 安装包

只做安卓 APK 分发，安装包放在 [Releases](https://github.com/cber-io/android/releases)，不进 git 历史（仓库体积不随版本增长）。App 线路配置仍在 [cber-io/app](https://github.com/cber-io/app)，两者互不影响。

## 约定

- 每个版本一个 Release：tag `v<versionName>-<versionCode>`，附件 `cber_com_<versionName>_<versionCode>.apk`
- Release 说明里写 APK 的 SHA-256 和签名证书指纹，发布后不覆盖附件；修包就发新的 versionCode

## 下载链接格式

```
# 大陆（经 gh-proxy）
https://gh-proxy.com/https://github.com/cber-io/android/releases/download/<tag>/<apk>
# 直连
https://github.com/cber-io/android/releases/download/<tag>/<apk>
```

## 版本记录

| 版本 | 下载（大陆） | SHA-256 |
|---|---|---|
| 1.0.1 (25) | [cber_com_1.0.1_25.apk](https://gh-proxy.com/https://github.com/cber-io/android/releases/download/v1.0.1-25/cber_com_1.0.1_25.apk) | `cf61999c0c19da3edb681c8ac80d02788ca1db9b783a00ef1c6768d6e3cfd9c9` |
| 1.0.1 (24) | [cber_com_1.0.1_24.apk](https://gh-proxy.com/https://github.com/cber-io/android/releases/download/v1.0.1-24/cber_com_1.0.1_24.apk) | `665c71f5536a3d03af50184b86a45028756e3df616e23a623c6c0012c54fe933` |
| 1.0.0 (23) | [cber_com_1.0.0_23.apk](https://gh-proxy.com/https://github.com/cber-io/android/releases/download/v1.0.0-23/cber_com_1.0.0_23.apk) | `51be99650c9da2375a28509d0b11c2e16e4f06bce7cb02970ae6dfa76bcc5828` |

## 签名证书

`CN=sgp, OU=cb, O=cb, L=sgp, ST=sgp, C=65`
SHA-256 `80:a9:c1:c6:0b:f8:e4:66:d5:71:7b:8a:b5:75:22:15:53:1d:a2:89:11:5f:db:68:a3:22:9c:9c:bf:4f:f9:cb`

校验：`apksigner verify --print-certs <apk>`，证书 SHA-256 必须与上面一致。
