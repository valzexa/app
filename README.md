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
| `vava_v1.0.28.apk` | Android | v1.0.28 | vava App（arm64，2026-10-28 构建；**新增统一账号 Google 登录**：优先复用系统里已登录的 Google 账号（原生 Credential Manager，命中时无任何弹窗），失败依次回退系统浏览器 → 内置浏览器；登录后与账密登录同构换取业务 JWT；**修复**中心接口不可达时 client_id 为空串导致原生登录被跳过的问题；含 v1.0.27 全部功能） |
| `vava_v1.0.28-x86_64.apk` | Android | v1.0.28 | vava App x86_64 版（模拟器 / x86 平板用，功能同 arm64 包） |
| `vava_v1.0.27.apk` | Android | v1.0.27 | vava App（arm64，2026-10-28 构建；**充值改为应用内原生弹层**：微信支付 / 银行卡（Visa、Mastercard，Creem）/ PayPal / USDT，微信扫码或复制支付链接完成支付，USDT 展示收款地址与精确金额，弹窗内轮询到账并自动刷新余额，不再跳转用户中心网页；**动态卡片改版**：显示作者头像与昵称、点击头像弹出资料卡，他人动态标题显示昵称，动态时间兼容秒级时间戳；含 v1.0.26 全部功能） |
| `vava_v1.0.27-x86_64.apk` | Android | v1.0.27 | vava App x86_64 版（模拟器 / x86 平板用，功能同 arm64 包） |
| `vava_v1.0.26.apk` | Android | v1.0.26 | vava App（arm64，2026-10-27 构建；**充值渠道对齐用户中心**：App 内钱包充值渠道与统一钱包 5 渠道（Creem 卡 / 支付宝 / 微信 / PayPal / USDT）一致，提示文案含支付宝/微信，多语言钱包词条补全；含 v1.0.25 全部功能） |
| `vava_v1.0.26-x86_64.apk` | Android | v1.0.26 | vava App x86_64 版（模拟器 / x86 平板用，功能同 arm64 包） |
| `vava_v1.0.25.apk` | Android | v1.0.25 | vava App（2026-10-27 发布；**动态图片点开可全屏滑动切换**：个人动态与群动态共用全屏查看器（PageView 左右滑动 + n/9 页码 + 双指缩放 + 视频播放入口），此前个人动态图片点击无响应、群动态查看器统一化；**支付渠道改版**：收银台改为 PayPal / 信用卡（Creem）/ USDT（TRC20）/ 收款二维码（人工确认）——支付宝微信直连下线，个人收款码付款后由管理员在后台人工确认入账（新增 `POST /api/admin/member/orders/:no/confirm-manual`）；USDT 下单展示收款地址/精确金额/网络并可复制，链上到账自动入账；**多语言扩展至 13 种**：新增常任理事国语言俄/法/西 + 加密高频韩/日（既有英语/越南/土耳其/乌克兰/印地/葡/印尼），核心词典覆盖基础界面与群功能，漏翻回落中文，语言选择器按「常任理事国 → 加密高频国家」分组；**新增群动态**：仅群成员可见/发布，文字+图片/动图/小视频共 9 个，头像点击弹资料页，审核管线同个人动态（待审仅作者可见）；**群自动回复**：群里 @管理员 且命中群管理配置的关键词 → 以该管理员身份按规则回复（60s/群限频，App 群设置可配 ≤20 条规则）；**群 Webhook 支持定向发用户**（`to_uid` 以系统身份单聊投递）+ **chat_id 对接审计**：查看/启用/重置/OpenAPI 推送全留痕，后台「对接审计」页可查；群菜单引用**未审核素材显示「未审核」且不可点**；**群动态入口在群资料页最上方**（群聊右上角 ⋮ 即达）；**群菜单改原生化**：锚定输入框按钮上方的悬浮卡片，二级菜单带箭头从右侧滑入；**小程序悬浮胶囊**：背景加深、最小化改大圆点；**修复登录/注册图形验证码不显示**（新中心 SVG textPath 改拉 PNG 位图渲染）；同步最新版用户中心 uc-sdk-go/js；含 v1.0.18-20 全部功能：群菜单四种动作（发消息/跳链接/跳小程序/搜聊天记录分页）、小程序/链接素材库（发布需审核）、群 Webhook、聊天气泡 Markdown+HTML、陌生人单聊 3 条限制后台可设、公众号下线） |

> 注：自 v1.0.26 起 vava 改用 `--split-per-abi` 分包发布：arm64 包（约 36MB）为手机主发布包，x86_64 包（约 38MB）供模拟器 / x86 平板；v1.0.25 及以前为通用 APK（约 99MB，压线 GitHub 单文件 100MB 限制）；armeabi-v7a 包构建但不发布。

### valink/ — Valink（原 lianlian 连连）

