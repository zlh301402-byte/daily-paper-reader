---
title: "CADGrasp: Learning Contact and Collision Aware General Dexterous Grasping in Cluttered Scenes"
title_zh: CADGrasp：学习杂乱场景中的接触与碰撞感知通用灵巧抓取
authors: "Jiyao Zhang, Zhiyuan Ma, Tianhao Wu, Zeyuan Chen, Hao Dong"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=CB8jwNE2vV"
tags: ["query:aerial-arm"]
score: 7.0
evidence: 灵巧抓取方法，可应用于空中机器人的抓取任务
tldr: 该论文提出CADGrasp算法，通过两阶段流程实现杂乱场景中的灵巧抓取。第一阶段预测场景解耦的接触与碰撞感知表示（稀疏IBS），第二阶段优化抓取位姿。该方法有效提升了灵巧手在复杂布局中的抓取成功率和安全性。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-cb8jwne2vv/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1411, \"height\": 979, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-cb8jwne2vv/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1409, \"height\": 517, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-cb8jwne2vv/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1398, \"height\": 282, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-cb8jwne2vv/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1439, \"height\": 415, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-cb8jwne2vv/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 997, \"height\": 601, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-cb8jwne2vv/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1405, \"height\": 500, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-cb8jwne2vv/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 645, \"height\": 540, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-cb8jwne2vv/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1402, \"height\": 1996, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-cb8jwne2vv/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1226, \"height\": 839, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-cb8jwne2vv/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 848, \"height\": 580, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-cb8jwne2vv/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1444, \"height\": 419, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-cb8jwne2vv/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1441, \"height\": 153, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-cb8jwne2vv/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1326, \"height\": 284, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-cb8jwne2vv/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 693, \"height\": 318, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-cb8jwne2vv/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1154, \"height\": 397, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-cb8jwne2vv/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 730, \"height\": 218, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-cb8jwne2vv/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 718, \"height\": 299, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-cb8jwne2vv/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1081, \"height\": 390, \"label\": \"Table\"}]"
motivation: 灵巧手在杂乱环境中抓取面临高自由度、遮挡和碰撞问题，现有方法缺乏接触与碰撞感知。
method: 提出两阶段算法：先预测稀疏IBS表示编码几何和接触关系，再进行抓取位姿优化。
result: 在多个基准上实现了稳定且无碰撞的灵巧抓取，优于现有方法。
conclusion: 接触与碰撞感知表示灵巧抓取的关键，该方法可推广至空中机器人的抓取操作。
---

## Abstract
Dexterous grasping in cluttered environments presents substantial challenges due to the high degrees of freedom of dexterous hands, occlusion, and potential collisions arising from diverse object geometries and complex layouts. To address these challenges, we propose CADGrasp, a two-stage algorithm for general dexterous grasping using single-view point cloud inputs. In the first stage, we predict a scene-decoupled, contact- and collision-aware representation—sparse IBS—as the optimization target. Sparse IBS compactly encodes the geometric and contact relationships between the dexterous hand and the scene, enabling stable and collision-free dexterous grasp pose optimization. To enhance the prediction of this high-dimensional representation, we introduce an occupancy-diffusion model with voxel-level conditional guidance and force closure score filtering. In the second stage, we develop several energy functions and ranking strategies for optimization based on sparse IBS to generate high-quality dexterous grasp poses. Extensive experiments in both simulated and real-world settings validate the effectiveness of our approach, demonstrating its capability to mitigate collisions while maintaining a high grasp success rate across diverse objects and complex scenes.

---

## 论文详细总结（自动生成）

# CADGrasp 论文详细总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

