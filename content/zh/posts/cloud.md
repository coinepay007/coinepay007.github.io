---
title: Cloudflare 怎么使用？新手必学的 10 个核心功能详解
slug: cloud
date: 2026-11-03
draft: false
---


# Cloudflare 怎么使用？新手必学的 10 个核心功能详解（2026 年完整教程）

Cloudflare 是目前非常受欢迎的网站加速与安全服务平台，可以帮助网站管理员管理 DNS 解析、提高网页访问速度、配置 SSL 证书、抵御恶意流量，并提供 Workers、Pages 等开发工具。

无论你是刚刚搭建个人博客、运营企业网站，还是使用 WordPress、GitHub Pages 或其他建站平台，都可以通过 Cloudflare 优化网站的访问体验。

对于刚开始接触 Cloudflare 的用户来说，最重要的不是一次性开启所有功能，而是先掌握域名接入、DNS 解析、CDN 加速、HTTPS 配置和基础安全防护。

本文将从注册账号开始，详细介绍 Cloudflare 新手必学的 10 个核心功能，并说明每个功能的用途、配置方法和注意事项。

如果你经常使用在线服务，也可以了解不同的在线支付工具和相关网络服务。例如，CoinePay 提供虚拟卡相关服务，适合有在线支付管理需求的用户了解；TRXAPI 则提供 TRON 网络能量租赁服务。这些都是独立的第三方服务，与 Cloudflare 没有官方合作或集成关系。

## 一、CoinePay 与 TRXAPI 服务介绍

### 1. CoinePay：在线支付虚拟卡服务

如果你经常使用海外网站、在线工具或数字服务，可以了解 CoinePay 提供的虚拟卡服务。

具体支持哪些商户和交易类型，需要以平台当前公布的服务条款及实际支付结果为准。

