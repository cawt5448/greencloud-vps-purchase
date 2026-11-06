# 绿云vps购买教程：从选套餐选机房到支付宝付款，一次讲清真实价格、退款政策和容易踩坑的隐藏限制

绿云（GreenCloud）的 VPS 从每月 6 美元起步，支持支付宝和微信付款，注册账户、选套餐、选机房、下单四步就能完成购买。对国内用户来说，流程本身不难，真正容易出问题的是三件事：套餐太多不知道选哪档、机房线路挑错导致晚高峰卡顿、以及下单前没看清退款条件。这篇文章把这三件事连同购买步骤一起讲清楚。

> **选购速览**：大多数个人用户选 **Ryzen KVM VPS** 或 **Budget KVM VPS** 的最低档就够了，$6/月、1 核 1G、NVMe 或 SSD 存储，10Gbps 端口；国内访问优先香港、日本、洛杉矶、旧金山机房。新客户首个 VPS 套餐有 7 天退款窗口（促销套餐除外）。
> 👉 [查看绿云全部套餐与当前价格](https://greencloudvps.com/billing/aff.php?aff=6679)

## 绿云的套餐分哪几类？价格是多少？

绿云的 KVM VPS 分五大系列：EPYC VDS（独占资源）、Ryzen VPS（高频 CPU + NVMe）、Budget KVM VPS（入门 SSD）、10Gbps VPS 和 Storage VPS（大盘鸡），官网均为月付计价；另外还有 Windows VPS、Forex VPS、MacOS VPS 和独立服务器产品线。下面两张表是已核验到具体价格的套餐。

**Linux KVM VPS（月付，10Gbps 端口，含 1 次免费备份/快照）**

| 套餐 | CPU / 内存 | 存储 | 流量（美欧 / APAC） | 月付 | 购买 |
| --- | --- | --- | --- | --- | --- |
| Budget SSDKVM-1 | 1 核 / 1 GB | 15 GB SSD | 1.5 TB / 750 GB | $6 | [开通 SSDKVM-1](https://greencloudvps.com/billing/aff.php?aff=6679&pid=kvmla-1) |
| Budget SSDKVM-2 | 1 核 / 2 GB | 15 GB SSD | 2 TB / 1 TB | $10 | [开通 SSDKVM-2](https://greencloudvps.com/billing/aff.php?aff=6679&pid=kvmla-2) |
| Budget SSDKVM-3 | 2 核 / 4 GB | 30 GB SSD | 4 TB / 2 TB | $20 | [开通 SSDKVM-3](https://greencloudvps.com/billing/aff.php?aff=6679&pid=kvmla-3) |
| Budget SSDKVM-4 | 4 核 / 8 GB | 60 GB SSD | 8 TB / 4 TB | $40 | [开通 SSDKVM-4](https://greencloudvps.com/billing/aff.php?aff=6679&pid=kvmla-4) |
| Budget SSDKVM-5 | 8 核 / 16 GB | 120 GB SSD | 12 TB / 6 TB | $80 | [开通 SSDKVM-5](https://greencloudvps.com/billing/aff.php?aff=6679&pid=kvmla-5) |
| Ryzen-1 | 1 核 3.5+ GHz / 1 GB | 15 GB NVMe | 1.5 TB | $6 | [开通 Ryzen-1](https://greencloudvps.com/billing/aff.php?aff=6679&pid=ryzenlavf-1) |
| Ryzen-2 | 1 核 / 2 GB | 30 GB NVMe | 2 TB | $10 | [开通 Ryzen-2](https://greencloudvps.com/billing/aff.php?aff=6679&pid=ryzenlavf-2) |
| Ryzen-3 | 2 核 / 4 GB | 50 GB NVMe | 4 TB | $20 | [开通 Ryzen-3](https://greencloudvps.com/billing/aff.php?aff=6679&pid=ryzenlavf-3) |
| Ryzen-4 | 4 核 / 8 GB | 80 GB NVMe | 8 TB | $40 | [开通 Ryzen-4](https://greencloudvps.com/billing/aff.php?aff=6679&pid=ryzenlavf-4) |
| Ryzen-5 | 8 核 / 16 GB | 150 GB NVMe | 12 TB | $80 | [开通 Ryzen-5](https://greencloudvps.com/billing/aff.php?aff=6679&pid=ryzenlavf-5) |

两个系列同档位价格完全一样，区别在磁盘和 CPU 型号：Ryzen 系列用 NVMe 4.0 盘，数据库、WordPress 这类读写密集的应用优先选它；Budget 系列是普通 SSD，跑代理、轻量服务足够。

**Windows VPS（月付，Windows Server 2022）**

| 套餐 | 配置 | 月付 | 购买 |
| --- | --- | --- | --- |
| Budget US1 | 1 核 / 1 GB / 25 GB SSD，1Gbps 不限流量 | $8 | [开通 US1](https://greencloudvps.com/billing/aff.php?aff=6679&pid=335) |
| Budget US1.5 | 1 核 / 1.5 GB / 30 GB | $12 | [开通 US1.5](https://greencloudvps.com/billing/aff.php?aff=6679&pid=339) |
| Budget US2 | 2 核 / 2 GB / 40 GB | $16 | [开通 US2](https://greencloudvps.com/billing/aff.php?aff=6679&pid=340) |
| Budget US3 | 2 核 / 3 GB / 60 GB | $24 | [开通 US3](https://greencloudvps.com/billing/aff.php?aff=6679&pid=341) |
| Budget US4 | 4 核 / 4 GB / 80 GB | $32 | [开通 US4](https://greencloudvps.com/billing/aff.php?aff=6679&pid=342) |
| Budget US5 | 5 核 / 5 GB / 100 GB | $40 | [开通 US5](https://greencloudvps.com/billing/aff.php?aff=6679&pid=343) |
| Budget US6 | 6 核 / 6 GB / 120 GB | $48 | [开通 US6](https://greencloudvps.com/billing/aff.php?aff=6679&pid=344) |
| SuperSaving Budget-1 | 1 核 / **2 GB** / 25 GB SSD（季付起，内存翻倍） | $10 | [开通 SuperSaving Budget-1](https://greencloudvps.com/billing/aff.php?aff=6679&pid=334) |
| Windows 10Gbps-1 | 2 核 / 4 GB / 60 GB SSD，10Gbps 不限流量 | $35 | [查看 Windows 10Gbps 套餐](https://greencloudvps.com/billing/aff.php?aff=6679) |
| Windows 10Gbps-3 | 6 核 / 9 GB / 120 GB SSD，10Gbps 不限流量 | $82 | [查看 Windows 10Gbps 套餐](https://greencloudvps.com/billing/aff.php?aff=6679) |

Windows 这边有个值得算账的点：Normal 档 US1 是 1 GB 内存 $8/月，SuperSaving 档同样的钱按季度付，内存直接翻倍到 2 GB。打算长期用的话，SuperSaving 明显更划算；只是临时挂个软件，月付 Normal 档更灵活。

EPYC VDS、Storage VPS、MacOS VPS 和独立服务器这几条线，官网确认存在但本文没有核验到逐档价格，下单前建议在官网对应页面确认实时报价。

## 绿云购买流程：从注册到付款的完整步骤

绿云没有独立的注册入口，账户是随第一笔订单一起创建的，所以直接从选套餐开始。整个流程六步：

1. **选产品类型**。先决定 Windows 还是 Linux VPS，再选 1Gbps 还是 10Gbps 带宽，然后点进对应系列的套餐页。
2. **选套餐和机房**。美国、欧洲机房的套餐需要先选数据中心；亚太机房同理。选哪里的逻辑下一节单独讲。
3. **配置操作系统**。在配置中心选择需要的系统版本，Linux 常见发行版都可以一键安装。
4. **填写账户信息**。邮箱和密码务必记住，后续账单、工单、重装都靠这个账户。
5. **选付款方式**。支持**支付宝和微信**，也有 PayPal、信用卡、银联和加密货币。注意一点：用加密货币付款不参与退款。
6. **勾选同意协议，提交订单**。付款完成后机器自动开通，Linux 机器通过 SSH 登录，Windows 通过 RDP 登录。

还有一个购买环节的现实问题：绿云的特价套餐经常处于缺货状态。官网购物车里曾出现过 EPYC NYC 特价套餐标注“0 可用”的情况，这类套餐补货时间不固定，有购买教程建议需要时反复刷新页面蹲补货。

## 机房怎么选？国内用户看线路

国内访问优先考虑香港、日本、洛杉矶、旧金山这四个机房。已核验的线路情况是：香港走 CN2 直连，延迟非常低；旧金山是 CN2 线路；新加坡直连；洛杉矶延迟也比较低；东京延迟相对多一些。

两点提醒。第一，上面说的低价套餐大部分是标准国际 BGP 路由，晚高峰直连国内可能拥堵丢包，对延迟敏感的业务建议配合 CDN 或中转使用。第二，APAC（亚太）机房的流量配额只有美国和欧洲机房的一半，比如 SSDKVM-1 在美欧是 1.5 TB，亚太机房只有 750 GB——流量用超后加购的价格差距更大：美国/欧盟 $3/TB/月，亚太 $15/TB/月。如果流量需求大，美西机房通常比亚太机房更划算。

另外，VPS 交付后想换位置要收 $3 一次性费用，亚太区域内只能在同一国家的机房之间换（比如新加坡两个机房互转），美国和欧盟区域内可以任意换。

## 退款政策和账单规则：下单前必须看清的部分

绿云的退款条款比大多数主机商严格，下单前把这几条看完能省掉很多麻烦：

- **新客户 7 天退款窗口**：注册账户后 7 天内，可对首个 VPS 套餐申请退款。
- **促销套餐一律不退**：所有特价、闪购、促销套餐（Promotional / Special Offers）不在退款范围内，包括使用折扣码的套餐。
- **加密货币付款不退**。
- **附加服务不退**：加购的 IP、带宽、存储等都不退。
- **已用流量超 10% 不符合退款条件**，被暂停或因违规终止的服务也不退。

账单规则同样值得留意：账单在到期日前 14 天生成，逾期 2 天收 10% 滞纳金，逾期 1 天可能暂停服务，3 天后可能直接终止。VPS 这类产品到期不续费机器就没了，数据记得提前备份。取消服务走 Client Area → Services → My Services → Request Cancellation，取消本身不等于退款。

一句话概括：抱着“买来试用、不好就退”的心态，只有新客户首个原价套餐这唯一一次机会；买特价套餐就当钱花了不退来决策。

## 那些教程不会告诉你的限制

下面几条来自绿云官方服务条款和第三方价格追踪页，普通测评文章大多不提，但每一条都可能直接影响你的使用体验：

- **IP 被墙的处理**：中国客户在 VPS 交付后 3 小时内，如果 IP 被屏蔽，可以免费更换一次 IP；超过 3 小时再换要收 $2。拿到机器后尽早测试连通性是有实际好处的。
- **端口是公平共享的**：即使是 10Gbps 套餐，持续超过 100 Mbps 跑满 6 小时、或频繁打满端口都不被允许。
- **CPU 不能长期占满**：连续 10 分钟以上占满 100% 系统资源属于违规，长时间视频转码、编译大型项目这类任务容易被限速甚至关机。绿云是 Unmanaged（无托管）服务，客服只管硬件和底层网络，系统里的软件问题一律自己解决。
- **用途禁令**：游戏服务器（CS、Half-Life 等）、TOR、直播/流媒体传输都在禁止列表里。
- **拒付等于封号**：发起 PayPal 或信用卡 chargeback 会导致所有服务立即暂停或终止。
- **加购价格透明**：+1 GB 内存 $5/月、+1 核 CPU $5/月、+20 GB SSD $5/月（最多加到套餐自带容量的两倍），后续扩容不用换套餐。

## 常见问题

**绿云支持支付宝吗？**
支持。付款方式里有支付宝和微信，国内用户不需要国际信用卡就能完成购买。

**绿云便宜套餐能用来建站吗？**
可以。$6/月档位就是完整的 KVM 虚拟机，带独立 IPv4、/64 IPv6 和 root 权限，控制面板支持一键重装和快照。注意选对机房，面向国内访客优先香港 CN2 或美西。

** Windows VPS 是正版的吗？**
绿云的 Windows VPS 预装 Windows Server 2022 并开启 RDP，系统由服务商提供，不需要你自己处理授权问题。

**被墙了怎么办？**
记住 3 小时这个节点：交付后 3 小时内发现 IP 被屏蔽可免费换一次，之后每次 $2。再不行可以花 $3 换机房位置。

## 下单前的最后建议

按需求对号入座：跑博客、轻量应用，Ryzen-1 或 SSDKVM-1 的 $6/月档位直接够用；数据库和读写密集的服务，同价位选 NVMe 的 Ryzen 系列；要 Windows 桌面挂软件，Normal US1 起步，长期用就上 SuperSaving；大流量需求避开亚太机房（配额减半、加购贵五倍）。

下单前最后确认两件事：机房线路是否符合你的访问场景，以及你选的是不是促销套餐——后者不退款，想保留 7 天退款保障就选原价套餐。确认好就可以 👉 [进入绿云官网选套餐付款](https://greencloudvps.com/billing/aff.php?aff=6679)。
