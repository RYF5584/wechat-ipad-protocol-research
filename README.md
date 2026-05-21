# wechat-ipad-protocol-research

![WeChat iPad Protocol](https://img.shields.io/badge/WeChat-iPad%20Protocol-07C160?style=flat-square)
![Type](https://img.shields.io/badge/Type-Public%20Research-1f6feb?style=flat-square)
![Docs](https://img.shields.io/badge/Docs-Continuous%20Update-f59e0b?style=flat-square)

**交流学习联系**

**WeChat: `RSCompanyCEO`**

**Telegram: `ryf5584`**

**QQ: `1043695584`**

这个仓库主要用来展示微信 iPad 协议方向的研究进展。

这里不会把最关键的实现、源码、核心样本直接公开出去，但会把真正有价值的研究方向、已经做到的效果、能解决什么问题写清楚，让外部能看懂这不是空讲概念，而是已经做到了可继续联调、可继续落地方向的研究能力。

## 这个仓库主要写什么

这个仓库重点记录微信 iPad 协议里的关键问题，比如：

- 登录链路里卡在哪一步
- 风控验证为什么过不去
- 某个安全参数到底是干什么的
- 某个接口研究完以后，能解决什么实际问题
- 这一块能力在业务上能带来什么效果

这里的文档不会只写“研究了什么”，而是会尽量写清楚：

- 这个方向具体解决什么事
- 为什么微信 iPad 协议会卡在这里
- 研究这块的思路是什么
- 现在已经能做到什么程度
- 后面还能继续往哪推进

## 公开内容和不公开内容

这里会公开：

- 微信 iPad 协议研究思路
- 已经验证过的结果级结论
- 某项能力对应的实际用途
- 接口返回格式、调用结构、PB 方向这类公开示意
- 持续更新的研究文档索引

这里不会公开：

- 关键源码
- 可直接复现的细节步骤
- 核心参数明文
- 关键样本
- 可直接交付第三方复用的敏感结果

## 文档目录规则

所有研究文档统一放在 `docs/` 下，目录结构固定为：

```text
docs/<研究模块>/<具体方向>/YYYY-MM-DD - <研究主题>.md
```

示例：

```text
docs/tools/mmsf0001/2026-05-21 - 基础版mmsf0001生成接口.md
```

## 研究索引

- `tools / mmsf0001`
  - [2026-05-21 - 基础版 mmsf0001 生成接口](./docs/tools/mmsf0001/2026-05-21%20-%20%E5%9F%BA%E7%A1%80%E7%89%88mmsf0001%E7%94%9F%E6%88%90%E6%8E%A5%E5%8F%A3.md)
  - 说明：围绕微信 iPad 协议登录里的风险验证参数准备，解决验证码和 PIN 前后的安全参数衔接问题
