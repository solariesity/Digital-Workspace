# Personal File Organization Guide

个人文件整理指南（中文草案）

版本：v0.2  
更新时间：2026-06-02

## Overview

本文给出一套适用于个人长期使用的文件整理规范，重点面向以下场景：

- 课程学习
- 实验室事务
- 科研项目
- 通用开发
- 媒体素材与安装包管理

这份指南的目标不是建立复杂的层级，而是提供一套稳定、可执行、可扩展的目录与命名规则，使文件能够被快速归档、长期维护和可靠检索。

## Design Goals

- 让新文件能够快速归位
- 让同一项目的资料、代码、结果保持聚合
- 让重要文件在数月或数年后仍可检索
- 降低下载目录、聊天接收目录、临时副本带来的混乱

## Core Principles

### 1. Organize by purpose first

顶层目录优先按用途划分，而不是混合使用“年份、文件类型、软件名称、来源渠道”等多套标准。

### 2. Keep the top level stable

顶层目录应尽量保持长期稳定。细粒度分类应下沉到二级目录或项目目录内部，而不是频繁调整根目录结构。

### 3. Separate source, work, and output

对于科研、写作、数据处理、图像处理、代码开发等任务，建议至少区分以下三类内容：

- `Source` / `Raw`：原始资料或原始数据
- `Work` / `Processed`：处理中间文件
- `Output` / `Final`：最终交付结果

### 4. Treat downloads as an inbox

`Downloads` 只作为中转区使用，不作为长期存储位置。新文件应在固定周期内完成归档。

### 5. Make important directories self-explanatory

对于长期维护的项目、科研目录或数据目录，建议包含一个 `README.md`，用于说明用途、结构和命名规则。

## Recommended Top-Level Structure

推荐的顶层目录结构如下：

```text
D:\
  Archive\            # 归档区：旧项目、旧版本、历史资料
  Courses\            # 课程学习
  Dev\                # 通用开发、脚本、练习、小工具
  Docs\               # 个人正式资料、证件、简历、表格
  Downloads\          # 临时下载中转区
  Installers\         # 安装包、镜像、驱动、压缩包
  Lab\                # 实验室事务、组会、报销、共享材料
  Media\              # 图片、视频、音频、截图、模板、素材
  Research\           # 个人科研主线
  Systems\            # 软件运行相关目录
```

若存在较强的历史路径兼容需求，可将下列目录继续保留为物理目录，并在规范中统一视作 `Systems` 类内容：

```text
D:\Systems\
  AppData_Local\      # 聊天接收目录、同步缓存、软件工作区
  Programs\           # 新增绿色软件、便携工具
  software\           # 历史兼容目录
  VM\                 # 虚拟机、虚拟磁盘、系统镜像
```

## Directory Conventions

### `Courses`

建议按“学期 -> 课程”组织：

```text
D:\Courses\
  2026-Spring\
    Machine-Learning\
    Remote-Sensing-Image-Processing\
  2026-Fall\
```

单门课程内部可进一步划分：

- `Slides`
- `Notes`
- `Assignments`
- `Labs`
- `Exam`

### `Lab`

建议结构：

```text
D:\Lab\
  Admin\
  GroupMeeting\
  Reimbursement\
  Shared\
  Templates\
```

归类原则：

- 实验室安排、组会、报销、共享模板等事务性内容进入 `Lab`
- 与个人科研主线直接相关的内容不应长期混放在 `Lab`

### `Research`

建议结构：

```text
D:\Research\
  Papers\
  Notes\
  Projects\
  Data\
  Thesis\
```

归类原则：

- 文献库、阅读笔记、正式项目、论文写作应彼此分离
- 长期推进的课题优先按“项目目录”组织

### `Dev`

建议结构：

```text
D:\Dev\
  Learning\
  Sandbox\
  Scripts\
  Tools\
```

归类原则：

- 与科研无关的练习、通用脚本和个人工具进入 `Dev`
- 与具体科研项目强相关的代码应保留在 `Research` 对应项目中

### `Docs`

建议结构：

```text
D:\Docs\
  Certificates\
  Forms\
  Official\
  Personal\
```

### `Media`

建议结构：

```text
D:\Media\
  Assets\
  Audio\
  Images\
  Recordings\
  Screenshots\
  Templates\
  Videos\
```

归类原则：

- `Screenshots` 仅放截图
- `Recordings` 仅放录屏
- 可复用设计资源或参考素材进入 `Assets`

### `Installers`

