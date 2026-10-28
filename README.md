# 基础模型驱动的三维空间智能与具身决策综述配套资源库

**Resources for A Survey of Foundation Model-driven 3D Spatial Intelligence and Embodied Decision-making**

## Overview / 项目简介

本资源库配套综述《基础模型驱动的三维空间智能与具身决策综述》，按论文四层研究框架整理代表性方法、数据集与评测基准、评价指标，帮助读者查找论文、官方代码和数据访问入口。

收录范围以论文修订稿的正文、参考文献及15张表为依据。资源库提供分类索引，不含原始数据集、模型权重或实验结果数据库。仅作为依赖出现的通用二维模型不逐一列入方法表；Uni3D等被实际讨论的三维表征模型保留，并在Task中说明作用。表格中的比较基线同样保留并明确标记。

本地整理版本：**v1.0.0**。整理及链接核查日期：**2026-10-28**。首版包含 **92种方法、24项数据资源、29项评价指标**。GitHub及ScienceDB的远程发布尚待作者完成，本页不预设其访问地址。

完整索引：[methods.csv](methods.csv) · [datasets.csv](datasets.csv) · [metrics.csv](metrics.csv)

## Taxonomy / 分类框架

| Category | 研究内容 | 方法数 |
| --- | --- | ---: |
| 3D Perception | 三维表征、开放词汇分类、语义与实例分割、目标检测 | 23 |
| Language-driven 3D Understanding | 语言定位、问答、空间推理、场景图与相关生成任务 | 35 |
| World Models and Dynamic Prediction | 当前占用估计及其预测基础、未来状态预测、条件场景生成与预测规划接口 | 17 |
| Embodied Decision and Interaction | 导航、任务规划、机器人操作与环境交互 | 17 |

四层框架表示能力关联，并非所有系统都必须执行的固定流水线。每种方法按综述主要讨论位置归入一个Category；多个任务以分号写入Task。当前状态估计不等于未来状态预测，轨迹规划也不自动等于未来环境状态建模。

## Methods / 代表性算法

以下为各类节选，完整清单见[methods.csv](methods.csv)。Year优先采用所链接的正式出版记录年份；仅确认预印本时使用预印本年份。CoRL工作按PMLR书目年份记录，可能与会议举办年份不同。Code为空表示本次未确认可用的官方代码入口，不等于断言该方法没有实现。


### 3D Perception / 三维感知

