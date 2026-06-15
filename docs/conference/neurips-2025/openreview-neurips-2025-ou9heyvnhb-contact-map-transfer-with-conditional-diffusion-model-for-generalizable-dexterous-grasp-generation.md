---
title: Contact Map Transfer with Conditional Diffusion Model for Generalizable Dexterous Grasp Generation
title_zh: 基于条件扩散模型的接触图迁移实现通用灵巧抓取生成
authors: "Yiyao Ma, Kai Chen, Kexin ZHENG, Qi Dou"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=ou9HeYvNhB"
tags: ["query:aerial-arm"]
score: 6.0
evidence: 灵巧抓取生成，可用于空中机械臂操作
tldr: 针对灵巧抓取生成中泛化性不足的问题，提出基于条件扩散模型的接触图迁移框架，将形状模板上的高质量抓取迁移到同类别新物体上。该方法将抓取迁移转化为物体接触图生成任务，在多种物体上展现了优越的泛化能力，有助于提升机器人操作中抓取模块的适应性和稳定性。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou9heyvnhb/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1448, \"height\": 339, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou9heyvnhb/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1438, \"height\": 461, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou9heyvnhb/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 729, \"height\": 509, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou9heyvnhb/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1381, \"height\": 320, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou9heyvnhb/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1449, \"height\": 434, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou9heyvnhb/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1446, \"height\": 223, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou9heyvnhb/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 753, \"height\": 380, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou9heyvnhb/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1419, \"height\": 573, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou9heyvnhb/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 735, \"height\": 254, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou9heyvnhb/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1439, \"height\": 378, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou9heyvnhb/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1448, \"height\": 772, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou9heyvnhb/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1305, \"height\": 977, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou9heyvnhb/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1295, \"height\": 1085, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou9heyvnhb/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1359, \"height\": 903, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou9heyvnhb/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1447, \"height\": 1173, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou9heyvnhb/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1409, \"height\": 1046, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou9heyvnhb/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1438, \"height\": 1066, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-ou9heyvnhb/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1441, \"height\": 237, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ou9heyvnhb/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1436, \"height\": 316, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ou9heyvnhb/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 651, \"height\": 441, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ou9heyvnhb/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1189, \"height\": 218, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ou9heyvnhb/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1023, \"height\": 194, \"label\": \"Table\"}]"
motivation: 现有灵巧抓取方法在未见物体和任务上泛化能力差，亟需高效且具备任务适应性的生成框架。
method: 提出接触图迁移框架，利用条件扩散模型从形状模板到新物体生成接触图，实现可泛化的灵巧抓取。
result: 在同类物体上的抓取成功率和多样性显著提升，证明了框架的有效性和泛化能力。
conclusion: 接触图迁移结合扩散模型是实现通用灵巧抓取的有效途径，可扩展到多种机械臂操作场景。
---

## Abstract
Dexterous grasp generation is a fundamental challenge in robotics, requiring both grasp stability and adaptability across diverse objects and tasks. Analytical methods ensure stable grasps but are inefficient and lack task adaptability, while generative approaches improve efficiency and task integration but generalize poorly to unseen objects and tasks due to data limitations. In this paper, we propose a transfer-based framework for dexterous grasp generation, leveraging a conditional diffusion model to transfer high-quality grasps from shape templates to novel objects within the same category. Specifically, we reformulate the grasp transfer problem as the generation of an object contact map, incorporating object shape similarity and task specifications into the diffusion process. To handle complex shape variations, we introduce a dual mapping mechanism, capturing intricate geometric relationship between shape templates and novel objects. Beyond the contact map, we derive two additional object-centric maps, the part map and direction map, to encode finer contact details for more stable grasps. We then develop a cascaded conditional diffusion model framework to jointly transfer these three maps, ensuring their intra-consistency. Finally, we introduce a robust grasp recovery mechanism, identifying reliable contact points and optimizing grasp configurations efficiently. Extensive experiments demonstrate the superiority of our proposed method. Our approach effectively balances grasp quality, generation efficiency, and generalization performance across various tasks. Project homepage: https://cmtdiffusion.github.io/

---

## 论文详细总结（自动生成）

# 论文深度总结

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：灵巧手抓取生成面临两难困境——分析性方法（如力闭合优化）能保证抓取稳定性但计算效率低、缺乏任务适应性；生成式方法（如扩散模型）效率高、能融入任务描述，但严重依赖训练数据的规模和质量，导致对未见物体（OOD）和未见类别泛化能力差。如何同时实现高稳定性、高效率、强泛化性和任务适应性，是当前挑战。

