---
layout: post
title: 🍪 JSON Web Tokens
categories: codetips
---

# JSON Web Tokens

JWT 见到的次数还挺多的，照猫画虎的用过，然而一经拷打就会露出底裤，所以整理记录一下

## Session

Session 是一个虚拟概念，不代指任何实体和数据，常被翻译为“会话”，代表了「一次」相互沟通，可包括多次通信

### Session-Data

代表在一次 Session 中暂存或使用的一些数据（数据实体），譬如用户id 或 短效配置信息，可能存储在 Server Side 亦或是 Client Side

### Session-ID

由于 Session-Data未必会直接放在程序内部，所以在大部分 Server Side Session（Session-Data存储在服务端时），需要一个「索引」用来找到具体的 Data，这个索引就是 Session-ID，（在 Client Side Session 的实现中可能没有这个 ID 的索引概念）

### Server Side Session

在大部分实现中，并不会直接传输 Session-Data，而是传输它的索引：Session-ID，Server 程序收到 Session-ID 后，从存储着 Data 的地方取出具体的 Session-Data 来使用。
在这种模式下，更容易被我们接触到的，其实是存储在 Cookies 里的 Session-ID，而许多人存在的一个误区，便是将 Session-ID 直接等同于 Session 本身，无视了 Session-Data 的存在，这其实是不正确的。

### Client Side Session

在这种实现方式中，Server 不存储 Session-Data，而是直接将 Session-Data 存储在 Client（浏览器）的 Cookies 里。
在这种情况下，你甚至找不到 Session-ID 的存在
客户端直接告诉服务端，我是 Alice，我的基本信息是 xxx，于是服务端使用这些数据返回了相应的页面。
对于新用户，本地一丁点儿信息都没有，于是服务端返回了一个空的 Session-Data 用来初始化，在后续的通信中，这个 Session-Data 会被继续填充上有意义的数据。
很显然，这里存在着巨大的安全问题：我直接修改存储在本地的 Session-Data，声称我自己是管理员怎么办？
为此，Client Side Session 需要加入**加密机制**或**签名机制**来进行校验，以确保所有的 Session-Data 都是由服务端生成的

## Cookies

> 提到 Session 就不能不提 Cookies，毕竟很多人会条件反射的把这二者弄混 😅

Cookies 自身就有非常多的玩儿法，抛开那些权限相关的内容，此处我们先只它最基础的几个特性：

- 在客户端（浏览器）内存储一些数据（而不是在服务端）
- 这些信息，可以由服务端设置，也可以由客户端设置
- 当用户发起 HTTP 请求时，匹配的 Cookies 会嵌入请求头部（ Header ）一起发送
  正是这些特征，让 Cookies 成为存储 Session-Data / Session-ID 的绝佳场所，在几乎所有的常见实现中，均默认使用 Cookies 来存储 Session 相关信息。

但是需要注意，Session-Data / Session-ID 选择 Cookie 作为容器只是因为「方便」，但这**并不是必然情况**：

> 我们完全可以实现一个 Web 框架，它使用 LocalStorage 来存储 Session-Data / Session-ID，在发起 XHR 请求时，主动将其加进 Header 内（甚至 URL 内），服务端则从相应位置读取信息完成业务逻辑，在这套框架体系内这是完全没有问题的。

实际上，许多框架都支持 Session with out Cookies 的实现，虽然存在各种各样的小问题或限制，但是确实可用。
因此，需要再次强调：对于 Session 机制来说，Session-Data / Session-ID 才是本体，Cookies 只是一个**存储容器**，这二者**没有捆绑关系**。

## Authentication

- 登录相关，“验证”、“鉴权”，通过一定的手段完成对用户身份的确认
- 对应的 http status code：401 Unauthorized

## Authorization

- 权限相关，“授权”、“批准”，授予某项权利，批准某个行为
- 对应的 http status code：403 Forbidden

## Base64

> 本质是为了将二进制转成文本，以防止在某些文本协议中直接放二进制会破坏文本协议，比如 html 协议中直接放二进制，某些字段会组成某某标签导致解析异常，像邮件等文本协议都会有这种问题；

