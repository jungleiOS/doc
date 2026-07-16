# 微信吃瓜热点文_案例素材_AI代码窃密事件_核验报告

核验时间：2026-07-13

## 结论摘要

这份素材不能整体按“事实已证实”使用。

可保留的主线是：

> 苹果已起诉 OpenAI，诉称 OpenAI 及两名前苹果员工 Tang Tan、Chang Liu 涉嫌窃取或不当使用苹果硬件商业机密。

必须降级或删除的主线是：

> Grok CLI 静默打包上传整个代码库、上传 `~/.claude.json`、上传 AGENTS/Skills、服务端暗改开关。

截至本次检索，未找到可靠公开报道、官方说明、独立技术报告或可复现证据支撑这组 Grok CLI 细节。

---

## 逐条核验

| 素材断言 | 核验状态 | 处理建议 |
|---|---|---|
| 2026-07-10 苹果起诉 OpenAI | 基本属实 | 可写，但必须写成“苹果起诉/诉称/指控” |
| 被告包括 OpenAI、Tang Tan、Chang Liu、io Products | 基本属实 | 可保留 |
| Tang Tan 是前苹果高管，现在负责 OpenAI 硬件 | 基本属实 | 可保留 |
| Chang Liu 离职后仍访问苹果系统/保留苹果设备 | 有诉状和媒体报道支撑 | 写成“苹果称/诉称” |
| 面试时要求苹果候选人携带实际零部件/设计资料 | 有诉状和媒体报道支撑 | 写成“苹果称/诉称” |
| OpenAI 使用苹果供应链/制造工艺信息 | 有诉状和媒体报道支撑 | 写成“苹果指控”，不要写成既定事实 |
| “OpenAI 硬件业务从根上就烂了” | 有报道引用诉状类似表述 | 可作为“诉状措辞”引用或转述 |
| “400+ 前苹果员工在 OpenAI” | 有 The Verge 报道称苹果如此主张 | 写成“苹果称” |
| Chang Liu 下载“超1000页机密文件” | 未核到 | 建议改成“下载多份/数十份机密硬件文件” |
| 马斯克称 Altman “Scam Altman” | 有报道支撑 | 可保留 |
| 马斯克暗示 Altman “该进监狱” | 未核到 | 删除或改成“继续攻击其涉嫌欺骗” |
| Grok CLI 自动打包整个工作目录上传 tar.gz | 未核到可靠来源 | 删除，除非补充原始逆向报告/抓包证据 |
| Grok CLI 上传两个快照、会话状态、配置和日志 | 未核到可靠来源 | 删除 |
| Grok CLI 扫描 `~/.claude.json`、AGENTS、30 多个 Skill 文件 | 未核到可靠来源 | 删除 |
| Grok CLI 曝光后服务端远程切开关，客户端未更新 | 未核到可靠来源 | 删除 |
| Claude Code 2.1.91-2.1.196 被中国漏洞库/媒体指存在后门风险 | 有多家媒体报道，但官方原文未检到 | 可写成“据媒体援引中国漏洞库警示” |
| Claude Code/Codex/Gemini “仅发送实际打开文件” | 未逐项核到官方支撑 | 不建议绝对化；改成“没有公开证据显示它们存在 Grok 式全量上传行为” |

---

## 可引用来源

1. AP News：报道苹果于 2026-07-10 起诉 OpenAI，并列出 Tang Tan、Chang Liu、诉状核心指控和 OpenAI 否认。
   链接：https://apnews.com/article/apple-openai-lawsuit-trade-secrets-theft-6fff8833f5889d86406b89a02dd8fb16

2. The Verge：报道苹果诉状中关于 Chang Liu 下载“dozens of confidential hardware-related files”、Tang Tan 要求候选人带“CAD/design artifacts”“prototypes”、400+ 前苹果员工等细节。
   链接：https://www.theverge.com/tech/964350/apple-openai-lawsuit-trade-secrets

