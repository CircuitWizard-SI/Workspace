---
name: minis-markdown-output
version: 1.0.0
description: Minis 聊天界面的通用 Markdown、代码、图片和文件输出规范。用于需要稳定显示代码、图片、音视频或工作文件链接的回答，以及发现附件链接、文件名编码或页面输出异常时。
---

# Minis 通用输出规范

本技能只负责通用 Markdown、代码、图片、音视频和文件链接；其它技能只负责各自领域的知识与任务流程。

## 通用 Markdown

- 根据内容选择清晰的标题、列表和段落结构。
- 代码只有在用户要求查看源码或需要保持原样时才放入代码围栏；代码围栏内保持原始缩进和字符。
- 不使用 HTML、不可见字符或手工空白制造版式间距。
- 附件、工作文件和网页资源优先使用可点击的 Minis 链接。

## 图片与文件

- 图片使用附件 Markdown：`![说明](minis://attachments/...)`。
- 工作文件使用链接：`[文件名](minis://workspace/...)`。
- 文件名含中文、空格或 emoji 时必须使用工具返回的已编码 minis_url，不手写未编码 URL。

## 最终自检

发送前检查 Markdown 结构、代码围栏、附件类型、链接路径和文件名编码是否完整；发现文件预览或链接风险时先修正输出，不要声称用户已经成功打开文件。

minis_url: minis://skills/minis-markdown-output/SKILL.md
