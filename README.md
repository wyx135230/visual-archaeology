# 🧭 Visual Archaeology 视觉考古

> 把一张参考图，逆向成"那位画师亲手画出来的 Prompt"。
> Not "describe what's in the image" — **become the artist who made it.**

你对着参考图只会写 `a beautiful colored pencil illustration of a girl...`？
这里教你另一条路：戴上放大镜，观察颜料与纤维的微观咬合，代入那位浑身沾满颜料的手工创作者，坐回工作台前，用**第一人称 + 物理手部动作**重建完整的创作流程，最终产出一条能 100% 锁死风格材质的生图 Prompt。

---

## ✨ 它解决什么问题

生图模型默认自带"数码塑料平滑感 / CG 空气刷 / 完美渐变网格"。
普通 Prompt 描述的是**旁观者看到的画面**，模型只能画出一张好看的数码图，画不出**媒介质感**。

Visual Archaeology 反向拆解的是：
- 作者用什么**基底**（熟绢 / 粗齿冷压纸 / 纯棉水彩纸 / 未涂布印刷纸）
- 用什么**物理工具与力道**（狼毫勾线笔悬腕铁线描 / 软性蜡质彩铅压感排线 / 墨辊压痕）
- 颜料与基底摩擦留下的**微观物理痕迹**（矿物微粒哑光绒面 / 纸齿跳白 / 水痕沉淀 / 网点孔径）
- 作者**主动舍弃了什么**、哪里**强制留白**

最终把"画面描述"变成"创作过程"，让模型看到**力与介质**，而不是像素。

---

## 🧬 核心方法论

```
参考图
  │
  ├─ ① 双重甄别：创作者原生特征 vs AI 伪特征（剥离）
  ├─ ② 创作源流判定：概念自发创作型 / 现实相片写生转译型
  ├─ ③ 空间视知觉范式锁定：纯 2D 扁平 / 2.5D 层叠 / 平面画意深度 / 3D 风格化
  ├─ ④ 意识接管：我不是识图工具，我就是这件作品的创作者
  ├─ ⑤ 三要素锁定：【物理工具】+【受体基底】+【微观物理反应】
  └─ ⑥ 12 阶段创作工作流重建 → 停笔判断
        │
        ▼
   产出 3 个版本 Prompt + Negative Prompt
```

输出固定包含：

| 版本 | 定位 | 适用模型 |
|---|---|---|
| **VERSION-A** | 完整意识接管与微观物理长文叙事 | FLUX / SD3 等高级语义模型 |
| **VERSION-B** | 高密度物理质感生产力版 | Midjourney v6 / SDXL |
| **VERSION-C** | 模块化可迁移创作者 DNA 模板（1:1 镜像克隆版） | 面向主题 / 主题定制复刻 |
| **Negative Prompt** | 针对该媒介天敌（数码 AI 伪特征）精准封杀 | 全部 |

---

## 🚀 快速上手（30 秒）

1. 把 skill 放进你的 skill 根目录（如 `.user_skills/visual-archaeology/`）。
2. 拿一张参考图（插画 / 海报 / 工笔重彩 / 彩铅 / 水彩 / 版画 / 拼贴 / 矢量…），作为输入。
3. 调用 `visual-archaeology`，让 AI 先做前置甄别，再输出完整逆向报告。
4. 把其中的 **VERSION-A / B / C** 与 **Negative Prompt** 直接投给对应生图模型。

### 一句话教程

```
输入：一张参考图
输出：① 视觉与物理媒介考古 → ② 作者意识重建 → ③ Visual DNA 视觉锁
     → ④ VERSION-A → ⑤ VERSION-B → ⑥ VERSION-C（镜像克隆）
     → ⑦ Negative Prompt → ⑧ 最高权重 5 条物理变量
```

> 💡 贴士：生图前把 Negative Prompt 焊进模型负向提示框，可彻底压制 `digital smooth / 3D CGI render / airbrush gradient` 等数码伪特征。

---

## 🎯 支持的画种

工笔重彩 · 古典矿物重彩 · 彩铅 / 铅笔 · 水彩 · 版画 / 复古印刷 · 海报 / 矢量平面 · 拼贴 / 混合媒介 · 素描 · 油画 · 复古招贴 · 数字混合媒介 · 抽象艺术

---

## 📦 安装

这是一份标准 `SKILL.md` 技能包，可挂载到任意支持 Agent Skill 的运行时：

- **Claude Code / Claude Skills**（`~/.claude/skills/`）
- **Codex CLI / OpenAI Agents**
- **Cursor / Windsurf 等 Agent 编辑器**
- 其他兼容 SKILL.md 规范的 Agent 运行时

目录结构：

```
visual-archaeology/
└── SKILL.md   ← 唯一入口，整个文件夹丢进 skills 目录即可
```

安装即生效，无需额外配置。

---

## 🧭 设计哲学

- **拒绝旁观者描述**：禁止 `Create an image of...`、`A beautiful illustration of...`
- **全程第一人称手部动作**：不是"画面里有什么"，而是"我的手如何操作材料"
- **抗数码平滑**：把 CG 塑料味当作敌人，用 `mineral pigment residue / paper tooth / waxy grain` 等高价值物理词武装 Prompt
- **镜像克隆法则**：VERSION-C 必须逐字继承 VERSION-A 的语言密度，绝不缩写偷懒

---

## ⚖️ License

MIT License

---