👉 [https://www.coinepay.net/login?referrer=7PFFZMCH](https://www.coinepay.net/login?referrer=7PFFZMCH)

### 2. TRXAPI：TRON 网络能量租赁服务

对于经常使用 TRON 网络进行 USDT TRC20 转账的用户，可以了解 TRXAPI 提供的能量租赁服务。

通过租赁能量，用户可以根据自身的转账需求管理部分 TRON 网络交易资源。

平台入口：

[https://www.trxapi.io/energy.html?lang=zh-TW](https://www.trxapi.io/energy.html?lang=zh-TW)

TRXAPI 邀请码：57YQDGFU

需要注意，CoinePay 和 TRXAPI 都是独立服务，与 Cloudflare 无官方关联。它们不能代替 Cloudflare 的域名管理、网站加速或安全防护功能。

## 二、Cloudflare 是什么？主要能做什么？

Cloudflare 是一家提供互联网基础设施服务的公司，主要业务包括 CDN、DNS、网站安全、网络性能优化和开发者平台。

简单来说，你可以把 Cloudflare 理解为网站与访客之间的一层网络服务。

当网站接入 Cloudflare 后，符合代理条件的访问请求可以先经过 Cloudflare 网络，再转发到你自己的服务器。

这样可以根据配置实现：

- 提高网站静态资源的访问速度。
- 缓存图片、CSS、JavaScript 等内容。
- 配置 HTTPS 加密连接。
- 过滤部分恶意访问和攻击流量。
- 管理域名 DNS 解析。
- 查看网站访问量和安全事件。
- 部署无服务器应用和静态网站。

Cloudflare 提供免费和付费方案，不同方案支持的功能和使用额度可能不同。新手可以先从免费方案开始，再根据网站需求决定是否升级。

官方入口：

[https://www.cloudflare.com/](https://www.cloudflare.com/)

官方文档：

[https://developers.cloudflare.com/](https://developers.cloudflare.com/)

## 三、Cloudflare 注册与域名接入教程

在使用 Cloudflare 的大部分网站功能之前，需要先注册账号并将域名添加到 Cloudflare。

### 1. 注册 Cloudflare 账号

首先打开 Cloudflare 官方网站：

[https://dash.cloudflare.com/sign-up](https://dash.cloudflare.com/sign-up)

按照页面提示填写电子邮箱和密码，完成账号注册。

注册完成后，登录 Cloudflare 控制面板。

### 2. 添加网站域名

登录后，找到添加网站或添加域名的入口。

输入你已经拥有的域名，例如：

`example.com`

这里需要填写的是自己的主域名，而不是完整的网站页面地址。

例如：

- 正确：`example.com`
- 通常不需要填写：`https://www.example.com/article`

按照页面提示选择适合自己的套餐。初次使用可以先选择 Free 免费方案。

### 3. 检查 DNS 记录

Cloudflare 通常会扫描现有域名的 DNS 记录，并尝试导入相关配置。

常见 DNS 记录包括：

- A：将域名指向 IPv4 地址。
- AAAA：将域名指向 IPv6 地址。
- CNAME：将一个域名指向另一个域名。
- MX：设置邮件服务器。
- TXT：用于域名验证、SPF、DKIM 等配置。

检查导入的记录是否完整，尤其要确认网站服务器 IP、邮件服务器和其他正在使用的服务没有遗漏。

### 4. 修改域名 Nameservers

完成域名添加后，Cloudflare 会提供两条分配给你域名的 Nameservers（名称服务器）。

登录你的域名注册商后台，找到域名 DNS 或 Nameserver 设置，将原来的名称服务器替换为 Cloudflare 提供的两条地址。

注意：

- 必须使用 Cloudflare 页面实际分配的名称服务器。
- 不要直接复制其他网站的 Nameserver。
- 修改前建议保存原有 DNS 配置。
- DNS 生效需要一定时间，具体取决于注册商和 DNS 缓存情况。

修改完成后，返回 Cloudflare 控制面板，等待系统确认域名激活。

只有在域名状态显示为 Active 后，才能正常使用大部分针对该域名的 Cloudflare 功能。

## 四、Cloudflare 新手必学的 10 个核心功能

下面介绍 Cloudflare 最值得新手掌握的 10 个功能。

## 功能一：DNS 域名解析

<AsyncImage query="Cloudflare dashboard DNS records management interface screenshot" aspectRatio="16:9" width="100%" />

DNS 是 Cloudflare 最基础、最重要的功能之一。

DNS 的主要作用是将域名解析到对应的服务器或其他网络服务。

例如，当访客访问：

`www.example.com`

DNS 系统会根据配置找到对应的目标地址。

### 如何配置 DNS？

登录 Cloudflare 后：

1. 选择需要管理的域名。
2. 打开 DNS 设置。
3. 进入 Records（记录）页面。
4. 点击 Add record（添加记录）。
5. 选择记录类型。
6. 填写名称和目标地址。
7. 保存配置。

例如，网站服务器使用 IPv4 地址时，可以添加一条 A 记录：

- Type：A
- Name：@
- IPv4 address：你的服务器 IP
- TTL：Auto

如果还需要让 www 子域名指向主域名，可以根据实际情况添加 CNAME 记录。

### DNS 记录中的橙色云朵和灰色云朵有什么区别？

Cloudflare DNS 记录通常会显示两种代理状态：

**橙色云朵：Proxied**

表示通过 Cloudflare 代理符合条件的 HTTP/HTTPS 流量，可以使用相关 CDN 和安全功能。

**灰色云朵：DNS only**

表示只使用 Cloudflare 提供 DNS 解析，不通过 Cloudflare 代理该记录的流量。

新手需要注意，不是所有 DNS 记录都适合开启代理。邮件服务器、部分验证记录和不支持代理的服务，应根据具体用途设置。

## 功能二：CDN 网站加速

<AsyncImage query="Cloudflare CDN global network website content delivery illustration" aspectRatio="16:9" width="100%" />

CDN 是 Cloudflare 最受欢迎的功能之一。

CDN 的全称是 Content Delivery Network，即内容分发网络。

它的主要作用是通过分布在不同地区的网络节点缓存和分发网站内容，让访客能够更快地获取部分网页资源。

### CDN 能加速哪些内容？

常见的缓存资源包括：

- 网站图片。
- CSS 样式文件。
- JavaScript 文件。
- 字体文件。
- 其他适合缓存的静态资源。

### 如何开启 Cloudflare CDN？

一般来说，可以按照以下步骤操作：

1. 登录 Cloudflare。
2. 选择需要配置的域名。
3. 打开 DNS 设置。
4. 找到网站对应的 A 或 CNAME 记录。
5. 确认该记录支持代理。
6. 将代理状态设置为橙色云朵 Proxied。

完成后，符合条件的 HTTP/HTTPS 请求就可以通过 Cloudflare 网络进行代理。

需要注意，CDN 并不意味着所有动态请求都会自动缓存。网站的缓存规则、响应头和资源类型都会影响实际效果。

## 功能三：SSL/TLS 证书与 HTTPS 加密

<AsyncImage query="Cloudflare SSL TLS encryption dashboard mode settings screenshot" aspectRatio="16:9" width="100%" />

SSL/TLS 是保护网站通信安全的重要功能。

配置 HTTPS 后，浏览器与网站之间的数据传输可以通过加密连接进行，减少数据在传输过程中被窃取或篡改的风险。

### Cloudflare SSL/TLS 有什么作用？

主要包括：

- 为网站提供 HTTPS 访问。
- 加密访客与 Cloudflare 之间的连接。
- 根据配置加密 Cloudflare 与源站服务器之间的连接。
- 帮助网站建立更安全的访问环境。

### 如何配置 SSL/TLS？

操作步骤：

1. 登录 Cloudflare。
2. 选择目标域名。
3. 打开 SSL/TLS。
4. 进入 Overview。
5. 查看当前加密模式。
6. 根据源站服务器的证书情况选择合适模式。

常见模式包括：

**Off：** 不使用 Cloudflare SSL/TLS 加密。

**Flexible：** 浏览器到 Cloudflare 使用 HTTPS，但 Cloudflare 到源站使用 HTTP。

**Full：** 浏览器到 Cloudflare 使用 HTTPS，Cloudflare 到源站也使用 HTTPS，但不会严格验证源站证书的有效性。

**Full (strict)：** 浏览器到 Cloudflare 和 Cloudflare 到源站都使用 HTTPS，并验证源站证书。

对于已经正确安装有效 SSL 证书的源站，通常建议使用 Full (strict)。

如果源站没有正确配置 HTTPS，不要直接切换到 Full (strict)，否则可能导致网站出现 525 或 526 等连接错误。

## 功能四：缓存管理与 Cache Rules

<AsyncImage query="Cloudflare caching cache rules dashboard configuration screenshot" aspectRatio="16:9" width="100%" />

Cloudflare 缓存功能可以减少重复访问时对源站服务器的请求，从而改善网站访问速度。

例如，网站有大量图片、CSS 和 JavaScript 文件，这些资源在适当配置后可以由 Cloudflare 缓存并提供给访客。

### 如何清理 Cloudflare 缓存？

当网站修改了图片、样式或页面内容，但访客仍然看到旧版本时，可以尝试清理缓存。

操作步骤：

1. 登录 Cloudflare。
2. 选择目标域名。
3. 打开 Caching（缓存）。
4. 找到 Configuration（配置）。
5. 使用 Purge Cache（清理缓存）功能。
6. 根据需要选择清理全部缓存或指定 URL。

### 什么是 Cache Rules？

Cache Rules 可以根据 URL、请求条件等规则控制内容是否缓存，以及缓存时间等行为。

例如，你可以针对图片目录设置缓存规则，但不要随意缓存登录页面、购物车、用户个人中心或其他包含个性化数据的页面。

错误的缓存配置可能导致访客看到过期内容，甚至出现账号数据混淆等问题。

## 功能五：DDoS 防护与基础安全保护

<AsyncImage query="Cloudflare DDoS protection security dashboard analytics screenshot" aspectRatio="16:9" width="100%" />

DDoS 攻击是网站运营中常见的安全威胁之一。

攻击者可能通过大量请求消耗网站服务器资源，导致正常用户无法访问。

Cloudflare 提供网络层和应用层的相关防护能力，可以帮助网站过滤和缓解部分恶意流量。

### Cloudflare DDoS 防护有什么作用？

主要包括：

- 缓解部分大规模恶意流量攻击。
- 保护网站正常访问。
- 减少源站服务器直接承受的流量压力。
- 配合其他安全规则过滤异常请求。

### 新手如何使用安全防护？

1. 登录 Cloudflare。
2. 选择网站域名。
3. 打开 Security（安全）相关设置。
4. 查看当前安全配置。
5. 根据网站情况调整防护选项。
6. 通过 Security Events 查看被拦截或触发规则的请求。

Cloudflare 会根据套餐提供不同的安全功能。不要认为开启 Cloudflare 后网站就能完全免受所有攻击，源站服务器本身仍然需要做好安全配置。

## 功能六：WAF 网站应用防火墙

<AsyncImage query="Cloudflare WAF custom security rules dashboard interface" aspectRatio="16:9" width="100%" />

WAF 的全称是 Web Application Firewall，即网站应用防火墙。

它主要用于检查进入网站的 HTTP 请求，并根据安全规则识别和处理可疑访问。

Cloudflare WAF 可以帮助网站管理员过滤一些常见的恶意请求和应用层攻击。

### WAF 可以防护哪些问题？

例如：

- 部分 SQL 注入攻击。
- 部分跨站脚本攻击。
- 异常访问请求。
- 恶意自动化流量。
- 针对网站特定路径的可疑请求。

### 如何设置 WAF？

一般可以按照以下步骤操作：

1. 登录 Cloudflare。
2. 选择目标域名。
3. 打开 Security。
4. 找到 WAF。
5. 查看可用的 Managed Rules 和 Custom Rules。
6. 根据网站实际情况配置规则。

Cloudflare 支持使用自定义规则，根据 IP 地址、URL 路径、请求头等条件匹配访问请求，并执行相应操作。

例如，可以针对某个不需要公开访问的后台路径设置额外的访问限制。

需要注意，规则设置过于严格可能误拦截正常访客。建议先检查安全事件，再逐步调整规则。

## 功能七：Redirect Rules 网站重定向

<AsyncImage query="Cloudflare redirect rules dashboard URL forwarding configuration" aspectRatio="16:9" width="100%" />

Redirect Rules 是网站管理中非常实用的功能。

它可以将一个 URL 自动跳转到另一个 URL。

例如：

`http://example.com`

跳转到：

`https://example.com`

也可以将旧页面跳转到新的页面，减少网站改版或更换链接后产生的访问问题。

### 如何设置重定向？

1. 登录 Cloudflare。
2. 选择需要配置的域名。
3. 打开 Rules（规则）。
4. 找到 Redirect Rules。
5. 创建新的重定向规则。
6. 设置匹配条件。
7. 填写目标 URL。
8. 选择重定向状态码并保存。

常见状态码包括：

- 301：永久重定向。
- 302：临时重定向。

如果页面地址永久更换，可以考虑使用 301；如果只是临时跳转，则可以根据需求使用 302。

设置完成后，建议使用浏览器测试新旧 URL，确认跳转方向和目标地址正确。

## 功能八：Analytics 网站流量分析

<AsyncImage query="Cloudflare website analytics traffic security performance dashboard screenshot" aspectRatio="16:9" width="100%" />

Cloudflare Analytics 可以帮助网站管理员了解网站的访问情况和网络表现。

对于运营博客、企业网站或内容站点的用户来说，流量数据可以帮助判断网站是否正常运行，以及是否存在异常访问。

### Analytics 可以查看哪些数据？

根据当前产品和套餐，通常可以查看相关指标，例如：

- 请求数量。
- 流量数据。
- 缓存命中情况。
- 安全事件。
- 访客相关统计。
- 源站请求情况。
- 网络性能指标。

### 如何查看网站数据？

1. 登录 Cloudflare。
2. 选择需要查看的域名。
3. 打开 Analytics。
4. 选择需要查看的数据分类。
5. 设置时间范围。
6. 查看流量和安全相关指标。

通过这些数据，你可以了解网站访问是否突然增加、缓存是否正常，以及是否存在异常请求。

需要注意，Cloudflare Analytics 的统计口径与 Google Analytics 等网站分析工具并不完全相同，两者的数据不一定一致。

## 功能九：Cloudflare Workers

<AsyncImage query="Cloudflare Workers dashboard code editor deployment interface" aspectRatio="16:9" width="100%" />

Cloudflare Workers 是 Cloudflare 提供的开发者平台功能，可以在 Cloudflare 网络上运行代码。

简单来说，它可以让开发者在不自行管理传统服务器的情况下，部署一些网络应用和后端逻辑。

### Workers 可以用来做什么？

常见用途包括：

- 创建 API 接口。
- 处理 HTTP 请求。
- 实现简单的数据处理逻辑。
- 构建动态网页功能。
- 连接数据库或其他外部服务。
- 部署轻量级应用。

### 如何创建 Workers？

1. 登录 Cloudflare。
2. 进入 Workers & Pages。
3. 选择创建应用或 Worker。
4. 按照界面提示创建项目。
5. 编写或导入代码。
6. 部署项目。
7. 使用分配的访问地址进行测试。

Workers 的使用方式适合有一定编程基础的用户。如果你只是想给普通网站配置 DNS 和 CDN，不需要专门学习 Workers。

此外，Workers 的运行额度、资源限制和部分高级功能可能因套餐而异，使用前应查看官方说明。

## 功能十：Cloudflare Pages 静态网站部署

<AsyncImage query="Cloudflare Pages GitHub repository deployment dashboard interface" aspectRatio="16:9" width="100%" />

Cloudflare Pages 是一个网站部署平台，适合发布静态网站和前端项目。

如果你使用 GitHub 管理网站代码，可以将仓库连接到 Cloudflare Pages，实现自动部署。

### Pages 适合哪些网站？

例如：

- 个人博客。
- 企业展示网站。
- 产品介绍页面。
- 文档网站。
- 静态网页项目。
- 前端开发项目。

### 如何使用 Cloudflare Pages？

1. 登录 Cloudflare。
2. 进入 Workers & Pages。
3. 选择创建应用。
4. 选择 Pages 相关部署方式。
5. 连接 GitHub 仓库。
6. 选择需要部署的代码仓库。
7. 配置构建命令和输出目录。
8. 开始部署。

部署成功后，Cloudflare 会提供一个可以访问的网站地址。

如果你有自己的域名，还可以按照页面提示绑定自定义域名。

需要注意，具体构建配置取决于你使用的前端框架和项目结构。不同项目的构建命令和输出目录可能不同。

## 五、Cloudflare 新手应该如何配置？

如果你刚刚注册 Cloudflare，不建议一次性开启所有功能。

对于普通博客、企业网站和内容站点，可以按照下面的顺序进行配置。

### 第一步：完成域名接入

先将域名添加到 Cloudflare，检查 DNS 记录，并按照要求修改域名 Nameservers。

### 第二步：确认 DNS 解析正常

检查网站主域名和 www 子域名是否都能正常访问。

如果网站无法打开，先检查 DNS 记录和源站服务器状态。

### 第三步：配置 HTTPS

根据源站证书情况设置 SSL/TLS 模式。

如果源站已经安装有效证书，通常可以使用 Full (strict) 模式。

### 第四步：开启 CDN 代理

将适合代理的网站 DNS 记录设置为橙色云朵。

确认网站可以正常访问后，再观察缓存和性能数据。

### 第五步：配置缓存规则

根据网站资源类型设置缓存策略。

图片、CSS 和 JavaScript 等静态资源可以根据实际情况进行缓存；登录、支付和用户个人信息页面则应谨慎处理。

### 第六步：检查安全设置

查看 Cloudflare 的安全事件和可用防护规则。

如果发现异常访问，可以根据实际情况配置 WAF 或其他安全规则。

### 第七步：定期查看 Analytics

通过 Analytics 了解网站流量、缓存和安全情况，发现异常后及时排查。

## 六、Cloudflare 使用过程中常见的问题

### 1. Cloudflare 接入后网站打不开怎么办？

可能原因包括：

- DNS 记录配置错误。
- 域名 Nameservers 尚未生效。
- 源站服务器无法访问。
- SSL/TLS 模式配置不正确。
- 防火墙阻止了 Cloudflare 的连接。

建议先确认 DNS 解析和源站服务器是否正常，再检查 SSL/TLS 设置。

### 2. Cloudflare 显示 522 错误怎么办？

522 通常表示 Cloudflare 与源站服务器建立连接时发生超时。

可以检查：

- 源站服务器是否正常运行。
- 服务器防火墙是否允许 Cloudflare 的访问。
- 源站是否负载过高。
- DNS 记录中的服务器 IP 是否正确。
- 网络连接是否存在问题。

### 3. Cloudflare 显示 525 错误怎么办？

525 通常表示 Cloudflare 与源站之间的 SSL 握手失败。

可以检查：

- 源站 HTTPS 是否正常。
- 源站是否正确安装 SSL 证书。
- 服务器是否支持对应的 TLS 配置。
- SSL/TLS 模式是否与源站配置匹配。

### 4. 开启 Cloudflare 后网站图片没有更新怎么办？

可能是 Cloudflare 或浏览器仍在使用旧缓存。

可以尝试：

1. 登录 Cloudflare。
2. 选择目标域名。
3. 打开 Caching。
4. 使用 Purge Cache 清理相关缓存。
5. 刷新浏览器页面。

如果问题仍然存在，需要检查源站文件是否真的更新成功。

### 5. Cloudflare 免费版够用吗？

对于个人博客、小型企业网站和普通内容站点，免费版通常可以作为入门选择。

如果网站需要更高级的 WAF 功能、更多安全规则、额外性能优化或企业级服务，可以根据实际需求考虑付费套餐。

具体功能和限制应以 Cloudflare 当前官方套餐说明为准。

## 七、Cloudflare 官方资源与学习入口

如果想进一步学习 Cloudflare 的使用方法，可以通过以下官方入口获取资料。

**Cloudflare 官方网站**

[https://www.cloudflare.com/](https://www.cloudflare.com/)

**Cloudflare 登录入口**

[https://dash.cloudflare.com/](https://dash.cloudflare.com/)

**Cloudflare 官方文档**

[https://developers.cloudflare.com/](https://developers.cloudflare.com/)

**Cloudflare DNS 文档**

[https://developers.cloudflare.com/dns/](https://developers.cloudflare.com/dns/)

**Cloudflare SSL/TLS 文档**

[https://developers.cloudflare.com/ssl/](https://developers.cloudflare.com/ssl/)

**Cloudflare WAF 文档**

[https://developers.cloudflare.com/waf/](https://developers.cloudflare.com/waf/)

**Cloudflare Workers 文档**

[https://developers.cloudflare.com/workers/](https://developers.cloudflare.com/workers/)

**Cloudflare Pages 文档**

[https://developers.cloudflare.com/pages/](https://developers.cloudflare.com/pages/)

## 八、总结：Cloudflare 新手应该先学会哪些功能？

Cloudflare 的功能非常丰富，但对于刚开始使用的用户来说，最重要的是先掌握网站接入和基础配置。

本文介绍的 10 个核心功能分别是：

1. DNS：管理域名解析。
2. CDN：加速网站静态资源访问。
3. SSL/TLS：配置 HTTPS 加密。
4. Cache Rules：管理网站缓存。
5. DDoS 防护：缓解恶意流量攻击。
6. WAF：过滤可疑网站请求。
7. Redirect Rules：配置 URL 重定向。
8. Analytics：查看网站流量和安全数据。
9. Workers：部署网络应用和后端代码。
10. Pages：部署静态网站和前端项目。

对于普通网站管理员，建议优先学习 DNS、CDN、SSL/TLS、缓存和安全防护。这些功能可以满足大部分基础网站运营需求。

如果你正在搭建个人博客、企业网站或内容站点，可以先使用 Cloudflare 免费方案完成基础配置，再根据访问量、网站类型和安全需求逐步学习高级功能。

同时，建议定期检查 DNS、SSL/TLS 和缓存配置，避免因为错误设置导致网站无法访问。

Cloudflare 不只是一个 CDN 工具，也是一个集 DNS、网络安全、网站加速和开发者服务于一体的平台。掌握这些基础功能，可以帮助你更好地管理网站并提高网站运行的稳定性。

如果你还需要了解在线支付工具，可以访问 CoinePay：

[https://www.coinepay.net/login?referrer=7PFFZMCH](https://www.coinepay.net/login?referrer=7PFFZMCH)

如果你经常使用 TRON 网络进行 USDT TRC20 转账，也可以了解 TRXAPI 能量租赁服务：

[https://www.trxapi.io/energy.html?lang=zh-TW](https://www.trxapi.io/energy.html?lang=zh-TW)

TRXAPI 邀请码：57YQDGFU

以上第三方服务与 Cloudflare 无官方合作关系，用户应根据自身需求和服务条款独立判断是否使用。

## 参考资料

- Cloudflare 官方网站：[https://www.cloudflare.com/](https://www.cloudflare.com/)
- Cloudflare 官方文档：[https://developers.cloudflare.com/](https://developers.cloudflare.com/)
- Cloudflare 产品介绍：[https://www.cloudflare.com/products/](https://www.cloudflare.com/products/)
- Cloudflare WAF 文档：[https://developers.cloudflare.com/waf/](https://developers.cloudflare.com/waf/)
- Cloudflare Analytics 文档：[https://developers.cloudflare.com/analytics/](https://developers.cloudflare.com/analytics/)