建议结构：

```text
D:\Installers\
  CommonApps\
  DevTools\
  Drivers\
  Office\
  OS\
```

### `Archive`

建议结构：

```text
D:\Archive\
  2025\
  2026\
    Courses\
    Lab\
    Research\
```

归类原则：

- 仅归档已结束、已替代或不再活跃的内容
- 活跃项目不应提前移入 `Archive`

## Project Templates

相比按文件类型零散堆放，项目模板通常更适合长期维护。

### Generic Project Template

```text
Project_Name\
  README.md
  00_Inbox\
  01_Admin\
  02_Source\
  03_Work\
  04_Output\
  99_Archive\
```

适用范围：

- 小型开发项目
- 写作项目
- 课程大作业
- 周期为数周的综合任务

目录说明：

- `00_Inbox`：待整理输入
- `01_Admin`：说明文档、要求、计划、流程
- `02_Source`：原始资料、原图、原文、原始数据
- `03_Work`：中间稿、临时脚本、工作记录
- `04_Output`：最终交付件
- `99_Archive`：旧版本、废弃稿、历史副本

### Research Project Template

```text
Research_Project_Name\
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

适用范围：

- 科研课题
- 论文复现
- 数据分析项目
- 模型训练任务

关键规则：

- `raw` 保留原始输入，不直接修改
- 处理后数据写入 `processed`
- 图表、导出结果、最终材料统一写入 `06_Output`
- 文稿、汇报材料、附录内容统一写入 `05_Writing`

## Naming Conventions

命名一致性通常比继续细分目录更重要。

### Date Format

统一使用：

```text
YYYY-MM-DD
```

示例：

- `2026-06-02`
- `2026-03-18`

该格式具有以下优点：

- 支持自然排序
- 跨平台兼容性较好
- 适合长期维护

### File Name Patterns

推荐模式：

```text
YYYY-MM-DD_topic_v01.ext
project_content_YYYY-MM-DD.ext
course_task_YYYY-MM-DD.ext
```

示例：

- `2026-06-02_group-meeting_v01.pptx`
- `rs-detection_experiment-log_2026-05-28.md`
- `remote-sensing_hw1_2026-03-18.docx`

### Versioning

推荐版本写法：

- `v01`
- `v02`
- `v03`
- `final`

补充建议：

- 版本号建议补零，便于排序
- `final` 建议仅保留一个当前版本
- 历史版本移动至 `Archive` 或项目内 `99_Archive`

### Character Rules

应尽量避免：

- `\ / : * ? " < > |`
- 文件名首尾空格
- 过深目录与过长路径

补充建议：

- 同一层目录尽量统一中英文风格
- 文件夹命名避免无意义名称，如 `新建文件夹`、`杂项`、`临时`
- 若需同步到云盘，应提前控制路径深度与文件名长度

## README Template

对于重要目录，建议提供一个最小可维护的 `README.md`：

```md
# Project Name

## Purpose
This directory stores ...

## Structure
- 01_Literature: references
- 02_Data/raw: raw input
- 02_Data/processed: processed data
- 03_Code: source code
- 06_Output: final outputs

## Naming Rules
- Use YYYY-MM-DD for dates
- Use v01, v02, ... for versions

## Current Status
- Current phase / milestone
```

## Minimal Rules

如果只保留最核心的执行规则，可以压缩为以下 8 条：

1. 顶层目录只按用途划分，不混用多套分类标准。
2. `Courses`、`Lab`、`Research` 三条主线保持分离。
3. `Downloads` 仅作为中转区使用。
4. 每个持续性任务建立独立项目目录。
5. 项目内部至少区分 `Source`、`Work`、`Output`。
6. 原始数据不直接覆盖修改。
7. 日期统一使用 `YYYY-MM-DD`。
8. 旧版本统一进入 `Archive` 或 `99_Archive`。

## Reference Skeletons

### Top-Level Skeleton

```text
D:\
  Archive\
  Courses\
  Dev\
  Docs\
  Downloads\
  Installers\
  Lab\
  Media\
  Research\
  Systems\
    AppData_Local\
    Programs\
    software\
    VM\
```

### Research Project Skeleton

```text
Project_Name\
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

## Summary

一套有效的个人文件整理规范，重点不在于建立更多目录，而在于建立稳定的分类边界、统一的命名方式，以及可重复使用的项目模板。

对于课程、实验室和科研并行推进的场景，上述结构已经能够覆盖大多数长期管理需求。
