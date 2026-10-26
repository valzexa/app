# software · 产品发布仓库

本仓库按产品目录收录各软件的**最新发布版本**（Windows 客户端 exe / Android APK 等面向终端用户的发布物）。

> 扫描时间：2026-10-22。来源为 projects 工作区各项目目录（website 下载目录、dist 发布目录、release 构建产物）。
> 说明：服务端编译的二进制（如 chatservices、hexiao、serverpanel、payhub、lianlian-server 等 Go 服务端 exe/linux 文件）与服务端部署包不属于本仓库收录范围；payhub 产品不收录。

## 目录结构

### ShopSuite/ — 门店管理系统（智店长）

| 文件 | 平台 | 版本 | 说明 |
| --- | --- | --- | --- |
| `ShopSuite.exe` | Windows | 最新版 | PC 客户端（官网发布） |
| `ShopSuiteWeb.exe` | Windows | 最新版 | Web 版客户端（官网发布） |
| `manager.apk` | Android | 最新版 | 门店管理 App（官网发布，包名 cn.tansuohao.apps） |
| `ShopSuite-mobile-v1.0.1.apk` | Android | v1.0.1 | 新版 Flutter 移动端（包名 com.tansuohao.flutter_mobile，2026-10-19 构建） |
| `门店管理系统-v2.1.1-修复网络错误.apk` | Android | v2.1.1 | 门店管理 App（dist 发布，包名 cn.wangxiao2.suite） |
| `智店长柜-松生活-20260929-v2.2.6.apk` | Android | v2.2.6 | 智店长柜（松生活客户版，包名 cn.tansuohao.shellsuite） |

### personal-suite/ — 个人套件

| 文件 | 平台 | 版本 | 说明 |
| --- | --- | --- | --- |
| `personal-suite.exe` | Windows | 最新版 | 个人套件 PC 客户端（官网发布） |
| `personal-suite-cloud.exe` | Windows | 最新版 | 个人套件云同步版（官网发布） |
| `personal.apk` | Android | 最新版 | 个人套件 App（官网发布，uni-app 版） |
| `personal-suite-v1.0.0.apk` | Android | v1.0.0 | Flutter 版 App（包名 com.persuite.personal_suite，2026-10-16 构建） |

### vava/ — vava

| 文件 | 平台 | 版本 | 说明 |
| --- | --- | --- | --- |
| `vava_v1.0.16.apk` | Android | v1.0.16 | vava App（2026-10-20 发布） |

> 注：dist 目录中另有 2026-10-21 重新构建的 1.0.16 安装包（约 132MB），因超过 GitHub 单文件 100MB 限制未收录；如需可改用 Git LFS。

### valink/ — Valink（原 lianlian 连连）

| 文件 | 平台 | 版本 | 说明 |
| --- | --- | --- | --- |
| `valink-v2.3.14.apk` | Android | v2.3.14 | Valink App（包名 com.valzexa.valink，2026-10-26 构建；流量实时计量修复、流量用尽自动断开并提示、未付费引导购买、免费体验保留列表按钮置灰；美元套餐 $1.99/7 天、$9.99/月、$59.90/年、$79.90/2 年） |
| `VaLink-win-x64.exe` | Windows | v1.0.5 | VaLink Windows 客户端（.NET 10 自包含单文件发布，2026-10-26 构建；未付费连接被拒引导购买、流量用尽自动断开并提示、免费体验保留列表置灰、服务端流量实时计量） |

### gouwu/ — 购物 / 谷里 GULI（竹竹快选 shop 的 Flutter 社交电商端）

| 文件 | 平台 | 版本 | 说明 |
| --- | --- | --- | --- |
| `gouwu-v1.0.0.apk` | Android | v1.0.0 | 谷里 GULI App（包名 cn.tansuohao.guli_app，2026-10-17 构建） |

### vavacoin/ — VavaCoin（VVC 数字资产交易所）

| 文件 | 平台 | 版本 | 说明 |
| --- | --- | --- | --- |
| `vavacoin_v1.2.3.apk` | Android | v1.2.3 | VavaCoin App（包名 cn.tansuohao.vavacoin，arm64，2026-10-26 构建；原生登录直连用户中心 + 7 语言；首页与买卖页新增 1m/5m/15m/1h/1d 折线走势图，实时现价叠加） |

## 未收录说明

- **payhub**：按需求不收录。
- **服务端二进制**：chatservices.exe / chatservices_linux、hexiao.exe、serverpanel.exe / serverpanel_linux、payhub.exe、lianlian-server、api-server、gouwu-linux 服务端部署包等均为服务端编译产物，不收录。
- **debug / 旧版本包**：app-debug.apk、vava-diag.apk、vava_v1.0.15.apk 等不收录。
- **ExploreMovie.exe**：官网 aimovie 页面有引用，但本地未找到该发布文件。
