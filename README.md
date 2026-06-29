# 2026R语言期末大作业

本仓库整理的是本次课程作业中与我自己复现工作直接相关的代码、结果和报告。

## 目录说明

### 01_R_project

R 项目的主体目录。

- `emoreg_R_original_reproduction_and_bottomup_mcmc/`：核心项目目录
- `R/`：通用函数
- `scripts/`：主流程脚本
- `route_A_original_reproduction/`：Route A，按原文方法进行复现
- `route_B_bottomup_mcmc/`：Route B，自行扩展的自下而上 MCMC 分析路径
- `outputs/`、`logs/` 等：本次运行得到的结果文件和日志

说明：

- `01_R_project` 中保留了代码、结果和报告相关内容
- 原始数据和处理后数据未直接上传
- 数据来源链接见  
  `01_R_project/emoreg_R_original_reproduction_and_bottomup_mcmc/data/raw/SOURCE_DATA_LINKS.txt`

### 02_source_materials

原实验相关的数据、代码、图谱和外部资料来源说明。

本目录没有直接上传原始材料，而是按类别放置了对应的 `SOURCE_LINK.txt`，用于说明原始来源，例如：

- 论文链接
- NeuroVault 数据链接
- OSF 链接
- GitHub 原始代码仓库链接
- 相关脑图谱资源链接

### 03_paper_and_course_materials

论文与课程材料来源说明目录。

- 本目录未直接上传原文件
- 使用 `SOURCE_LINKS.txt` 说明论文来源和课程材料情况

### 04_复现报告与汇报ppt

本次作业最终提交材料。

- `复现报告.docx`：最终书面报告
- `汇报ppt.pptx`：汇报演示文稿

## 使用说明

如果要复现实验，主要查看 `01_R_project`。

- 看 Route A：进入 `route_A_original_reproduction/`
- 看 Route B：进入 `route_B_bottomup_mcmc/`
- 缺失的数据部分请先根据链接说明自行下载或按代码重新生成
