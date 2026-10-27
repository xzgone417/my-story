# 原创世界观与力量体系重建实施计划

> 历史计划，已被 2026-10-27 的“裂印”设定取代。当前规则见 [`book-01-whisper/settings/pathways.md`](../../../book-01-whisper/settings/pathways.md)。

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** 清空旧有仿写设定，并在原目录骨架上建立原创世界观总纲与原创力量体系。

**Architecture:** 以一个统一的超常底层机制支撑所有能力表现；宇宙层、社会层和力量层分别写入职责清晰的 Markdown 文件。人物、封印物和剧情大纲在本阶段只清空为重建状态，避免新旧设定混杂。

**Tech Stack:** Markdown、PowerShell、ripgrep、Git 工作区检查。

---

### Task 1: 清空旧设定并更新工作区索引

**Files:**
- Modify: `README.md`
- Modify: `shared-settings/README.md`
- Modify: `book-01-whisper/README.md`
- Modify: `book-01-whisper/settings/characters.md`
- Modify: `book-01-whisper/settings/artifacts.md`
- Modify: `book-01-whisper/outlines/master_outline.md`
- Modify: `book-01-whisper/outlines/volume_1.md`

- [x] **Step 1: 删除旧作品索引、人物、封印物和剧情正文内容**

  将上述文件改写为重建期索引或明确的空白工作区说明，不复制旧名称、人物、组织和情节。

- [x] **Step 2: 检查旧专有名词是否仍被正式文档引用**

  Run: `rg -n "序列9|序列0|魔药|扮演法|灰雾|塔罗会|圣恩斯|莱恩|星空议会" README.md shared-settings book-01-whisper`

  Expected: 只在迁移说明或设计规格中出现，不在新的正式设定中出现。

### Task 2: 重建宇宙与社会世界观

**Files:**
- Modify: `shared-settings/universe_laws.md`
- Modify: `book-01-whisper/settings/worldview.md`

- [x] **Step 1: 定义统一超常机制的来源、边界和历史原因**

  文档必须解释现实结构、超常现象重新可接触的原因、远古历史断层、高位存在的限制，以及超常使用留下的证据。

- [x] **Step 2: 定义当代时代、地理、社会秩序和五类阵营**

  时代容器必须支持城市案件、跨地区调查、信息传播和远古遗迹探索；不得复用罗兰帝邦、圣恩斯、第五纪或旧教会名称。

- [x] **Step 3: 建立神话真相的分层公开规则**

  明确哪些事实属于公众认知、调查者可知和深层真相，并为每层设置可复核的证据类型。

### Task 3: 重建原创力量体系

**Files:**
- Modify: `book-01-whisper/settings/pathways.md`

- [x] **Step 1: 选择并命名统一底层机制**

  从候选元素中只纳入能通过来源、接口、代价和证据检验的元素，并记录舍弃或改造其他元素的理由。

- [x] **Step 2: 定义四类权限变化和角色能力记录格式**

  使用感知、解析、介入、重构作为能力变化维度；每项能力必须有作用范围、触发条件、证据、失败后果和反制手段。

- [x] **Step 3: 定义成长、代价、失控和能力克制规则**

  成长不得采用固定序列或魔药晋升；代价必须具体、持续并可检测；系统必须列出不可做到的事情和至少三种克制关系。

### Task 4: 一致性验证

**Files:**
- Check: all Markdown files under `shared-settings/` and `book-01-whisper/`

- [x] **Step 1: 扫描旧设定残留**

  Run: `rg -n "序列|魔药|途径|扮演|灰雾|塔罗|圣恩斯|罗兰|绯红之月|极光会" shared-settings book-01-whisper`

  Expected: 新正式设定无命中；设计规格中的历史说明不参与正式设定验收。

- [x] **Step 2: 检查核心规则交叉一致**

  Run: `rg -n "来源|接口|感知|解析|介入|重构|代价|证据|阵营|历史" shared-settings/universe_laws.md book-01-whisper/settings/worldview.md book-01-whisper/settings/pathways.md`

  Expected: 三份核心文档均能找到相互对应的机制、历史、代价和证据说明。

- [x] **Step 3: 查看工作区差异并汇总重建结果**

  Run: `git diff --stat; git diff --check`

  Expected: 只包含本计划列出的文档变更，且无空白错误。