- **研究动机**：作者提出“迁移式框架”，将分析性方法在形状模板上采样的高质量抓取，通过生成式模型高效地迁移到同类别的新物体上，从而融合两种范式的优势。

- **整体含义**：将抓取生成问题重新定义为**物体接触图的跨物体迁移问题**，利用条件扩散模型同时建模物体几何相似性和文本任务描述，实现可泛化的灵巧抓取生成。

## 2. 论文提出的方法论

### 核心思想
- 将抓取迁移问题转化为从模板物体到目标物体**生成物体接触图**（contact map）的任务。
- 引入**双映射机制**的条件扩散模型：模板分支学习模板特征并重建模板接触图；目标分支在目标点云和模板特征的双重条件下进行去噪，生成目标接触图。
- 额外定义**部位图（part map）** 和**方向图（direction map）**，描述更丰富的接触细节，并通过**级联扩散框架**联合生成三个图，保证内部一致性。
- 最后通过**鲁棒优化机制**自动筛选可靠的接触点，高效恢复抓取参数。

### 关键技术细节
1. **条件扩散模型的双分支架构**：
   - **模板分支**：编码器 `f_enc` 提取模板点云与接触图特征 `h_e`，通过适应模块 `A_e` 注入目标分支的特征，用解码器重建模板接触图，最小化重建损失 `L_recon`。
   - **目标分支**：编码器 `g_enc` 提取目标点云与噪声特征 `h_t^a`，通过适应模块 `A_a` 融合模板特征 `h_e`，再与语言特征 `f_l(ℓ)` 拼接，最后解码器预测噪声，最小化扩散损失 `L_diff`。
   - **适应模块**：交叉注意力机制实现双向特征融合，显式建模几何相似性。
   - 总损失：`L_contact = L_recon + λ L_diff`（λ=1）。

2. **级联扩散框架**：
   - 先生成接触图 `c`，然后以 `(x_e, c_e, p_e, x_a, c_pred)` 为条件生成部位图 `p`，再以 `(x_e, c_e, p_e, d_e, x_a, c_pred, p_pred)` 为条件生成方向图 `d`。
   - 模板分支：分别用负对数似然损失（部位图）和余弦相似度损失（方向图）进行监督。
   - 目标分支：各图分别训练扩散网络，但前一阶段的预测作为后续阶段的条件输入，保证一致性。

3. **鲁棒抓取优化**：
   - 基于方向图：同一部位内的方向向量应交于一点（关节位置），通过最小二乘求得估计关节 `Ĵ`。
   - 筛选规则：①平均距离小于阈值 `τ_a`（去除高噪声部位）；②每个点到 `Ĵ` 的距离小于 `τ_b`（去除离群点）。
   - 保留可靠点后，用梯度下降优化手部参数，损失函数包含 `E_cont`（接触图误差）、`E_dir`（方向余弦误差）、`E_h`（穿透、自然度、距离正则项）。

## 3. 实验设计

### 数据集与场景
- **数据集**：自定义的 **CapGrasp 数据集**（1.8k 物体，32 类别，50k 任务抓取），将人体抓取重定向到 ShadowHand。
- **训练/测试划分**：
  - 选择 24 个类别（剔除极少实例的），16 个为**已见类别**（约10%物体作为同级测试），8 个为**未见类别**（用于跨类别泛化测试）。
- **任务类型**：包括任务无关（task-agnostic）和任务导向（task-oriented）两类场景。

### Benchmark 与对比方法
- **任务无关抓取**：分析性方法 DFC、DexGraspNet；生成式方法 ContactGen、UGG；迁移方法 Tink。
- **任务导向抓取**：生成式方法 RealDex、DexGYS；迁移方法 Tink。
- 评价指标：抓取成功率（SR）、穿透深度（Pen.）、接触覆盖率（Cov.）；任务一致性：接触误差（Cont. Err.）、VLM辅助一致性（Consis.）、Chamfer距离、R-Precision、P-FID 等。

### 实验设置补充
- 对每个方法，从模板选5个最优抓取进行迁移或优化，保证公平比较。
- 仿真环境：IsaacGym，重力 -9.8 m/s²，提升10cm后稳定2cm以内为成功。
- 真实世界实验：人形机器人平台 + Inspire 灵巧手，用多视图 RGB 重建点云，测试4类物体、5种任务。

## 4. 资源与算力

