---
title: "OWMM-Agent: Open World Mobile Manipulation With Multi-modal Agentic Data Synthesis"
title_zh: OWMM-Agent：具备多模态智能体数据合成的开放世界移动操控
authors: "Junting Chen, Haotian Liang, Lingxiao Du, Weiyun Wang, Mengkang Hu, Yao Mu, Wenhai Wang, Jifeng Dai, Ping Luo, Wenqi Shao, Lin Shao"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=vSLzoUoJt6"
tags: ["query:aerial-arm"]
score: 4.0
evidence: 开放世界移动操控的多模态智能体架构，可推广至空中机械臂系统
tldr: 开放世界移动操控需要应对开放指令和复杂环境，且需整合高层决策与底层控制。本文提出OWMM-Agent，一种多模态智能体架构，维护多视图场景帧和智能体状态进行决策，通过函数调用控制机器人。同时，通过多模态智能体数据合成缓解领域偏移问题。实验表明该框架在多个开放场景中有效。该工作为通用移动操控提供了可扩展的解决方案。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-vslzouojt6/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1243, \"height\": 687, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vslzouojt6/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1364, \"height\": 804, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vslzouojt6/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1280, \"height\": 589, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vslzouojt6/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1405, \"height\": 418, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vslzouojt6/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 829, \"height\": 522, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vslzouojt6/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1399, \"height\": 368, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vslzouojt6/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1411, \"height\": 1655, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vslzouojt6/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1433, \"height\": 2047, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-vslzouojt6/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1455, \"height\": 885, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vslzouojt6/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1426, \"height\": 369, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vslzouojt6/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1459, \"height\": 413, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vslzouojt6/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1405, \"height\": 211, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vslzouojt6/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1455, \"height\": 797, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vslzouojt6/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1535, \"height\": 392, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vslzouojt6/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1463, \"height\": 377, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vslzouojt6/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1508, \"height\": 245, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vslzouojt6/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 906, \"height\": 211, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vslzouojt6/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 907, \"height\": 210, \"label\": \"Table\"}]"
motivation: 开放世界移动操控面临指令泛化和系统集成复杂性挑战。
method: 提出多模态智能体架构，融合多视图场景和状态进行决策，通过函数调用控制机器人。
result: 在开放世界场景中实现了有效的移动操控任务。
conclusion: OWMM-Agent为通用移动操控系统设计提供了参考。
---

## Abstract
The rapid progress of navigation, manipulation, and vision models has made mobile manipulators capable in many specialized tasks. 
However, the open-world mobile manipulation (OWMM) task remains a challenge due to the need for generalization to open-ended instructions and environments, as well as the systematic complexity to integrate high-level decision making with low-level robot control based on both global scene understanding and current agent state. To address this complexity, we propose a novel multi-modal agent architecture that maintains multi-view scene frames and agent states for decision-making and controls the robot by function calling.
A second challenge is the hallucination from domain shift. To enhance the agent performance, we further introduce an agentic data synthesis pipeline for the OWMM task to adapt the VLM model to our task domain with instruction fine-tuning. We highlight our fine-tuned OWMM-VLM as the first dedicated foundation model for mobile manipulators with global scene understanding, robot state tracking, and multi-modal action generation in a unified model. Through experiments, we demonstrate that our model achieves SOTA performance compared to other foundation models including GPT-4o and strong zero-shot generalization in real world.
The project page is at https://hhyhrhy.github.io/owmm-agent-project.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

开放世界移动操控（OWMM）任务要求移动操作机器人在未见过的环境中，根据开放式自然语言指令执行操作。该任务面临两大挑战：
- **泛化与集成复杂性**：需要将高层决策（场景理解、任务规划）与底层机器人控制（导航、抓取、放置）进行系统集成，同时保证对未见指令和环境的泛化能力。
- **领域偏移导致的幻觉**：预训练的视觉语言模型（VLM）在机器人任务中会出现领域偏移，例如难以进行非障碍物可导航区域检测、机器人状态跟踪、以及基于自身运动学约束的决策。

现有方法（如2D语义地图、3D语义场+CLIP）受限于嵌入模型能力，难以处理复杂组合指令，且需要耗时的密集三维重建。而直接应用通用VLM（如GPT-4o）又存在上述领域偏移问题。