灵巧手在杂乱场景中的抓取是机器人自主操作的关键挑战。与单物体抓取不同，杂乱场景中物体堆叠导致遮挡、部分观测，且灵巧手高自由度（DoF）与复杂布局使得直接映射点云到位姿的非线性极强，对物理约束（如碰撞）非常敏感。现有方法（如DexGraspNet2.0）通过端到端扩散模型直接预测位姿，但泛化能力受限；两阶段方法（如GraspTTA）依赖完整物体几何，不适用于部分观测的杂乱场景。因此，论文提出一种**接触与碰撞感知的中间表示**——稀疏IBS（Interaction Bisector Surface），将两阶段框架应用于杂乱场景，实现稳定、无碰撞的灵巧抓取。

## 2. 论文提出的方法论：核心思想、关键技术细节

**核心思想**：将抓取问题分解为两个阶段：  
- **第一阶段（条件IBS生成）**：从单视角点云预测稀疏IBS（场景解耦的接触与碰撞感知表示）。  
- **第二阶段（抓取位姿优化）**：以预测的稀疏IBS为约束，通过能量函数优化生成抓取位姿。

**关键技术细节**：  
1. **稀疏IBS定义**：在抓取种子点 \( p_s \) 和手腕位姿 \( T \) 定义的规范空间中，构造 \( n \times n \times n \) 体素网格（\( n=40 \)），每个体素编码三个通道：IBS表面占据、拇指接触点占据、其他手指接触点占据。该表示紧凑编码手与场景的几何和接触关系，且与场景解耦，适用于部分观测。  
2. **手腕位姿估计**：使用ResUNet14提取点云特征，预测点云抓取性（graspness），经FPS采样得到种子点；再用去噪扩散模型（DDPM）从种子点特征生成手腕位姿 \( T \)。  
3. **IBS候选生成**：将观测点云规范化和体素化后，训练一个**条件占据扩散模型**（occupancy-diffusion）。使用3D UNet（4级：40³,20³,10³,5³，特征维32,64,128,256），通过体素级层级条件拼接点云特征。损失函数为噪声预测的L2损失。采样多个IBS候选后，基于力闭合得分排序，选最优作为最终中间表示。  
4. **抓取位姿优化**：针对预测的IBS，定义能量函数 \( E = \lambda_1 E_j + \lambda_2 E_{sp} + \lambda_3 E_p + \lambda_4 E_d \)，分别约束关节极限、自穿透、接触力（通过IBS表面法向）和碰撞避免（手指与IBS表面点距离）。使用梯度优化同时优化多个初始配置，按最终残差排序选择最优位姿。

**公式说明**（文字）：  
- 关节极限能量 \( E_j \)：超出预设范围的惩罚。  
- 自穿透能量 \( E_{sp} \)：手部点对间过近距离的惩罚。  
- 接触能量 \( E_p \)：鼓励手指接触点沿IBS表面法向指向物体。  
- 碰撞能量 \( E_d \)：将手指约束在IBS表面外侧（安全空间），含拇指与其他手指的权重。

## 3. 实验设计：数据集、场景、benchmark及对比方法

- **数据集**：  
  - 训练对象：GraspNet1Billion中的60个训练物体。  
  - 测试对象：GraspNet1Billion + ShapeNet中的1259个物体。  
  - 抓取场景：DexGraspNet2.0提供的7600个训练场景（采样100个用于IBS生成训练）和670个测试场景，按密度分为dense（8-11物体）、random（1-10）、loose（1-2）。  
- **基准（Benchmark）**：采用与DexGraspNet2.0相同的评估协议，报告**成功率（Success Rate）**。  
- **对比方法**：  
  - DexGraspNet2.0（端到端扩散基线）  
  - HGC-Net（回归基线）  
  - ISAGrasp（单物体回归，适配到杂乱场景）  
  - GraspTTA（两阶段单物体，省略优化阶段）  
- **额外评估**：  
  - 跨本体泛化（零样本迁移到Allegro手）。  
  - 真实世界实验：使用Flexiv Rizon-4机械臂+Leap Hand，30个物体，5个杂乱场景（4-8物体/场景）。

## 4. 资源与算力

