# cinematic-continuity-prompt

一个面向 Seedance、即梦、小云雀、MiniMax H3 等 AI 视频模型的高精度中文提示词 Skill。

它将视觉创意转译为可执行的导演调度，重点处理人物与场景连续性、动作因果、物理反馈、镜头运动、参考素材分工、对白同步、动态声音以及可验证的最终状态。

## 主要能力

- 无参考图、首帧、首尾帧、尾帧和多模态参考模式
- 参考图先行：先设计可动首帧，再依据实际生成图编写视频提示词
- 连续一镜到底、动作匹配分镜和复杂物理运动
- 手机原生实拍、第一人称 POV、人物微表演和成年克制亲密互动
- 对白口型、声线、距离、动作音与环境声的同步设计
- 参考图片、视频和音频的职责分配与冲突检查
- 导演版、可复制完整提示词和高风险稳定重试版
- 提示词审查、生成失败定位与减负重构

## 安装

### 使用 Skills CLI

```bash
npx skills add https://github.com/shaoye0219-svg/cinematic-continuity-prompt
```

### 手动安装

将仓库克隆到 Codex 的 skills 目录：

```powershell
git clone https://github.com/shaoye0219-svg/cinematic-continuity-prompt.git "$env:USERPROFILE\.codex\skills\cinematic-continuity-prompt"
```

## 使用方式

在请求中明确调用：

```text
使用 cinematic-continuity-prompt，帮我把这段剧情写成一份尽可能详细的10秒AI视频提示词。
```

也可以用于审查现有提示词：

```text
使用 cinematic-continuity-prompt，检查这份提示词中的人物连续性、运镜冲突、动作因果和生成风险，并给出完整重写版。
```

## 默认输出

1. 简洁导演判断
2. 一份完整、可直接复制的中文提示词
3. 仅在高风险镜头中提供稳定重试版

## 目录

```text
cinematic-continuity-prompt/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── exemplar-library.md
    ├── method-comparison.md
    ├── precision-writing-guide.md
    ├── prompt-framework.md
    └── regression-suite.md
```

## 方法来源

本 Skill 综合了静态画面要素设计、连续动作与物理反馈方法，以及 MiniMax H3 官方提示词指南中关于输入模式、关键帧连接、参考素材职责、运镜和音画时间线的可泛化原则。

平台专属格式不会被强制用于其他模型。详细的采用与取舍记录在 [`references/method-comparison.md`](references/method-comparison.md)。

## License

[MIT](LICENSE)