本文旨在提出一个统一的VLM智能体框架，通过多模态数据合成进行指令微调，使VLM学习全局场景理解、状态跟踪和多模态动作生成，从而解决OWMM任务。

## 2. 论文提出的方法论：核心思想、关键技术细节

### 2.1 核心思想
- **无需详细几何表示**：不需要完整的三维场景重建，仅需预建图阶段的相机位姿图与关联RGB图像，机器人接近目标区域时再获取局部几何信息。
- **利用2D到3D反投影**：通过VLM的视觉-语言对齐能力，将高层语言推理与底层坐标控制衔接起来。
- **多轮、多图、多模态推理**：将OWMM任务建模为VLM的多轮推理问题，VLM生成思维链过程、跟踪智能体状态、输出带坐标的多模态动作。

### 2.2 技术框架

**OWMM-Agent架构**（图2）：
- **输入**：自然语言指令L；预建图相机位姿图G和关联RGB图像I；当前头部相机RGB-D图像I_c, D_c；机器人历史状态H_t-1。
- **VLM核心模型（OWMM-VLM）**：基于InternVL-2.5微调，冻结ViT，微调MLP和LLM。输入多张场景图+当前全景图+指令+历史，输出JSON格式的高层动作（包含动作类型和坐标）。
- **动作执行**：通过函数调用将高层动作转为底层规划器执行：
  - 多种动作类型：场景帧检索（Search Scene Frame）、导航到点（Nav to point）、抓取（Pick）、放置（Place）。
  - 规划器：路径规划器（导航）和运动规划器（机械臂），采样满足机械约束的轨迹。

**思维链（CoT）推理设计**：
- 结构化推理链包含：任务指令理解与总结 → 当前观测的感知与定位 → 任务决策（含目标坐标/边界框） → 决策总结（写入历史，供下一步使用）。
- 目的：解决预训练VLM的目标位置错误、多图像幻觉、长时推理中死循环等问题。

**数据合成流水线**：
1. **PDDL任务规划**：使用Habitat仿真生成符号化任务计划（保证逻辑一致性）。
2. **轨迹执行与数据收集**：记录机器人坐标、动作、物体位置、相机参数。
3. **关键帧选择与过滤**：对导航、抓取、放置动作分别筛选可见且可达的帧。
4. **思维链标注生成**：基于预定义模板生成结构化CoT，并用GPT-4o mini进行语言风格多样化。

### 2.3 关键公式
- 智能体策略：`a_t = F_agent(L, G, I, I_ct, D_ct, x_t)`，输出底层连续动作。
- 高层动作生成：`A_t, H_t = F_vlm(L, G, I, I_ct, H_t-1)`，`a_t = A_t(x_t, D_ct)`（由规划器解析）。

## 3. 实验设计

### 3.1 数据集
- **仿真**：使用Habitat仿真环境（基于HomeRobot框架），143个HSSD场景、157个操作物体（YCB + Google Scanned Objects）、1471个收纳容器。
- **训练/测试分割**：113训练场景 vs 30测试场景；137训练物体 vs 20测试物体（测试集物体完全未见）。
- **最终数据集**：572K个标注，包含Pick（64.7K）、Place（68.9K）、导航（59.6K）、场景帧检索（378.8K）四个子集。

### 3.2 Benchmark与对比方法
- **单步评估**：评估三个核心能力：
  - 自我中心决策（Ego-centric Decision-making）准确率
  - 图像检索（Image Retrieval）准确率
  - 可操作性定位（Affordance Grounding）评分（基于边界框中心点到真值点的距离，标准化后1减）
- **回合评估**：在仿真中完成完整任务，测量物体到目标收纳容器的距离（严格阈值0.85m、宽松阈值1.7m），并报告子目标成功率（图像检索、物体接近、抓取、死循环次数）。
- **真实世界评估**：在实验室环境中使用Fetch机器人，人工确认后执行动作，评估动作正确性、可操作性准确性、目标可达性。

**对比方法**：
- 通用VLM：GPT-4o、InternVL2.5-8B
- 模块化方法：GPT-4o+PIVOT、GPT-4o+RoboPoint（GPT-4o做决策，PIVOT/ RoboPoint提供可操作性定位）
- 消融：OWMM-VLM-8B、OWMM-VLM-38B

## 4. 资源与算力
- **训练**：
  - OWMM-VLM-8B：8块NVIDIA A100 GPU，约7小时（1个epoch）
  - OWMM-VLM-38B：24块NVIDIA A100 GPU，约18小时（1个epoch）