3. Business Insider：梳理苹果诉状中的主要爆点，包括安全 bug、面试收集信息、OpenAI 领导层被指参与等。
   链接：https://www.businessinsider.com/apple-sues-openai-trade-secret-theft-2026-7

4. Times of India：报道马斯克在 X 上称 Sam Altman 为 “Scam Altman”，并称其 “takes scamming to a whole new level”。
   链接：https://timesofindia.indiatimes.com/technology/tech-news/elon-musk-responds-to-apple-accusing-openai-of-stealing-trade-secrets-says-sam-altman-takes-scamming-to-a-whole-new-/articleshow/132340808.cms

5. Tom's Hardware：报道中国 National Vulnerability Database 对 Claude Code 的安全警示，并提到版本区间、敏感信息、Anthropic 工程师对反滥用实验的解释。
   链接：https://www.tomshardware.com/tech-industry/artificial-intelligence/china-alleges-that-claude-code-contains-backdoors-calls-mechanism-a-serious-threat-govt-claims-claude-sends-sensitive-information-to-remote-servers-without-consent

6. TechRadar：报道 Claude Code 被中国方面指存在后门风险，提到 2.1.91 到 2.1.196 版本区间和 Alibaba 禁用背景。
   链接：https://www.techradar.com/pro/china-warns-users-of-alleged-security-backdoor-vulnerabilities-in-anthropics-claude-code-tells-users-to-uninstall-for-sfaety-reasons

---

## 建议改稿口径

### 标题建议降风险

原口径：

> 你的代码正在被AI偷走

建议：

> AI编程工具信任危机：苹果起诉OpenAI，开发者该重新检查本地权限了

或者保留吃瓜感，但降低事实风险：

> 72小时，AI编程工具的信任底线被连续拷问

### 苹果段落

可用：

> 7月10日，苹果在加州联邦法院起诉 OpenAI、io Products，以及两名前苹果员工 Tang Tan、Chang Liu。苹果诉称，OpenAI 在硬件业务上不当获取并使用苹果商业机密。

不要写：

> OpenAI 偷了苹果机密。

除非全文明确这是“苹果的指控”，否则容易把未判决指控写成既定事实。

### 马斯克段落

可用：

> 马斯克随后在 X 上继续攻击 Sam Altman，称其为 “Scam Altman”，并说他把“诈骗”提升到了新高度。

不要写：

> 马斯克暗示奥特曼该进监狱。

本次未核到这个说法。

### Grok CLI 段落

建议整段删除，或降级成待核线索：

> 另有社媒传言称某些 AI CLI 工具存在静默上传代码库的风险，但截至本文检索，尚未找到可靠公开证据。真正可确定的是：AI Agent 一旦拥有本地文件权限，风险边界必须被重新审视。

不要写：

> Grok CLI 静默上传整个代码库。

当前没有可靠来源支撑。

### Claude Code 段落

可用：

> 多家媒体报道，中国漏洞库曾警示 Claude Code 2.1.91 至 2.1.196 存在可上传敏感信息的监控机制风险；相关说法仍有争议，Anthropic 方面将其解释为反滥用实验。

不要写：

> 工信部通报 Claude Code 存在安全后门。

更稳妥写法是“媒体援引中国国家漏洞库/CNVD 警示”。本次未直接检到官方原文。

---

## 最终建议

这篇稿子如果继续发，建议从“三瓜合一”改成“两条已核主线 + 一条风险提醒”：

1. 已核主线一：苹果起诉 OpenAI，指控商业机密被窃取。
2. 已核主线二：Claude Code 安全争议和中国漏洞库警示。
3. 风险提醒：AI Agent 本地文件权限过大，企业和个人都应检查授权、密钥和敏感目录。

不要把 Grok CLI 作为核心爆点，除非能补到原始逆向报告、抓包截图、xAI 客户端版本信息、二进制哈希、上传域名和可复现实验步骤。