| 文件 | 平台 | 版本 | 说明 |
| --- | --- | --- | --- |
| `valink-v2.3.17-arm64.apk` | Android | v2.3.17 | Valink App（包名 com.valzexa.valink，arm64 手机主包，2026-10-28 构建；**新增统一账号 Google 登录**：Credential Manager 复用系统已登录 Google 账号（静默优先，无 UI），失败依次回退系统浏览器（`valink://uc-login` 深链回跳）→ 内置 WebView；**服务端修复钱包扣款**：同名订单并发/重试不再重复开通套餐（原先「钱扣一次、货发两次」），并发购买多单时长正确叠加，扣款成功后记账失败不再阻断开通；含 v2.3.16 全部功能） |
| `valink-v2.3.17-x86_64.apk` | Android | v2.3.17 | Valink App x86_64 版（模拟器 / x86 平板用，功能同 arm64 包） |
| `valink-v2.3.16-arm64.apk` | Android | v2.3.16 | Valink App（包名 com.valzexa.valink，arm64 手机主包，2026-10-28 clean 全量重编；**充值渠道对齐统一钱包 5 渠道**：Creem 卡（默认选中）/ 支付宝 / 微信 / PayPal / USDT——充值页按用户中心渠道开关动态下发，支付宝/微信附链接支付引导，USDT 弹框保持打开可反复核对；套餐购买走钱包余额；含 v2.3.15 全部功能） |
| `valink-v2.3.16-x86_64.apk` | Android | v2.3.16 | Valink App x86_64 版（模拟器 / x86 平板用，功能同 arm64 包） |
| `valink-v2.3.15.apk` | Android | v2.3.15 | Valink App（包名 com.valzexa.valink，2026-10-26 构建；新增俄/土/越/波斯/印尼/葡/西 7 种语言，默认跟随系统、缺省英语；余额支付、免费体验置灰保留、流量实时计量） |
| `VaLink-win-x64.exe` | Windows | v1.0.7 | VaLink Windows 客户端（.NET 10 自包含单文件发布，2026-10-28 重编；**充值渠道对齐统一钱包 5 渠道**：Creem 卡（默认）/ 支付宝 / 微信 / PayPal / USDT，支付宝/微信附链接支付引导，与 APK 充值页同能力；购买走余额支付；9 种语言） |

> 注：自 v2.3.16 起 valink 改用 gradle ABI splits 分包发布：arm64 包（v2.3.17 为 67.1MB）为手机主发布包，x86_64 包（70.4MB，libbox 核心含 x86_64 原生库）供模拟器 / x86 平板；v2.3.15 及以前为通用 APK。

### gouwu/ — 购物 / 谷里 GULI（竹竹快选 shop 的 Flutter 社交电商端）

| 文件 | 平台 | 版本 | 说明 |
| --- | --- | --- | --- |
| `gouwu-v1.0.0.apk` | Android | v1.0.0 | 谷里 GULI App（包名 cn.tansuohao.guli_app，2026-10-17 构建） |

### vavacoin/ — VavaCoin（VVC 数字资产交易所）

| 文件 | 平台 | 版本 | 说明 |
| --- | --- | --- | --- |
| `vavacoin_v1.3.6.apk` | Android | v1.3.6 | VavaCoin App（包名 cn.tansuohao.vavacoin，arm64，2026-10-28 构建；**新增统一账号 Google 登录**：优先复用系统已登录 Google 账号（原生），失败回退系统浏览器（`vavacoin://uc-login` 深链回跳）→ 内置浏览器；补全第②级系统浏览器回退；含 v1.3.5 全部功能） |
| `vavacoin_v1.3.5.apk` | Android | v1.3.5 | VavaCoin App（包名 cn.tansuohao.vavacoin，arm64，2026-10-28 构建；**开户费**：VGD 开户默认 5 USDT（后台可调），开户遇 4005 弹「支付开户费并开通」确认并重发 pay_fee；**开发者 API**：实时价格 / 币种转换 / 转账，配套 7 语言开发者门户与后台开发者管理，费率与 App 一致；含 v1.3.2 USDT 内部结算余额、v1.3.3 币种子账户（7 币种开户制）、v1.3.4 转账手续费提示与后台账户冻结；全站亮色主题） |

## 未收录说明

- **payhub**：按需求不收录。
- **服务端二进制**：chatservices.exe / chatservices_linux、hexiao.exe、serverpanel.exe / serverpanel_linux、payhub.exe、lianlian-server、api-server、gouwu-linux 服务端部署包等均为服务端编译产物，不收录。
- **debug / 旧版本包**：app-debug.apk、vava-diag.apk、vava_v1.0.15.apk 等不收录。
- **ExploreMovie.exe**：官网 aimovie 页面有引用，但本地未找到该发布文件。
