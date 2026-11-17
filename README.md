# Claude 国内使用教程（2026）

从一台干净的电脑，走到能稳定跑起来。每一步做什么、按什么顺序做、看到什么算正常。

这份只讲操作。想知道每个动作背后防的是什么，看姊妹仓 [claude-fangfen](https://github.com/sobadgirl/claude-fangfen)。

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
![Last Update](https://img.shields.io/github/last-commit/sobadgirl/use-claude-in-china)

系列仓库｜[教程](https://github.com/sobadgirl/use-claude-in-china) · [避坑](https://github.com/sobadgirl/claude-fangfen) · [合集](https://github.com/sobadgirl/awesome-claude-cn) · [服务](https://github.com/sobadgirl/get-claude-in-china)

## 目录

- [0. 先选路线](#0-先选路线)
- [1. 三件套：邮箱、网络、支付](#1-三件套)
- [2. 注册](#2-注册)
- [3. 订阅](#3-订阅)
- [4. 装客户端](#4-装客户端)
- [5. 头三天怎么用](#5-头三天怎么用)
- [6. 对着症状查](#6-对着症状查)
- [7. 常见问题](#7-常见问题)
- [附：开工前检查清单](#附开工前检查清单)

## 0. 先选路线

Claude 有三种用法，准备工作不一样，别混着来。

| 用法 | 你拿到什么 | 门槛 | 适合谁 |
|---|---|---|---|
| Claude.ai 网页 / App | 聊天、写东西、读图、做分析 | 中 | 不写代码的人 |
| Claude Code（命令行） | 在终端里让 Claude 直接改你的项目 | 高 | 开发者、重度使用者 |
| API（Console） | 把模型接进自己的产品 | 高 | 有产品要接模型的人 |

三条路的第一道坎一样：账号得活着。第二道坎不一样。

新手最常犯的错是先买了 Pro，再去折腾 Claude Code，结果发现要的是另一套东西。先想清楚你每天到底在哪用。

## 1. 三件套

邮箱、网络、支付，这三样决定了你账号的出厂设置。注册前定死，中途换任何一样都是在给自己找事。

### 1.1 邮箱

做什么：

1. 自己注册一个 Gmail。别买。
2. 打开两步验证。
3. 记下注册日期，以及注册时所在地的城市名，后面要用来对齐时区。

别做：一次性邮箱（10minutemail、temp-mail 这类）、QQ 邮箱、163 邮箱、买来的二手 Gmail。二手号风控值本来就高，你不是第一个用它的人。

### 1.2 网络

做什么：

1. 选一个国家的节点，之后不换。
2. 优先住宅 IP 或独享静态 IP。
3. 注册、登录、订阅、日常使用，全程同一条线路。

别做：共享 VPN 出口（Surfshark、NordVPN 这类公共池，ASN 早被标成高风险）、今天新加坡明天日本、注册一个线路付款另一个线路。

怎么判断你的 IP 干不干净：查这段 IP 的 ASN。看到的是 AWS、DigitalOcean、Vultr、阿里云海外这类云厂商名字，就是机房 IP；看到的是宽带运营商名字，才是住宅 IP。免费查询站随便找一个输进去就有。

机房 IP 不是绝对不能用，是更容易被扫到。原理在 [claude-fangfen](https://github.com/sobadgirl/claude-fangfen) 里讲。

### 1.3 支付

2026 年翻车率最高的一步不是注册，是付款。

能用的：

| 方式 | 稳定性 | 说明 |
|---|---|---|
| 美区 Apple ID + App Store 礼品卡 | 目前最稳 | iOS 上内购，Apple 直接收单，绕开 Stripe |
| 真实美区银行卡 | 最稳 | 门槛最高，要有美国身份或可靠代持 |

别用的：

- 加密货币充值的不需要 KYC 的虚拟卡（U 卡）。Anthropic 按发卡行 BIN 段批量清退，2026 年已经清了好几轮，付款成功也可能几小时内被退款并封号。
- 代充。手里的卡多是黑卡或套现卡，几个月后 chargeback，账号跟着连坐。
- Google Pay 绑虚拟卡。底层还是虚拟卡 BIN，一样秒退。

## 2. 注册

1. 用 1.1 那个 Gmail，在 1.2 那条线路上打开 `claude.ai`。
2. 手机号验证用你能长期收到的号。接码平台的一次性号，等于在申请表上写"我是批量注册"。
3. 姓名填真实拼音，后面支付账单上的名字尽量跟它一致。
4. 注册完先别急着订阅，把页面放一会儿，正常聊两轮。

可能弹人机验证（hCAPTCHA），点就是了，这是正常现象。

不正常的是：注册完立刻要求身份验证，或者登录直接提示地区不可用。这时候别反复重注册，先把 1.2 的线路换干净再试。

## 3. 订阅

### 3.1 选哪一档

| 档位 | 月费 | 适合 |
|---|---|---|
| Pro | $20 | 网页聊天为主，偶尔写点代码 |
| Max x5 | $100 | 每天写代码，Claude Code 是主力工具 |
| Max x20 | $200 | 整天挂着 agent、长上下文、多项目并行 |

Max 的风控比 Pro 更严，秒封秒退款的比例明显更高，第一次别直接上 x20。另外三档都是月付，别买年付，账号出问题的时候年付退不回来。

### 3.2 美区 Apple ID 加礼品卡

1. 注册一个美区 Apple ID，地址选美国免税州，比如 Oregon，州税为 0，充值不额外扣。
2. 往这个 Apple ID 充 App Store 礼品卡。买卡走官方渠道，或者你能追责的代购。
3. 在 iPhone 或 iPad 上装 Claude App，用你的 Claude 账号登录。
4. App 内点订阅，付款方式选 Apple ID 余额。
5. 订阅成功后回网页端刷新，权益已经同步。Claude Code 用同一个账号登录即可。

这一步有个容易忽略的点：订阅动作发生在 Apple 的服务器上，但你的 Claude 账号仍然在记 IP。订阅时用的线路必须跟注册时是同一条。

## 4. 装客户端

### 4.1 网页

`claude.ai`，什么都不用装。Projects、Artifacts、文件上传都在这里。

### 4.2 桌面端

官网下 macOS 或 Windows 版。能读本地文件、能截屏，比网页顺手。

### 4.3 手机

iOS 走美区 Apple ID 下载。Android 走 Google Play，需要一个能访问 Google 的环境。

### 4.4 Claude Code

前提是 Node.js 18 以上。

```bash
node -v
npm install -g @anthropic-ai/claude-code
claude
```

首次运行会打开浏览器走 OAuth 授权，用同一个账号登录，授权完回终端就能用。

国内直连 Anthropic 会超时，要么全程走同一条稳定线路，要么把 Claude Code 装到海外服务器上跑，本地只走 SSH。第二种是长期方案，因为这个仓库里所有关于环境一致性的要求，本质上都是要求 Claude 的出口固定在一台不会变的机器上。

另一个：别把 OAuth 令牌接进第三方工具。Anthropic 2026 年 2 月起明确这违反服务条款。

装完跑一句最小的验证：

```bash
claude -p "用一句话介绍你自己"
```

有输出就通了。

## 5. 头三天怎么用

新号前 72 小时是风控集中观察期。这三天别干这些事：

- 一上来就批量跑任务、爬数据、生成数据集
- 一天几百次调用
- 手机、电脑、服务器三头同时登录
- 频繁改密码、改邮箱、改支付方式

每天多少量算自然、为什么是 72 小时，看 [claude-fangfen](https://github.com/sobadgirl/claude-fangfen) 第 3 节。

一句话版本：头三天像个人一样用。

## 6. 对着症状查

| 症状 | 大概率原因 | 往下走 |
|---|---|---|
| 登录提示地区不可用 | 线路 ASN 被标了 | 换线路，见 1.2 |
| 付款成功但几小时后收到退款邮件 | 卡 BIN 被清退 | 换支付方式，见 1.3 |
| 要求上传证件做身份验证 | 触发 KYC | [claude-fangfen](https://github.com/sobadgirl/claude-fangfen) 的 KYC 一节 |
| 账号停用，邮件说违反条款 | 已封 | [claude-fangfen](https://github.com/sobadgirl/claude-fangfen) 的封号自救一节 |
| Claude Code 一直超时 | 线路或 DNS | 见 4.4 |
| 能聊天但不能调 API | 订阅和 API 额度是两套 | 去 Console 单独开 |

## 附：开工前检查清单

- [ ] 自己注册的 Gmail，开了两步验证，记下注册日期和城市
- [ ] 一条固定线路，查过 ASN 不是机房
- [ ] 美区 Apple ID 已注册，地址填的免税州
- [ ] 礼品卡余额够付你选的那档，且选的是月付
- [ ] 想清楚主要在网页用还是命令行用
- [ ] 读过 [claude-fangfen](https://github.com/sobadgirl/claude-fangfen) 的高风险行为清单
- [ ] 头三天不打算跑批量任务

## 7. 常见问题

### Claude 在国内怎么注册

准备三样：自己注册的 Gmail、一条固定的境外线路、一个能长期收短信的手机号。在 `claude.ai` 填邮箱和手机号，收验证码即可。注册完先正常聊两轮，别急着订阅。

### 注册 Claude 用什么邮箱

自己注册的 Gmail 最稳，开了两步验证。QQ 和 163 也能用，但权重低。买来的二手 Gmail 和一次性邮箱不要碰，风控值是继承的，前一个人做过什么你无法知道。

### 没有海外信用卡怎么订阅 Claude

走美区 Apple ID。注册一个美区账户，用支付宝里的 PockytShop 小程序买 App Store 礼品卡充值，然后在 iPhone 上的 Claude App 里内购。Apple 直接收单，绕开 Stripe，不需要任何海外银行卡。

### 美区 Apple ID 需要美国手机号吗

不需要。苹果支持用中国 +86 手机号接收验证码，国内邮箱也能注册，全程免费，五分钟。只需要把国家或地区选成美国，地址填一个免税州的。

### 美区 Apple ID 填哪个地址

五个免税州任选：俄勒冈、蒙大拿、特拉华、阿拉斯加、新罕布什尔。最常用俄勒冈，邮编 97 开头，区号 503。选免税州的原因很实际：其他州会加 8% 到 10% 的州税，充 20 美元不够付 20 美元的订阅。

### Claude 礼品卡在哪买，买多少

支付宝搜 PockytShop 小程序，地区切到美国，选 App Store 礼品卡，按实时汇率买。第一次要装小火箭（$2.99）加首月 Pro（$20），买 23 到 25 美元比较稳，零头会留在余额里抵扣下个月。

### Claude Pro 和 Max 怎么选

网页聊天、偶尔写代码，Pro 每月 20 美元够了。每天写代码、Claude Code 是主力，Max x5。整天挂着 agent、长上下文、多项目并行，才考虑 Max x20。第一次别直接上最高档，Max 的风控比 Pro 严。

### Claude Code 怎么安装

Node.js 18 以上，然后 `npm install -g @anthropic-ai/claude-code`，运行 `claude` 走 OAuth 授权。国内直连会超时，要么全程同一条线路，要么装在海外服务器上跑、本地走 SSH。

### Claude Code 一直超时怎么办

先确认线路是不是通的，再看 DNS 有没有泄漏。都正常还超时，多半是出口 IP 被限速或者节点本身不稳。别关掉网络反复重试，重试次数多了反而像异常行为。

### Claude 时区要设成什么

跟你线路所在的城市一致。线路在美国就设纽约，别留东八区。IP 在洛杉矶、系统时区是北京时间，这条不用算法也能看出来。Mac 上还要去定位服务里关掉「设置时区」，否则会自动跳回去。

## 贡献

哪一步在你那里对不上，开 Issue 说清楚系统、时间、报错原文。别贴账号、邮箱、卡号、IP 全段。

## License

MIT。本仓库与 Anthropic, PBC 无官方关联。Claude / Anthropic 是 Anthropic, PBC 的注册商标。

## Changelog

2026-11-17 · v1.0 首版：路线选择、三件套、注册、订阅、客户端、观察期、排错表
