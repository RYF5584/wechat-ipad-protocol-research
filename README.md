# wechat-ipad-protocol-research

![WeChat iPad Protocol](https://img.shields.io/badge/WeChat-iPad%20Protocol-07C160?style=flat-square)
![Type](https://img.shields.io/badge/Type-Public%20Research-1f6feb?style=flat-square)
![Docs](https://img.shields.io/badge/Docs-Continuous%20Update-f59e0b?style=flat-square)
![Last Commit](https://img.shields.io/github/last-commit/RYF5584/wechat-ipad-protocol-research?style=flat-square)

**交流学习联系**

**WeChat: `RSCompanyCEO`**

**Telegram: `ryf5584`**

**QQ: `1043695584`**

## 更新记录

> 以下为研究记录总览，按时间倒序排列（最新在最上面），点击标题可跳转至对应文档。

- [2026-06-15 - 视频号模块全链路功能](./docs/channels/2026-06-15%20-%20%E8%A7%86%E9%A2%91%E5%8F%B7%E6%A8%A1%E5%9D%97%E5%85%A8%E9%93%BE%E8%B7%AF%E5%8A%9F%E8%83%BD.md)
- [2026-06-10 - 短信登录新设备安全验证链路](./docs/login/security-verify/2026-06-10%20-%20%E7%9F%AD%E4%BF%A1%E7%99%BB%E5%BD%95%E6%96%B0%E8%AE%BE%E5%A4%87%E5%AE%89%E5%85%A8%E9%AA%8C%E8%AF%81%E9%93%BE%E8%B7%AF.md)
- [2026-06-02 - 新版微信死号A16强开](./docs/login/unban/2026-06-02%20-%20%E6%96%B0%E7%89%88%E5%BE%AE%E4%BF%A1%E6%AD%BB%E5%8F%B7%E5%BC%BA%E5%BC%80.md)
- [2026-05-24 - Mac 微信安全验证人工滑块方案与 UUID 研究](./docs/login/security-verify/2026-05-24%20-%20Mac%E5%BE%AE%E4%BF%A1%E5%AE%89%E5%85%A8%E9%AA%8C%E8%AF%81%E4%BA%BA%E5%B7%A5%E6%BB%91%E5%9D%97%E6%96%B9%E6%A1%88%E4%B8%8EUUID%E7%A0%94%E7%A9%B6.md)
- [2026-05-21 - 基础版 mmsf0001 生成接口](./docs/tools/mmsf0001/2026-05-21%20-%20%E5%9F%BA%E7%A1%80%E7%89%88mmsf0001%E7%94%9F%E6%88%90%E6%8E%A5%E5%8F%A3.md)

这个仓库主要用来展示微信 iPad 协议方向的研究进展。

这里不会把最关键的实现、源码、核心样本直接公开出去，但会把真正有价值的研究方向、已经做到的效果、能解决什么问题写清楚，让外部能看懂这不是空讲概念，而是已经做到了可继续联调、可继续落地方向的研究能力。

如果你正在找下面这些能力，这个仓库里的公开研究会更有参考价值：

- 微信 iPad 协议登录与扫码链路研究
- 微信 iPad 协议过验证方案评估
- 微信协议登录安全验证需要 UUID 的链路梳理
- Mac 微信、网页验证页、滑块、验证码、PIN 之间的承接研究
- 底层安全参数、证书材料、风险验证前置能力整理

这里更适合让外部快速看懂三件事：

- 这个方向到底卡在哪里
- 目前已经解决到了什么程度
- 是否值得继续做合作、联调或能力对接

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

## 对外合作价值

这个仓库的公开文档，重点不是讲抽象概念，而是帮助外部快速判断合作价值。

对于真正有需求的人，通常最关心的是：

- 某条微信 iPad 协议登录链路现在到底能不能跑
- 遇到安全验证时，是页面问题、参数问题，还是上下文问题
- `mmsf0001 / securityInfo / uuid` 这类能力目前能不能稳定承接
- 网页人工滑块、验证码、PIN 这种分支能不能真正接进后续流程
- 这项能力是停留在研究结论，还是已经能沉淀成可对接模块

所以这里的文档会尽量把“问题、思路、结果、价值”四件事讲清楚，方便外部判断是否继续深入合作。

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
docs/<研究模块>/<具体方向>/assets/<资源文件>
```

示例：

```text
docs/tools/mmsf0001/2026-05-21 - 基础版mmsf0001生成接口.md
docs/login/security-verify/2026-05-24 - Mac微信安全验证人工滑块方案与UUID研究.md
docs/login/security-verify/assets/微信协议模拟手动提交验证码页面.png
```

文档里的图片统一放在对应方向目录下的 `assets/` 里，不再和 Markdown 文件混放。
