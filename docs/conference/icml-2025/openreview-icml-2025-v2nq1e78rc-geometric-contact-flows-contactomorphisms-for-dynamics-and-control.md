---
title: "Geometric Contact Flows: Contactomorphisms for Dynamics and Control"
title_zh: 几何接触流：用于动力学与控制的接触同胚
authors: "Andrea Testa, Søren Hauberg, Tamim Asfour, Leonel Rozo"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=v2nQ1e78Rc"
tags: ["query:aerial-arm"]
score: 7.0
evidence: 提供接触动力学的几何建模，可应用于空中机器人物理交互控制
tldr: 针对复杂动力学系统中力交换与耗散的建模挑战，本文提出几何接触流（GCF）框架，利用黎曼与接触几何作为归纳偏置，构建潜在接触哈密顿模型并集成接触同胚来适应目标动力学。该方法在学习接触动力学时保持稳定性，为空中机械臂的物理交互控制提供了理论基础。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 919, \"height\": 402, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 848, \"height\": 506, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 816, \"height\": 303, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 805, \"height\": 310, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1773, \"height\": 1232, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 827, \"height\": 237, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 837, \"height\": 314, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 857, \"height\": 559, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 854, \"height\": 349, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 818, \"height\": 608, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 847, \"height\": 277, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 842, \"height\": 655, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 799, \"height\": 826, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 822, \"height\": 555, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 826, \"height\": 620, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 845, \"height\": 659, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 802, \"height\": 310, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 799, \"height\": 307, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 794, \"height\": 263, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 849, \"height\": 615, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 863, \"height\": 357, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 848, \"height\": 742, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v2nq1e78rc/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 828, \"height\": 629, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-v2nq1e78rc/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 848, \"height\": 111, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v2nq1e78rc/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 846, \"height\": 113, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v2nq1e78rc/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 857, \"height\": 180, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v2nq1e78rc/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 840, \"height\": 179, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v2nq1e78rc/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 862, \"height\": 153, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v2nq1e78rc/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 864, \"height\": 201, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v2nq1e78rc/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 860, \"height\": 210, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v2nq1e78rc/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 860, \"height\": 210, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v2nq1e78rc/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 674, \"height\": 314, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v2nq1e78rc/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 713, \"height\": 296, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v2nq1e78rc/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 796, \"height\": 211, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v2nq1e78rc/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 800, \"height\": 276, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v2nq1e78rc/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 876, \"height\": 369, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v2nq1e78rc/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 857, \"height\": 498, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v2nq1e78rc/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 857, \"height\": 498, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v2nq1e78rc/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 617, \"height\": 544, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v2nq1e78rc/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 843, \"height\": 275, \"label\": \"Table\"}]"
motivation: 复杂动力学系统建模困难，特别是涉及力交换和耗散的场景，需要几何约束和能量传递的精确刻画。
method: 构建潜在接触哈密顿模型作为先验，通过集成接触同胚（contactomorphisms）自适应目标动力学，保持稳定性与能量守恒。
result: 在多个接触动力学基准上，GCF优于现有方法，并能进行不确定性感知的轨迹预测。
conclusion: 结合几何归纳偏置的接触流框架有效提升了接触动力学的学习与控制性能。
---

## Abstract
Accurately modeling and predicting complex dynamical systems, particularly those involving force exchange and dissipation, is crucial for applications ranging from fluid dynamics to robotics, but presents significant challenges due to the intricate interplay of geometric constraints and energy transfer. This paper introduces Geometric Contact Flows (GFC), a novel framework leveraging Riemannian and Contact geometry as inductive biases to learn such systems. GCF constructs a latent contact Hamiltonian model encoding desirable properties like stability or energy conservation. An ensemble of contactomorphisms then adapts this model to the target dynamics while preserving these properties. This ensemble allows for uncertainty-aware geodesics that attract the system’s behavior toward the data support, enabling robust generalization and adaptation to unseen scenarios. Experiments on learning dynamics for physical systems and for controlling robots on interaction tasks demonstrate the effectiveness of our approach.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）
- **核心问题**：准确建模和预测涉及力交换与耗散的复杂动力学系统（如流体动力学、机器人交互）是重要的科学和工程挑战。传统黑箱模型（如MLP）缺乏物理可解释性，在数据支持区域外泛化不可靠，无法捕捉系统变量间由能量函数支配的物理关系。
- **整体含义**：本文提出**几何接触流（Geometric Contact Flows, GCF）**框架，利用**黎曼几何**和**接触几何**作为归纳偏置，学习具有能量耗散、力交互等特性的复杂动力学系统，同时保持物理一致性和鲁棒泛化能力。该工作为数据驱动的物理仿真、机器人技能学习等提供了新的几何先验建模范式。

