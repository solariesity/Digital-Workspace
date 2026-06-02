# Personal File Organization Guide

个人文件整理指南

[![Version](https://img.shields.io/badge/version-v1.0-blue)](./)
[![Status](https://img.shields.io/badge/status-active-brightgreen)](./)

一份适用于个人长期使用的文件整理规范，覆盖课程学习、实验室事务、科研项目、通用开发和媒体素材管理等场景。

> A personal file organization standard covering coursework, lab affairs, research projects, general development, and media asset management.

---

## 目录

- [1. 设计目标](#1-设计目标)
- [2. 核心原则](#2-核心原则)
- [3. 顶层目录结构](#3-顶层目录结构)
- [4. 各目录规范](#4-各目录规范)
  - [4.1 Courses（课程）](#41-courses课程)
  - [4.2 Lab（实验室）](#42-lab实验室)
  - [4.3 Research（科研）](#43-research科研)
  - [4.4 Dev（开发）](#44-dev开发)
  - [4.5 Docs（文档）](#45-docs文档)
  - [4.6 Media（媒体）](#46-media媒体)
  - [4.7 Installers（安装包）](#47-installers安装包)
  - [4.8 Archive（归档）](#48-archive归档)
  - [4.9 Systems（系统）](#49-systems系统)
  - [4.10 Downloads（下载中转）](#410-downloads下载中转)
- [5. 项目模板](#5-项目模板)
  - [5.1 通用项目模板](#51-通用项目模板)
  - [5.2 科研项目模板](#52-科研项目模板)
- [6. 命名规范](#6-命名规范)
- [7. README 模板](#7-readme-模板)
- [8. 版本管理](#8-版本管理)
- [9. 文件生命周期](#9-文件生命周期)
- [10. 最小规则（速查）](#10-最小规则速查)
- [11. 参考骨架](#11-参考骨架)
- [12. 补充建议](#12-补充建议)

---

## 1. 设计目标

| 目标 | 说明 |
|------|------|
| **快速归位** | 新文件能在 30 秒内决定存放位置 |
| **保持聚合** | 同一项目的资料、代码、结果集中存放，不零散分布 |
| **长期可检索** | 重要文件在数月或数年后仍可通过名称或目录定位 |
| **减少混乱源** | 降低下载目录、聊天接收目录、临时副本带来的熵增 |

---

## 2. 核心原则

### 原则 1：按用途优先划分

顶层目录统一按**用途**划分。避免混用"年份 + 文件类型 + 软件名称 + 来源渠道"等多套分类标准。

### 原则 2：顶层保持稳定

顶层目录长期不变。细粒度分类下沉到二级目录或项目目录内部，不频繁调整根目录结构。

### 原则 3：分离来源、过程和结果

对于科研、写作、数据处理、代码开发等任务，至少区分以下三类：

| 分类 | 含义 | 示例 |
|------|------|------|
| **Source** / Raw | 原始资料或原始数据 | 下载的论文 PDF、实验原始数据 |
| **Work** / Processed | 处理中间文件 | 清洗后的数据、草稿、临时脚本 |
| **Output** / Final | 最终交付结果 | 导出的图表、提交的论文、发布的代码 |

> 核心规则：**原始数据不直接覆盖修改。** 始终保留一份未修改的原始副本。

### 原则 4：下载目录仅为中转区

`Downloads` 不作为长期存储位置。新文件应在固定周期内（建议每周）完成归档。

### 原则 5：重要目录自描述

长期维护的项目、科研或数据目录应包含一个 `README.md`，说明用途、结构和命名规则。

---

## 3. 顶层目录结构

```
D:\
  Archive\        # 归档区：旧项目、旧版本、历史资料
  Courses\        # 课程学习
  Dev\            # 通用开发、脚本、练习、小工具
  Docs\           # 个人正式资料、证件、简历、表格
  Downloads\      # 临时下载中转区（仅作中转，不长期存放）
  Installers\     # 安装包、镜像、驱动、压缩包
  Lab\            # 实验室事务、组会、报销、共享材料
  Media\          # 图片、视频、音频、截图、模板、素材
  Research\       # 个人科研主线
  Systems\        # 软件运行环境相关
```

> 顶层目录不超过 **10 个**，保持一目了然。

---

## 4. 各目录规范

### 4.1 Courses（课程）

按 **学期 → 课程** 两级组织：

```
D:\Courses\
  2026-Spring\
    Machine-Learning\
    Remote-Sensing-Image-Processing\
  2026-Fall\
```

单门课程内部建议划分：

```
Course-Name\
  Slides\         # 课件
  Notes\          # 笔记
  Assignments\    # 作业
  Labs\           # 实验
  Exam\           # 考试相关
```

---

### 4.2 Lab（实验室）

```
D:\Lab\
  Admin\          # 行政事务
  GroupMeeting\   # 组会材料
  Reimbursement\  # 报销单据
  Shared\         # 共享材料
  Templates\      # 模板文件
```

> 与个人科研主线直接相关的内容不应长期混放在 `Lab`，而应归入 `Research` 对应项目。

---

### 4.3 Research（科研）

```
D:\Research\
  Papers\         # 文献库（PDF + 笔记）
  Notes\          # 阅读笔记、想法、备忘
  Projects\       # 正式课题（每个课题一个项目目录）
  Data\           # 跨项目共享的数据集
  Thesis\         # 学位论文
```

每个课题目按[科研项目模板](#52-科研项目模板)组织。

---

### 4.4 Dev（开发）

```
D:\Dev\
  Learning\       # 学习路径（教程、练习）
  Sandbox\        # 临时实验、原型
  Scripts\        # 通用脚本
  Tools\          # 自用小工具
```

> 与具体科研项目强相关的代码应保留在 `Research/Projects/<Project>/03_Code`。

---

### 4.5 Docs（文档）

```
D:\Docs\
  Certificates\   # 证书、奖状扫描件
  Forms\          # 常用表格
  Official\       # 官方文件（证明、合同）
  Personal\       # 个人文档（简历、求职材料）
```

---

### 4.6 Media（媒体）

```
D:\Media\
  Assets\         # 可复用设计资源、参考素材
  Audio\          # 音频
  Images\         # 图片
  Recordings\     # 录屏
  Screenshots\    # 截图
  Templates\      # 设计模板
  Videos\         # 视频
```

> `Screenshots` 和 `Recordings` 应定期清理——截图通常在分享后即可删除，有价值者归档到对应项目。

---

### 4.7 Installers（安装包）

```
D:\Installers\
  CommonApps\     # 常用软件（浏览器、压缩工具等）
  DevTools\       # 开发工具（IDE、Git、数据库工具）
  Drivers\        # 驱动
  Office\         # 办公软件
  OS\             # 操作系统镜像
```

> 安装完成后，若安装包可在官网随时获取，建议直接删除而非囤积。

---

### 4.8 Archive（归档）

```
D:\Archive\
  2025\
    Courses\
    Lab\
    Research\
  2026\
    Courses\
    Lab\
    Research\
```

归档条件（满足其一即可归档）：

- 项目已完结且短期内不会重启
- 课程成绩已出且资料不再参考
- 文件已被新版本完全替代
- 超过 12 个月未访问

> 活跃项目不应提前移入 `Archive`。

---

### 4.9 Systems（系统）

```
D:\Systems\
  AppData_Local\  # 聊天软件接收目录、同步工具缓存、软件工作区
  Programs       # 软件安装目录、绿色软件、便携工具
  VM\             # 虚拟机文件、虚拟磁盘、系统镜像
```

---

### 4.10 Downloads（下载中转）

`Downloads` 是唯一的**临时区域**。建议习惯：

- 每周归档一次，将文件移入对应目录
- 下载后已安装的安装包 → 确认不需要保留则直接删除
- 聊天接收的临时文件 → 归档或删除，不在 Downloads 长期滞留

---

## 5. 项目模板

### 5.1 通用项目模板

```
Project-Name\
  README.md
  00_Inbox\       # 待整理输入
  01_Admin\       # 说明文档、要求、计划、流程
  02_Source\      # 原始资料、原图、原文、原始数据
  03_Work\        # 中间稿、临时脚本、工作记录
  04_Output\      # 最终交付件
  99_Archive\     # 旧版本、废弃稿、历史副本
```

适用范围：小型开发项目、写作项目、课程大作业、周期为数周的综合任务。

### 5.2 科研项目模板

```
Research-Project-Name\
  README.md
  01_Literature\  # 参考文献、相关论文
  02_Data\
    raw\          # 原始输入（不可修改）
    processed\    # 处理后的数据
  03_Code\        # 源代码
  04_Experiments\ # 实验记录、日志、超参数记录
  05_Writing\     # 文稿、汇报材料、附录
  06_Output\      # 图表、导出结果、最终材料
  99_Archive\     # 旧版本、废弃稿
```

适用范围：科研课题、论文复现、数据分析项目、模型训练任务。

---

## 6. 命名规范

### 日期格式

统一使用 `YYYY-MM-DD`：

```
2026-06-03
2026-03-18
```

优点：自然排序、跨平台兼容、无歧义（`06-03` vs `03-06`）。

### 文件名模式

```
<日期>_<主题>_<版本>.ext
<项目>_<内容>_<日期>.ext
<课程>_<任务>_<日期>.ext
```

示例：

```
2026-06-02_group-meeting_v01.pptx
rs-detection_experiment-log_2026-05-28.md
remote-sensing_hw1_2026-03-18.docx
```

### 版本号

格式：`v01`、`v02`、…、`final`

| 标记 | 使用场景 |
|------|----------|
| `v01` ~ `v0N` | 工作过程中的迭代版本 |
| `draft` | 初稿，结构和内容仍在调整 |
| `final` | 已交付/提交的最终版本（仅保留一个） |
| `final_v02` | 已交付后又做了修订（尽量少用） |

> 版本升级时机：**内容有实质性变更时升号**（如章节调整、数据更新、重新排版），仅改了一个标点或微调格式不升号。

### 字符限制

**禁止使用：**
- Windows 保留字符：`\ / : * ? " < > |`
- 文件名首尾空格

**建议遵守：**
- 同层目录统一中/英文风格，避免混搭
- 避免无意义名称：`新建文件夹`、`杂项`、`临时`、`test`
- 若需同步云盘，控制路径深度不超过 5 层，全路径不超过 260 字符

---

## 7. README 模板

重要目录应包含一个最小可维护的 `README.md`：

```markdown
# Project Name

## 用途 / Purpose

本目录用于存放 XXX 项目的全部资料和代码。

## 结构 / Structure

- `01_Literature/` — 参考文献
- `02_Data/raw/` — 原始数据（不可修改）
- `02_Data/processed/` — 处理后的数据
- `03_Code/` — 源代码
- `04_Experiments/` — 实验记录
- `05_Writing/` — 论文文稿
- `06_Output/` — 最终输出
- `99_Archive/` — 历史版本

## 命名规则 / Naming

- 日期格式：`YYYY-MM-DD`
- 版本格式：`v01`、`v02`、…、`final`

## 当前状态 / Status

- 阶段：实验阶段（2026-06）
- 下次节点：提交初稿（2026-07-15）
```

---

## 8. 版本管理

### 日常版本

在文件名中标注版本号，历史版本移入 `99_Archive/`：

```
proposal_v01.md
proposal_v02.md
proposal_final.md
99_Archive\
  proposal_v01.md
  proposal_v02.md
```

### Git 项目

代码类项目优先使用 Git 管理版本，不在文件名中加版本号。文件名回退到：

```
experiment-log_2026-05-28.md
```

### 关键节点备份

对于学位论文、重要报告等不可恢复的文件，建议在关键节点手动备份一份到 `99_Archive/`：

```
Thesis\
  05_Writing\
    thesis_ch3_2026-06-03.docx
  99_Archive\
    thesis_ch3_review-submitted_2026-05-20.docx
```

---

## 9. 文件生命周期

每个文件最终会进入以下四种状态之一：

```
创建 → 使用中 → [归档 | 保留 | 删除]
```

**删除判断标准：**

| 可以删除 | 不能删除 |
|----------|----------|
| 临时截图（已发送/已使用） | 有签名/盖章的正式文件 |
| 安装完成后即可重新下载的安装包 | 实验原始数据 |
| 已被 `final` 替代的中间草稿（无参考价值） | 合同、证书扫描件 |
| 聊天软件自动缓存的图片 | 已提交的作业和论文 |
| 重复的副本（确认内容一致） | 未备份的创作类文件 |

> 不确定时，先移入 `Archive`，6 个月后再决定。

---

## 10. 最小规则（速查）

如果只保留最核心的 8 条：

1. 顶层目录只按**用途**划分，不混用多套分类标准。
2. `Courses`、`Lab`、`Research` 三条主线保持分离。
3. `Downloads` 仅作为中转区，**每周归档一次**。
4. 每个持续性任务建立**独立项目目录**。
5. 项目内部至少区分 **Source → Work → Output**。
6. **原始数据不直接覆盖修改**。
7. 日期统一使用 `YYYY-MM-DD`。
8. 旧版本统一进入 `Archive` 或 `99_Archive`。

---

## 11. 参考骨架

### 顶层骨架

```
D:\
  Archive\
    2025\
    2026\
  Courses\
    2026-Spring\
    2026-Fall\
  Dev\
    Learning\
    Sandbox\
    Scripts\
    Tools\
  Docs\
    Certificates\
    Forms\
    Official\
    Personal\
  Downloads\          # 仅中转
  Installers\
    CommonApps\
    DevTools\
    Drivers\
    Office\
    OS\
  Lab\
    Admin\
    GroupMeeting\
    Reimbursement\
    Shared\
    Templates\
  Media\
    Assets\
    Audio\
    Images\
    Recordings\
    Screenshots\
    Templates\
    Videos\
  Research\
    Papers\
    Notes\
    Projects\
    Data\
    Thesis\
  Systems\
    AppData_Local\
    Programs\
    VM\
```

### 科研项目骨架

```
Project-Name\
  README.md
  01_Literature\
  02_Data\
    raw\
    processed\
  03_Code\
  04_Experiments\
  05_Writing\
  06_Output\
  99_Archive\
```

---

## 12. 补充建议

- **先建骨架再使用。** 花 15 分钟把顶层目录和模板目录建好，后续文件归位会快很多。
- **不要过度设计。** 如果某个目录长期只有 1-2 个文件，不需要再建子目录。
- **定期维护。** 建议每学期末做一次 Archive 清理，把已完结的内容移出活跃区。
- **README 不用一次写完。** 新建项目时先写一句用途，后续逐步补充结构说明。
- **工具辅助。** 可配合 [Everything](https://www.voidtools.com/)（Windows 文件搜索）或 [Listary](https://www.listary.com/) 快速定位文件，降低对目录层级深度的依赖。

---

*最后更新：2026-06-03*
