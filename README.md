# 奇幻小说创作仓库 (My Story Workshop)

本仓库用于**中文奇幻小说（类似《诡秘之主》风格）**的创作、世界观构建与大纲章节管理。

仓库采用**顶级平行架构**，每一个一级目录对应一部独立的小说作品，或通用的总设定集。

---

## 顶级目录索引 (Workspace Index)

### 1. 通用总设定集
- **[`shared-settings/`](./shared-settings/)**：存储整个非凡宇宙的通用底层法则（三大守恒定律、失控与扮演法、神性与锚等）。

### 2. 小说作品库 (Novels)
- **[`book-01-whisper/`](./book-01-whisper/)**：《深渊低语》（示例首部小说，克苏鲁蒸汽朋克 + 序列魔药 + 悬疑解谜）。

---

## 规范文档与创作指南 (Rules)

- **[`AGENTS.md`](./AGENTS.md)**：项目级约束文件，包含奇幻写作十四条诫律。
- **[`.agents/rules/fantasy_novel_rules.md`](./.agents/rules/fantasy_novel_rules.md)**：诡秘风格小说详细创作与设定制订指南。

---

## 如何新建一部新小说？

1. 在仓库根目录新建一个一级目录（如 `book-02-xxx/`）。
2. 在该一级目录下建立标准脚手架：
   - `README.md`：本书索引
   - `settings/`：本书特有设定（途径、势力、人物、封印物）
   - `outlines/`：大纲（总大纲、分卷大纲）
   - `chapters/`：正文文本（按卷存储）
3. 在本 `README.md` 的“小说作品库”列表中添加索引项。