## 2. 论文提出的方法论：核心思想、关键技术细节
### (a) 核心思想
- **潜在接触哈密顿模型**：在一个低维潜在空间（接触流形）中定义一个具有期望性质（如稳定性、节能、收敛）的接触哈密顿动力学，作为归纳偏置。
- **接触同胚集成**：通过一组保持接触结构的光滑可逆映射（contactomorphisms）将潜在动力学适配到目标观测动力学，同时保留潜在系统的物理属性（如能量演化律）。
- **不确定性感知泛化**：利用集成模型的预测方差量化不确定性，并通过修改黎曼度量使测地线避开高不确定区域，引导系统轨迹回归到数据支持区域。
- **安全区域修正**：将障碍物等不安全区域映射到潜在空间，通过惩罚项迫使轨迹避开这些区域。

### (b) 关键技术细节
- **接触哈密顿动力学**：在(2d+1)维接触流形上定义哈密顿函数 \( H(z) \)，其向量场由式(2)给出，流线为接触同胚。选取特定形式的 \( H_g \)（如式(7a)-(7c)）可赋予目标系统周期、收敛或安全停止等行为。
- **接触同胚网络**：由K个参数化子流组成，每个子流通过积分一个特定形式的接触哈密顿向量场得到（式(11)），该哈密顿由随机傅里叶特征网络（RFFN）参数化。使用接触分裂积分器保持结构，并可解析求逆。
- **训练损失**：同时最小化环境空间和潜在空间的轨迹预测误差（式(12)），通过权重 \( w_x \gg w_z \) 平衡，潜在项起正则化作用。
- **集成训练**：训练N个随机初始化的接触同胚，将同一轨迹映射到N个潜在轨迹，随机采样逆映射计算环境预测，平均损失（算法2）。
- **不确定性引导控制**：将潜在空间中的不确定性项 \( \sigma_z \) 加入最优控制目标（式(18)），通过小控制输入 \( u \) 弯曲轨迹避开高不确定区；加入障碍能量项 \( E_\Upsilon \)（式(19)）实现障碍规避。

### (c) 公式与算法流程（文字说明）
- **潜在动力学演化**：\( z(t) = \varphi_g(t)( z(0) ) \) 由选择的哈密顿 \( H_g \) 生成。
- **完整预测流**：\( x(t) = \varphi_r^{-1}(T) \circ \varphi_g(t) \circ \varphi_r(T)( x_0 ) \)，即先映射到潜在，积分潜在动力学，再映射回环境。
- **不确定性计算**：将环境点 \( x \) 通过N个接触同胚得到N个潜在点，计算方差 \( \sigma_z \)，类似计算环境方差 \( \sigma_x \)。
- **自适应控制**：求解最优控制问题 min\_u ∫(σ_z² + ‖u‖²) dt，s.t. ˙z = Z_{Hg} + u，使轨迹朝低不确定性方向修正。

## 3. 实验设计：数据集/场景、基准、对比方法
### (a) 数据集与场景
- **弹簧网格动力学**（60维）：20个不同初始条件的二维方形网格节点（4×4），由弹簧连接，模拟大变形和振荡。仿真8秒。
- **量子动力学**：单模玻色子系统，其期望位置、动量和相位演化由接触哈密顿算符控制。20个不同参数系统，仿真8秒。
- **手写轨迹数据集**：LASA（一阶简单轨迹）和 DigiLeTs（二阶复杂自交叉轨迹），各4个字符。
- **机器人任务**：① 缠绕拉动任务（Wrap-and-Pull）：机器人将绳缠绕在鼓上并拉动；② 洗碗机装载任务（Dishwasher Loading）：机器人拉篮、等待放盘、推篮、归位。均为真实机器人平台（Franka Emika Panda）。

### (b) 基准方法对比
- **EF**（Euclideanizing Flows）：使用微分同胚映射一阶动力学。
- **NCDS**（Neural Contractive Dynamical Systems）：强制全局收缩的一阶系统。
- **HNN**（Hamiltonian Neural Networks）：学习保守哈密顿系统。
- **DHNN**（Dissipative Hamiltonian Neural Networks）：扩展HNN以包含耗散。
- **MLP**（多层感知机）：纯黑箱基线。