- **文中明确说明**：
  - GPU：2 张 **NVIDIA 3090**。
  - 训练时长：约 **24 小时**（1000 epoch，batch size 56，workers 4）。
  - 框架：PyTorch，Adam 优化器，学习率 2e-4。
  - 点云点数：模板和目标各 2048 点，特征维度 512。
  - 扩散步数：训练和采样均 1000 步。
- 未说明：总参数量、内存消耗、推理时间等细节。

## 5. 实验数量与充分性

- **主要实验结果**：
  - 表1：任务无关抓取比较（5个 baselines + 2个消融变体），在已见类别新物体上测试。
  - 表2：任务导向泛化比较（4个 baselines + 2个消融变体），包括已见和未见类别。
  - 表3：消融实验（去除各个模块：适应模块A_a/A_e、级联框架两个变体、任务描述、鲁棒优化），共7组变体。
  - 表4：人体手部抓取比较（ContactGen、Tink）。
  - 表5：生成指标比较（P-FID、CD、R-Precision）。
  - 真实世界实验：5个任务各重复5次，记录平均成功率。
  - 附录补充：对模板选择鲁棒性测试（随机模板、不同生成方法模板）、DexGYS+Template变体比较、级联框架可视化消融、任务嵌入消融等。
  - 定性结果：大量可视化图（Fig.10-17）展示接触图、部位图、方向图、最终抓取效果。

- **充分性评价**：
  - 实验覆盖了**任务无关与任务导向**、**已见与未见类别**、**仿真与真实场景**、**多种baseline**和**消融实验**。
  - 所有对比方法使用了相同的数据集和评价协议，公平性较好。
  - 但缺少统计显著性检验（如多次重复的标准差），部分结果仅有数值无误差棒。
  - 跨类别泛化实验设计合理，但未见类别只有8个，数量有限。

## 6. 论文的主要结论与发现

1. **所提迁移框架在任务无关抓取中**：成功率84.65%超过所有对比方法（DexGraspNet 83.63%、DFC 78.98%），穿透深度仅1.47mm，接触覆盖率38.16%，综合最优。
2. **任务导向泛化**：在已见类别新物体上成功率达79.32%，接触误差0.0287，一致性83.60；在未见类别上成功率74.14%，显著优于RealDex（29.90%）和DexGYS（39.16%）。
3. **各模块均有效**：适应模块（A_a/A_e）、级联框架、任务描述、鲁棒优化分别对性能有正向贡献（消融实验下降明显）。
4. **鲁棒优化策略**：能有效过滤部位图和方向图中的噪声，比仅用接触图更好（79.32 vs 76.14），而不用鲁棒优化反而更差（55.04）。
5. **真实世界验证**：平均成功率70%，表明方法对感知噪声具有一定鲁棒性。
6. **额外验证**：人体手部模型上同样优于ContactGen和Tink；对模板选择鲁棒。

## 7. 优点

- **方法论创新性强**：将抓取迁移重新定义为接触图生成，利用扩散模型同时建模几何相似性和任务语义，新颖且有效。
- **级联扩散框架**：保证接触图、部位图、方向图三者内在一致性，设计巧妙。
- **鲁棒优化机制**：利用方向图几何特性自动筛选可靠点，提升参数恢复的鲁棒性。
- **泛化能力突出**：无需对每个新类别重新训练，直接泛化到未见物体和类别，在多项指标上大幅超越现有方法。
- **实验丰富且公平**：对比方法覆盖主流分析/生成/迁移方法，消融实验系统，附加真实世界验证和人体手部实验。
- **代码与数据开源**（project homepage），可复现性强。

## 8. 不足与局限

- **机械手局限性**：目前仅测试在 ShadowHand（五指灵巧手）上，虽然补充了人体手部实验，但未验证对不同手指数量/形态的跨本体泛化。
- **类别覆盖有限**：CapGrasp 数据集中只用了24个类别（16训练+8测试），未见类别个数较少（8个），泛化结论的统计稳健性受限。
- **计算资源要求**：需要在2张3090上训练24小时，推理时需1000步扩散采样，效率有待提升。
- **真实世界实验规模较小**：仅4类物体、5个任务，且成功率70%，说明仍有提升空间；实验环境相对理想（多视角RGB重建），未测试遮挡、动态光照等复杂条件。
- **缺乏不确定性量化**：所有实验报告的是单次运行结果，未给出多次重复的误差棒或置信区间，可能掩盖方差。
- **任务描述依赖**：假设任务文本准确可用，实际应用中可能面临文本歧义或缺失。
- **模板依赖**：虽然对模板变形有一定鲁棒性，但若模板与目标几何差异极大（如跨类别模板误用），性能可能下降（论文未测试此极端情况）。

（完）