论文明确说明：  
- 训练设备：8块NVIDIA RTX 4090 GPU。  
- 批大小：64。  
- 优化器：AdamW，学习率6e-5。  
- 训练轮数：130 epochs，耗时约2天。  
- 推理时间：单次抓取平均6.51秒（含手腕估计1.38s + IBS生成1.39s + 排序0.71s + 优化3.03s）。  

信息较为完整，算力描述清晰。

## 5. 实验数量与充分性

论文进行了充分的实验：  
- **模拟实验**：在670个测试场景（含三个密度级别）上与4种基线对比，报告成功率。  
- **跨本体实验**：在Allegro手上零样本测试。  
- **真实世界实验**：5个场景，30个物体，共31-32次抓取尝试。  
- **消融实验**：  
  - 模块交互（IBS排序、位姿排序、接触分解），8种组合（表5）。  
  - 体素分辨率（2.5mm、5mm、10mm），比较内存与成功率（表6）。  
  - 物体体积与成功率关系（表7）。  
  - 推断效率与运行时间分解。  
  - 握持多样性分析（图8）、穿透深度分析（图9）。  

实验覆盖核心对比、消融、跨场景、跨本体、真实部署，且均以标准协议执行，客观公平。消融实验验证了每个设计的必要性。不足之处：未报告详细的误差棒（标准差只提及“small deviations”，未在表中给出）。

## 6. 论文的主要结论与发现

- 提出的两阶段框架CADGrasp在模拟和真实环境中均优于现有方法，在dense场景下成功率86.5%（GraspNet-1B），比DexGraspNet2.0（83.3%）高约3.2个百分点。  
- 稀疏IBS作为中间表示能有效编码接触与碰撞信息，避免对完整物体几何的依赖，且可零样本迁移到不同灵巧手（Allegro）。  
- 体素级条件扩散模型能高效生成高质量IBS；力闭合排序能筛选更优候选。  
- 真实世界平均成功率93.8%（30/32），显著高于DexGraspNet2.0的83.9%。  
- 方法在小型物体上成功率略低（77.0%），但对中等和大型物体表现稳健（91.5%）。  
- 推理时间6.51秒，优于其他两阶段方法（如GraspTTA 43.23秒）。

## 7. 优点：方法或实验设计上的亮点

- **创新性**：首次将IBS作为杂乱场景灵巧抓取的中间表示，实现场景解耦、接触与碰撞感知，克服了两阶段方法在部分观测下的局限。  
- **通用性**：表示与手部本体无关，零样本跨手泛化，降低对特定手部数据的依赖。  
- **完备性**：两阶段框架设计合理：第一阶段用扩散模型生成候选并排序，第二阶段用多能量函数优化，兼顾质量和物理约束。  
- **实验全面**：涵盖模拟和真实、多密度场景、跨手、消融、计算效率分析，验证了方法的鲁棒性和实用性。  
- **开源准备**：代码将在接收后开放，便于复现。

## 8. 不足与局限

- **小型物体性能有限**：体积<0.00025m³的物体成功率仅77.0%，可能因训练数据中该类物体较少或体素分辨率不足以捕捉精细细节。  
- **推理时间较长**：6.51秒非实时，虽优于同类方法，但可进一步优化采样器（如DDIM）和并行化。  
- **实验统计量不足**：未在表格中呈现误差棒或置信区间，虽然提及“small deviations”但缺乏量化。  
- **真实实验规模**：仅5个场景、30个物体，样本量较小，可能不足以完全反映真实分布。  
- **未涉及动态场景**：假设场景静态，未考虑物体移动或机器人运动时的实时调整。  
- **依赖仿真训练**：所有训练在DexGraspNet2.0的仿真场景中进行，Sim-to-Real差距仅通过点云表示部分缓解，但未在多种真实环境（不同光照、纹理）中验证。  
- **未讨论社会影响**：虽然论文包含NeurIPS checklist，但未深入讨论潜在负面应用或公平性。

（完）
