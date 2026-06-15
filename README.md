# Stop Slop 中文版

一个清理中文 AI 腔的 skill。

<img width="3840" height="2160" alt="G-Yg4RVbIAAhVxW" src="https://github.com/user-attachments/assets/902afc15-1f40-4a9d-af24-8cd67afb8ebf" />

## 这是什么

AI 写中文时常出现固定痕迹：铺垫套话、公式化结构、空泛判断、翻译腔、节奏整齐但没有细节。这个 skill 用来抓出这些问题，并把文本改得更具体、更直接。

## 文件结构

```
stop-slop/
├── SKILL.md              # 核心规则
├── references/
│   ├── phrases.md        # 需要删除或替换的中文短语
│   ├── structures.md     # 需要避开的中文结构
│   └── examples.md       # 修改前后示例
├── README.md
└── LICENSE
```

## 快速开始

**Codex 或 Claude Code：**把这个文件夹作为 skill 使用。

**Claude Projects：**上传 `SKILL.md` 和 `references/` 下的参考文件。

**自定义指令：**复制 `SKILL.md` 里的核心规则。

**API 调用：**把 `SKILL.md` 放进系统提示。需要细节时再加载 reference 文件。

## 它会抓什么

**套话短语**：开场铺垫、强调拐杖、商业黑话、没有事实功能的程度词、空泛判断、元评论。见 `references/phrases.md`。

**结构套路**：二元反转、否定铺垫、三段式口号、设问自答、虚假主体、远距离旁白、被动句。见 `references/structures.md`。

**句子层规则**：少用模板开头，不用破折号制造力度，避免连续短句口号，少用懒惰绝对词，优先主动句。

## 评分

每项 1 到 10 分：

| 维度 | 问题 |
|------|------|
| 直接 | 句子在说事，还是在宣布自己要说事？ |
| 节奏 | 长短有变化，还是像模板生成？ |
| 信任 | 是否尊重读者判断，还是过度解释？ |
| 真实 | 是否像具体的人写给具体的人？ |
| 密度 | 有没有能删掉而不损失信息的词句？ |

低于 35/50：继续改。

## 作者

基于 [Hardik Pandya](https://hvpandya.com) 的 Stop Slop 改写为中文语境。

## License

MIT。可自由使用和分享。
