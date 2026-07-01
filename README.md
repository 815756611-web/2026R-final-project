# 2026R语言期末大作业

本仓库包含本次课程作业中与我自己复现工作直接相关的代码、结果和报告。

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

本目录中：

- `00_paper_and_metadata/paper.pdf` 为论文原文
- 其他原始数据与外部材料因 GitHub 空间限制未直接上传
- 其余子目录使用 `SOURCE_LINK.txt` 提供原始数据或代码来源链接

### 03_复现报告与汇报ppt

本次作业最终提交材料。

- `复现报告.docx`：最终书面报告
- `汇报ppt.pptx`：汇报演示文稿

## 使用说明

如果要复现实验，主要查看 `01_R_project`。

- 看 Route A：进入 `route_A_original_reproduction/`
- 看 Route B：进入 `route_B_bottomup_mcmc/`
- 缺失的数据部分请先根据链接说明自行下载或按代码重新生成