Base64 编码使用 6 个二进制位来表示一个字符，正好可以表示 64 个不同的字符，也是 Base64 编码名称的由来，这些字符包括：

- 26 个大写字母 A ~ Z
- 26 个小写字母 a ~ z
- 10 个数字 0 ~ 9
- 2 个特殊字符 `+` `/`
  编码步骤：
- 将编码对象转换为二进制（使用 ASCII 编码 8 位）字符串
- 把二进制的字符串按照每 6 位一组来分组，不足用 0 补齐
- 把每一组的二进制位转换为十进制数字，按照 Base64 编码表中转换为对应字符
- Base64 编码之后的位数需要是 4 的倍数，不足的结尾用 `=` 补齐
  最后，Base64 只是一种编码方式，并不提供数据的保密性，所有的数据都是以明文的形式存储的

## Base64URL

因为 Base64 中存在三个字符`+`、`/`和`=`，这些字符在 URL 里面有特殊含义，所以要被替换掉：`=`被省略、`+`替换成`-`，`/`替换成`_` ，这就是 Base64URL 算法。

## JWT 原理

服务器认证以后，生成一个 JSON 对象，发回给用户

```json
{
  "姓名": "张三",
  "角色": "管理员",
  "到期时间": "2018年7月1日0点0分"
}
```

用户与服务端通信的时候，都要发回这个 JSON 对象。服务器完全只靠这个对象认定用户身份。为了防止用户篡改数据，服务器在生成这个对象的时候，会加上签名

## JWT 数据结构

由三部分组成：
`Header.Payload.Signature`

### Header

是一个JSON对象，描述jwt的元数据

```json
{
  "alg": "HS256", // 签名算法，默认sha256（hs256）
  "typ": "JWT" // token 类型
}
```

### Payload

也是一个JSON对象，存放实际需要传递的数据，有 7 个官方字段，亦可以自定义字段

- iss (issuer)：签发人
- exp (expiration time)：过期时间
- sub (subject)：主题
- aud (audience)：受众
- nbf (Not Before)：生效时间
- iat (Issued At)：签发时间
- jti (JWT ID)：编号

### Signature

对前两部分的签名，防止数据篡改，需要指定一个密钥（secret），然后使用 Header 指定的签名算法按照一定的方式生成签名

```
HMACSHA256(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
  secret)
```

算出签名以后，把 Header、Payload、Signature 三个部分拼成一个字符串，每个部分之间用"点"（`.`）分隔，就可以返回给用户

## JWT 的特点

- JWT 默认是不加密，但也是可以加密的。生成原始 Token 以后，可以用密钥再加密一次。
- JWT 不加密的情况下，不能将秘密数据写入 JWT。
- JWT 不仅可以用于认证，也可以用于交换信息。有效使用 JWT，可以降低服务器查询数据库的次数。
- JWT 的最大缺点是，由于服务器不保存 session 状态，因此无法在使用过程中废止某个 token，或者更改 token 的权限。也就是说，一旦 JWT 签发了，在到期之前就会始终有效，除非服务器部署额外的逻辑。
- JWT 本身包含了认证信息，一旦泄露，任何人都可以获得该令牌的所有权限。为了减少盗用，JWT 的有效期应该设置得比较短。对于一些比较重要的权限，使用时应该再次对用户进行认证。
- 为了减少盗用，JWT 不应该使用 HTTP 协议明码传输，要使用 HTTPS 协议传输。

## Session 和 JWT 的关系是什么？

有一篇蛮有名的文章：[Stop using JWT for sessions](http://cryto.net/%7Ejoepie91/blog/2016/06/13/stop-using-jwt-for-sessions/) ,作者提到的那些将 JWT 用做 Session 实现的人，实际上说的都是 **Client Side Session**
那么问题变的比较清晰了：

- JWT 只是一种处理数据的手法，它通过签名保证了信息的不可篡改，特定的格式也具备其它一些小特性。
- JWT 的特性，让它具备成为 Client Side Session 的数据处理方式的潜力，也确实有人这么做了。
  而那些关于 JWT 与 Session 优劣的争论，实际上大部分都是在争论 Sever Side Session 和 Client Side Session 的优劣。