### (c) 评价指标
- 动态时间弯曲距离（DTWD）衡量轨迹重构误差。
- 收敛比率（轨迹在数据流形内停留时间百分比）衡量泛化能力。
- 能量消耗（焦耳）衡量机器人交互效率。
- 障碍物回避中的距离跟踪。

## 4. 资源与算力
- **文中说明**：框架运行于配备 13th Gen Intel Core i7-13850HX CPU 的机器上，未提及使用GPU。训练历时约 **5000个epoch**，平均耗时 **4小时**。
- **缺失信息**：未明确说明是否使用GPU、GPU型号及数量。推理时间有报告（表17），但训练算力未进一步量化。

## 5. 实验数量与充分性
### 实验数量
- **物理系统重建**：弹簧网格（20个系统，20次试验？），量子系统（20个系统，20次试验？），手写数据（8个字符，每种方法有统计均值和方差），机器人任务（5次重复试验）。
- **消融实验**：
  - 接触结构保持 vs 普通微分同胚（重建和泛化表现）。
  - 损失权重 \( w_z \) 的影响。
  - 哈密顿参数化（完整、去掉质量矩阵、去掉势能等）。
  - 网络架构（MLP、RBF、RFFN）。
  - 集成 vs 单映射的泛化对比。
- **可扩展性实验**：在合成数据上改变目标维度（6-14 DOF）和模型规模（K, nh），评估重构精度和推理时间。

### 充分性与公平性
- 对比方法均选取最佳配置，且报告了多次试验的均值与标准差，统计意义明确。
- 消融研究覆盖了关键组件，验证了每个设计选择的必要性。
- 实验覆盖了从低维简单系统（手写字符）到高维复杂系统（弹簧网格、量子系统）以及真实机器人交互，场景多样。
- 未在相同算力下严格复现所有基线（仅使用作者发布或最佳配置），但已尽力对齐参数量，具有一定公平性。

## 6. 论文的主要结论与发现
- **主要结论**：GCF在接触动力学建模中显著优于现有基于微分同胚、哈密顿或耗散哈密顿的方法，在物理系统重建、手写轨迹生成和机器人交互任务中均取得领先性能。
- **关键发现**：
  - 接触同胚集成通过不确定性量化有效识别数据边界，引导轨迹回归流形（泛化性能提升）。
  - 保守/安全潜在动力学可传递至环境空间，实现能量自适应停止（如机器人荷重任务）。
  - 接触结构保持（而非普通微分同胚）对于维持物理可解释性和泛化至关重要。
  - 潜在损失权重 \( w_z \) 可有效正则化潜在空间，提升环境重构质量。
  - RFFN网络在平滑性和表达力上优于MLP和RBF。

## 7. 优点
- **几何归纳偏置的创新**：首次将接触几何与集成学习结合用于动力学建模，自然处理非保守力与耗散。
- **可解释性与物理一致性**：接触同胚保证了能量演化律（如式(8)）、阻尼系数等物理量可解析推导。
- **鲁棒泛化机制**：通过集成不确定性修改黎曼度量，无需额外监督即可避免未见过区域。
- **安全交互能力**：引入障碍能量惩罚实现主动避障和碰撞回退，对机器人安全操作至关重要。
- **网络架构可逆性**：接触分裂积分器使得逆映射计算高效，实现单次前向/反向即可完成长时预测。
- **消融全面**：对结构保持、损失设计、哈密顿形式、网络类型、集成必要性等进行了系统验证，结论可靠。

## 8. 不足与局限
- **实验覆盖的局限**：
  - 未在极高维度（>60）或真实流体动力学等经典挑战上验证，可扩展性仅基于合成数据。
  - 对比方法中未包含最新神经ODE变体（如Graph Neural Simulator、Transformer-based dynamics），基线选择有一定年代性。
  - 机器人任务仅包含两个操控场景，且未在多个机器人平台或不同接触类型上比较。
- **偏差风险**：
  - 潜在接触哈密顿的形式（如式(11)）手动设计，可能对特定动力学的泛化能力不足。
  - Lagrangian action s 的估计依赖特定物理假设（如单位质量、线性衰减势能），在更一般系统中可能引入误差。
- **计算与部署限制**：
  - 集成需要训练N个网络并同时维护，推理时多次前向，实时性可能受限（最快至0.194秒/步，见表17）。
  - 未在GPU上评估，若迁移至低成本边缘设备可能性能下降。
- **应用限制**：
  - 需要系统满足自治的接触哈密顿假设，对于非保守且无法用单变量s描述的复杂耗散可能不适用。
  - 当前框架不适用于明确需要时间作为输入的非自治系统（如含时外力）。

（完）