- **基础模型**：InternVL-2.5（8B和38B两个变体），GPU内存需求见附录I，8B模型在单卡A100-40G上推理时间4.84秒（8+1帧），38B模型在4卡A100-40G上推理时间4.39秒（8+1帧）。
- 文中明确给出了训练和推理的算力配置。

## 5. 实验数量与充分性

### 实验数量
- **单步评估**：在4K测试样本上评估，报告了多个模型的5项指标。
- **回合评估**：308个测试回合，报告全任务成功率及子目标成功率。
- **真实世界评估**：10个测试样本，人工评估3项指标。
- **消融研究**：对数据多样性（场景/物体比例）、数据规模（0k/15k/45k/76k/152k）、模型设计（有无beam search、输出格式、有无推理总结）分别进行了实验。
- **故障模式分析**：对100个失败回合进行手动分类。
- **计算效率实验**：比较不同帧数下的推理时间和内存占用。

### 充分性与公平性
- **充分**：覆盖单步、回合、真实世界三个层次的评估，有全面的消融，分析了数据扩展律和多样性影响。
- **客观**：使用了标准化的评分公式和阈值，对比方法按原始设定配置（如RoboPoint、PIVOT的单图模式）。
- **公平**：对比方法GPT-4o+PIVOT/RoboPoint中，GPT-4o负责决策，PIVOT/RoboPoint负责定位；本文模型端到端完成所有功能。由于任务设计不同，直接比较存在一定偏差，但作者在单步评估中同时报告了RoboPoint和PIVOT的单图定位能力作为补充。

## 6. 论文的主要结论与发现
1. **OWMM-VLM-38B**在所有指标上达到SOTA，显著优于GPT-4o等通用模型和模块化方法（单步评估中自我中心决策97.85%，图像检索87.54%，可操作性定位0.88-0.97；回合评估全任务成功率21.90%，无死循环）。
2. **数据扩展至关重要**：随着训练数据从0k增至152k，性能对数级提升，但收益递减，表明存在瓶颈。
3. **对象和环境多样性影响有限**：在控制数据量（45k）下，仅改变场景或物体比例，性能波动<5%。
4. **嵌入式智能可通过数据驱动学习**：机器人距离目标多近才能交互等先验知识可以通过数据学习获得。
5. **推理和总结不可缺失**：去掉推理和总结组件后，图像检索从79.0%降至65.9%，自我中心决策从96.7%降至90.5%。
6. **边界框输出优于直接输出坐标**：利用基础模型预训练的视觉定位知识，输出边界框更好。
7. **真实世界零样本泛化能力强**：尽管只在仿真数据上微调，在真实Fetch机器人上动作生成成功率达90%（27/30）。

## 7. 优点
- **统一的VLM端到端框架**：无需多个独立模型，减少系统复杂度，同时完成场景理解、状态跟踪和动作生成。
- **高效的数据合成流水线**：基于仿真自动生成结构化CoT标注，最小化人工成本，且语言风格多样化增强鲁棒性。
- **创新的推理设计**：结构化思维链解决了预训练VLM在多图像推理和长期任务中的霍尔效应，并实现状态跟踪。
- **验证充分**：在仿真和真实环境均取得了SOTA，并进行了详细消融和故障分析，提供了计算效率分析，整体实验设计严谨。
- **开源**：项目代码和数据集已匿名开源，可复现。

## 8. 不足与局限
- **预建图依赖**：需要预建图阶段（相机位姿图+2D占据地图），未能实现在线探索与建图。
- **复杂操控有限**：仅支持吸盘末端执行器，不适用于灵巧手等复杂末端。
- **跨本体泛化问题**：模型学习了特定机器人（Fetch）的运动学先验（如最大伸展距离），直接部署到其他机器人可能失败。
- **轮次评估绝对成功率较低**：严格阈值下全任务成功率仅21.9%，虽然优于对比方法，但说明任务难度大，且后期抓取/放置环节是主要瓶颈（物体抓取成功率38.56%，目标图像检索30.39%）。
- **真实实验规模小**：仅10个测试样本，虽人工评判，但样本量有限，泛化性尚需更大规模验证。
- **未考虑动态环境中的物体移动**：预建图阶段假设场景静态，动态变化可能影响检索和导航。

（完）
