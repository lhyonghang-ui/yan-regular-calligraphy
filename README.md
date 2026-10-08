# 颜体楷书创作与评析 Skill

这是一个中文 Codex Skill，用于依据《颜勤礼碑》的笔法、结构和章法规律，完成颜体楷书分析、临帖指导、数字作品创作、质量检查和学习测试。

本仓库保存的是对42页学习资料的整理结果，不包含现代出版字帖的整套扫描图片。示例图片属于数字生成作品，不是颜真卿真迹，也不是实体毛笔原作。

## 主要能力

- 解释颜体点、横、竖、撇、捺、钩、折、提的用笔变化。
- 分析独体、上下、左右、左中右、包围和多体结构。
- 为指定文字规划主笔、重心、迎让、穿插、疏密和章法。
- 生成书法图像后检查错字、简繁体、结构和伪署名问题。
- 使用配套测试题检验读帖、迁移创作和评析能力。

## 文件结构

```text
yan-regular-calligraphy/
├── SKILL.md
├── agents/openai.yaml
├── references/
│   ├── yan-qinli-principles.md
│   ├── stroke-methods.md
│   ├── structure-methods.md
│   ├── creation-and-review.md
│   ├── evaluation-rubric.md
│   └── source-index.md
├── evals/
│   ├── test-prompts.md
│   ├── answer-key.md
│   └── trigger-cases.csv
├── assets/examples/厚德載物.png
└── LICENSE
```

## 安装方法

### 安装为个人 Skill

把整个 `yan-regular-calligraphy` 文件夹复制到：

```text
~/.codex/skills/yan-regular-calligraphy/
```

### 只在某个项目中使用

复制到项目目录：

```text
项目目录/.codex/skills/yan-regular-calligraphy/
```

安装后重新打开相应 Codex 对话或项目，让技能列表重新加载。

## 使用方法

明确调用：

```text
使用 $yan-regular-calligraphy，分析《颜勤礼碑》中“门”字左右竖画的关系。
```

```text
使用 $yan-regular-calligraphy，以颜体楷书规律创作“寿”字，并说明结构安排。
```

```text
使用 $yan-regular-calligraphy，为“厚德载物”设计一幅竖式书法作品，生成后逐字检查。
```

自然语言调用：

```text
请按《颜勤礼碑》的规律评析这幅楷书，重点看横轻竖重和左右迎让。
```

## 测试方法

1. 先使用 `evals/test-prompts.md` 的基础题和迁移题。
2. 用 `evals/answer-key.md` 检查关键点，不要求答案逐字一致。
3. 使用 `evals/trigger-cases.csv` 测试技能何时应该触发、何时不应该触发。
4. 对图像作品必须人工核对正文，不能只依赖自动文字识别。

## 内容与版权边界

- 参考知识来自本次对42张《颜勤礼碑》教学图片的逐页观察与归纳。
- 仓库不分发原扫描图，避免把来源不明或仍受版权保护的出版物重新公开传播。
- 如以后添加公版碑帖图片，应在文件旁注明来源、馆藏和授权状态。
- 本技能不能用于书画真伪鉴定，也不能替代书法教师的现场执笔指导。

## GitHub 发布前检查

- 确认不含原字帖扫描图、个人信息、密钥和临时文件。
- 运行技能校验并检查 ZIP 能正常解压。
- 由仓库所有者决定公开或私有后再上传。