| Method | Year | Task | Paper | Code |
| --- | ---: | --- | --- | --- |
| Uni3D | 2024 | 3D Representation Learning (3D Backbone) | [Paper](https://proceedings.iclr.cc/paper_files/paper/2024/hash/cc2c03ce028a1d6cbed6f98cede7f5a9-Abstract-Conference.html) | [Code](https://github.com/baaivision/Uni3D) |
| ULIP | 2023 | 3D Representation Learning; Zero-shot 3D Object Classification | [Paper](https://openaccess.thecvf.com/content/CVPR2023/html/Gao_ULIP_Learning_a_Unified_Representation_of_Language_Images_and_Point_CVPR_2023_paper.html) | [Code](https://github.com/salesforce/ULIP) |
| OpenScene | 2023 | Open-vocabulary 3D Semantic Segmentation | [Paper](https://openaccess.thecvf.com/content/CVPR2023/html/Peng_OpenScene_3D_Scene_Understanding_With_Open_Vocabularies_CVPR_2023_paper.html) | [Code](https://github.com/pengsongyou/openscene) |
| OpenMask3D | 2023 | Open-vocabulary 3D Instance Segmentation | [Paper](https://proceedings.neurips.cc/paper_files/paper/2023/hash/d77b5482e38339a8068791d939126be2-Abstract-Conference.html) | [Code](https://github.com/OpenMask3D/openmask3d) |
| Open3DIS | 2024 | Open-vocabulary 3D Instance Segmentation | [Paper](https://openaccess.thecvf.com/content/CVPR2024/html/Nguyen_Open3DIS_Open-Vocabulary_3D_Instance_Segmentation_with_2D_Mask_Guidance_CVPR_2024_paper.html) | [Code](https://github.com/VinAIResearch/Open3DIS) |
| CoDA | 2023 | Open-vocabulary 3D Object Detection | [Paper](https://papers.nips.cc/paper_files/paper/2023/file/e352b765e625934ce86919995e2371aa-Paper-Conference.pdf) | [Code](https://github.com/yangcaoai/CoDA_NeurIPS2023) |

### Language-driven 3D Understanding / 语言驱动的三维理解

| Method | Year | Task | Paper | Code |
| --- | ---: | --- | --- | --- |
| 3D-LLM | 2023 | 3D Visual Grounding; 3D Question Answering; 3D Dialogue | [Paper](https://papers.neurips.cc/paper_files/paper/2023/hash/413885e70482b95dcbeeddc1daf39177-Abstract-Conference.html) | [Code](https://github.com/UMass-Embodied-AGI/3D-LLM) |
| Chat-Scene | 2024 | 3D Visual Grounding; 3D Captioning; 3D Question Answering | [Paper](https://proceedings.neurips.cc/paper_files/paper/2024/hash/cebbd24f1e50bcb63d015611fe0fe767-Abstract-Conference.html) | [Code](https://github.com/Collab-Gen/Chat-Scene) |
| SeeGround | 2025 | Zero-shot 3D Visual Grounding | [Paper](https://openaccess.thecvf.com/content/CVPR2025/papers/Li_SeeGround_See_and_Ground_for_Zero-Shot_Open-Vocabulary_3D_Visual_Grounding_CVPR_2025_paper.pdf) | [Code](https://github.com/iris0329/SeeGround) |
| VLM-Grounder | 2025 | Zero-shot 3D Visual Grounding | [Paper](https://proceedings.mlr.press/v270/xu25c.html) | [Code](https://github.com/InternRobotics/VLM-Grounder) |
| UniGround | 2026 | Training-free 3D Visual Grounding | [Paper](https://arxiv.org/abs/2603.08131) | — |
| M3Fusion | 2026 | 3D Visual Grounding; Multiview Multimodal 3D Perception | [Paper](https://doi.org/10.1360/SSI-2025-0293) | — |

### World Models and Dynamic Prediction / 世界模型与动态预测

| Method | Year | Task | Paper | Code |
| --- | ---: | --- | --- | --- |
| POP-3D | 2023 | Open-vocabulary 3D Occupancy Estimation (Current State) | [Paper](https://papers.nips.cc/paper_files/paper/2023/hash/9e30acdeff572463c1db9b7de59de64c-Abstract-Conference.html) | [Code](https://github.com/vobecant/POP3D) |
| GaussTR | 2025 | Self-supervised 3D Occupancy Estimation (Current State) | [Paper](https://openaccess.thecvf.com/content/CVPR2025/html/Jiang_GaussTR_Foundation_Model-Aligned_Gaussian_Transformer_for_Self-Supervised_3D_Spatial_Understanding_CVPR_2025_paper.html) | [Code](https://github.com/hustvl/GaussTR) |
| LOMA | 2025 | Language-assisted Semantic Scene Completion (Current State) | [Paper](https://ojs.aaai.org/index.php/AAAI/article/view/32264) | — |
| OccLLaMA | 2026 | Future Occupancy Prediction; Occupancy-Language-Action Modeling | [Paper](https://ieeexplore.ieee.org/abstract/document/11696643/) | — |
| GAIA-1 | 2023 | Action-conditioned Future Driving Video Generation | [Paper](https://arxiv.org/abs/2309.17080) | — |
| DriveDreamer | 2024 | Controllable Future Driving Video Generation | [Paper](https://www.ecva.net/papers/eccv_2024/papers_ECCV/html/6416_ECCV_2024_paper.php) | [Code](https://github.com/JeffWang987/DriveDreamer) |

### Embodied Decision and Interaction / 具身决策与交互

| Method | Year | Task | Paper | Code |
| --- | ---: | --- | --- | --- |
| LEO | 2024 | Embodied Navigation; Robotic Manipulation; 3D Visual Grounding; 3D Question Answering | [Paper](https://proceedings.mlr.press/v235/huang24ae.html) | [Code](https://github.com/embodied-generalist/embodied-generalist) |
| NavFoM | 2026 | Cross-embodiment Navigation; Cross-task Navigation | [Paper](https://proceedings.iclr.cc/paper_files/paper/2026/hash/ceb45c48e29e7f49b0b47edb98e43691-Abstract-Conference.html) | — |
| DualVLN | 2026 | Vision-and-Language Navigation; Continuous Trajectory Generation | [Paper](https://openreview.net/pdf?id=GK4rznYwhn) | [Code](https://github.com/InternRobotics/InternNav) |
| VoxPoser | 2023 | Language-guided Robotic Manipulation; 3D Value-map Planning | [Paper](https://proceedings.mlr.press/v229/huang23b.html) | [Code](https://github.com/huangwl18/VoxPoser) |
| SocialNav | 2026 | Socially-aware Embodied Navigation | [Paper](https://openaccess.thecvf.com/content/CVPR2026/html/Chen_SocialNav_Training_Human-Inspired_Foundation_Model_for_Socially-Aware_Embodied_Navigation_CVPR_2026_paper.html) | [Code](https://github.com/AMAP-EAI/SocialNav) |
| PathPainter | 2026 | BEV-guided Embodied Navigation | [Paper](https://arxiv.org/abs/2605.07496) | — |

## Datasets / 数据集

完整条目及模态说明见[datasets.csv](datasets.csv)。该表也包含评测基准、衍生标注及仿真学习环境，其类型在Description中注明。

| Dataset / Benchmark | 主要用途 |
| --- | --- |
| ScanNet / ScanNet200 / S3DIS / Replica | 室内三维分割、场景表征与语义建图 |
| nuScenes / SUN RGB-D | 驾驶场景感知与室内三维检测 |
| ScanRefer / Multi3DRefer | 单目标及多目标三维视觉定位 |
| ScanQA / SQA3D | 场景问答与情境式空间推理 |
| SceneVerse / 3DSSG | 三维视觉语言学习与场景关系建模 |
| R2R / ALFRED | 视觉语言导航与家庭任务执行 |
| CALVIN / RLBench / LIBERO | 长程或多任务机器人操作 |
| Occ3D-nuScenes / SemanticKITTI / UniOcc | 占用估计、语义场景补全与时序占用评测 |
| 3DMM-Vet / Anywhere3D-Bench / IRef-VLA | 三维理解、多层级定位与交互式指代评测 |
| Social-VLN | DualVLN所讨论的社会导航评测设置 |

ScanNetv2在ScanNet条目中说明，不重复计为独立数据集。ScanRefer、ScanQA等语言标注与底层ScanNet扫描是关联但不同的资源；Occ3D-nuScenes也区别于原始nuScenes。RLBench包含仿真环境，不能视为一个固定规模的静态数据文件。Social-VLN链接至作者项目说明，并非已验证的独立数据下载。

## Evaluation Metrics / 评价指标

完整英文名称、简要定义和优化方向见[metrics.csv](metrics.csv)。

| 适用任务 | 主要指标 |
| --- | --- |
| 三维分割与检测 | IoU、mIoU、AP、mAP、OA、NDS |
| 三维视觉定位 | Acc@0.25、Acc@0.5、F1@0.5 |
| 问答与描述 | BLEU、METEOR、ROUGE、CIDEr、EM、Avg. Acc. |
| 场景图 | Recall、R@K，以及对应任务定义下的mAP |
| 占用估计 | IoU、mIoU、RayIoU |
| 导航与操作 | SR、SPL、NE、OSR、Goal Progress、Completion Rate、Avg. Reward |
| 效率与社会导航 | Feature Construction Time、FPS、HCR、Distance Compliance Rate |

同名mAP的匹配规则和类别集合可能不同，应以相应官方评测协议为准。BLEU-1作为BLEU的具体变体、EM@1作为EM的具体设置、RayIoU@1m/2m/4m作为RayIoU的阈值设置，在Description中说明。CIDEr可能按×100尺度报告，各种指标及不同尺度不能直接作数值比较。SR和Success Rate合并为一个条目。

## Notes / 使用说明

链接核查按三张CSV中的去重地址统计：176个地址均已核查，其中167个取得在线页面或官方索引的对应证据；其余9个DOI地址已由作者人工确认能够跳转至出版页面，且页面论文标题与相应方法对应，涉及FMGS、Lang3DSG、OV-SCAN、ConceptGraphs、OccNeRF、Scene-MMKG、3UR-LLM、CoDAv2和M3Fusion。部分地址会限制自动抓取，链接核查不包含代码运行验证。

- 本资源库整理公开论文、算法、数据集和评价指标的索引信息，不表示作者已重新实现或复现全部算法，也不提供统一实验排行榜。
- 不同研究采用的数据划分、监督条件及评价协议可能存在差异，论文信息不构成统一实验设置下的性能排名。
- POP-3D、GaussTR等条目按实际功能注明当前占用估计。将其放在世界模型相关分类中不代表其具备未来环境预测能力。Anticipation-VLA的子目标预测也不直接等于完整环境动力学预测。
- Uni3D、OpenShape等属于三维表征模型；SelfOcc、VoxFormer等部分条目属于比较基线。具体作用见Task，不能将所有条目都称为基础模型。
- **名称与版本**：CoDA原论文表4将Det-CLIP²与3D-CLIP分别列出，因此CLIP2与3D-CLIP (CoDA baseline)分开收录。后者的Paper链接指向定义该比较基线的CoDA论文，Year为该比较的出处年份。ConceptGraphs对应正文写法Concept-Graphs；Oryx MLLM对应ORYX。表10的Chat-3D v2为Chat-Scene同一研究线的早期实现，按家族收录在Chat-Scene条目中，但不将二者实验配置等同；3UR-LLM+按同篇论文配置并入3UR-LLM。
- **年份与链接**：DrivePI、DualVLN和OccLLaMA采用已确认的2026年正式发表记录，区别于稿中引用的预印本年份。预印本地址不被表述为正式会议DOI。部分官方代码仓库可能迁移、改名或更新主分支，使用时应选择与所引论文对应的版本；RoboBrain 2.0的作者代码入口目前重定向至后续版本仓库。
- Code只填写本次确认具有作者关联的官方入口；空值可能表示尚未发布、官方身份尚未确认或当前入口无法核实。链接核查不包含安装、训练或运行验证。网站的访问限制或临时失败也不等于资源不存在。
- 数据集通过原始发布方或学术托管入口访问，本库不重新分发原始数据。第三方资源的版权与使用许可归原作者或相应权利人所有，访问、下载和使用需遵守各资源自身要求。

## Citation / 引用说明

配套综述题名：**基础模型驱动的三维空间智能与具身决策综述**。

英文题名：**A survey of foundation model-driven 3D spatial intelligence and embodied decision-making**。

作者：王思芳、吴晗、李嘉巍、张宇航、徐明亮。

引用综述时请以最终正式出版信息为准；本页尚未填写卷期、页码或DOI。实际使用某一方法或数据集时，请同时引用相应原始论文。ScienceDB资源标识符在正式发布后由作者补充。

## Updates / 后续更新

本资源库可随相关研究发展持续更新，并保留与论文对应的首版内容。
