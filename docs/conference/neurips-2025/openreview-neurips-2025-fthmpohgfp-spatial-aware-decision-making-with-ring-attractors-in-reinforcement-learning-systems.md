---
title: Spatial-Aware Decision-Making with Ring Attractors in Reinforcement Learning Systems
title_zh: 基于环吸引子的空间感知强化学习决策
authors: "Marcos Negre Saura, Richard Allmendinger, Wei Pan, Theodore Papamarkou"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=FthMPOhgfp"
tags: ["query:drone-arm"]
score: 4.0
evidence: 使用环吸引子的空间感知决策强化学习方法，可应用于机器人控制中的旋转角度
tldr: 该论文将环吸引子模型引入深度强化学习，通过显式编码动作空间和空间信息，提高了学习速度和准确性。在机器人控制任务中，环吸引子能够稳定探索过程中的动作选择，尤其适用于包含连续旋转角度的控制场景。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-fthmpohgfp/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 732, \"height\": 645, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fthmpohgfp/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 700, \"height\": 411, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fthmpohgfp/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 708, \"height\": 411, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fthmpohgfp/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1452, \"height\": 450, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fthmpohgfp/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1127, \"height\": 677, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fthmpohgfp/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1273, \"height\": 760, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fthmpohgfp/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1472, \"height\": 463, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fthmpohgfp/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1391, \"height\": 1415, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fthmpohgfp/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1389, \"height\": 1414, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fthmpohgfp/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1067, \"height\": 1309, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-fthmpohgfp/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1401, \"height\": 916, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fthmpohgfp/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 597, \"height\": 2340, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fthmpohgfp/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 617, \"height\": 2327, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fthmpohgfp/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 630, \"height\": 2343, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fthmpohgfp/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 628, \"height\": 2346, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fthmpohgfp/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1390, \"height\": 1021, \"label\": \"Table\"}]"
motivation: 标准深度强化学习在空间感知和连续动作选择上存在局限，受神经科学环吸引子启发提出改进。
method: 在深度强化学习网络中嵌入环吸引子结构，显式编码动作空间并实现时间滤波以稳定动作选择。
result: 实验表明环吸引子提升了强化学习在机器人控制等任务中的学习速度和精度。
conclusion: 环吸引子是一种有效的生物启发式机制，能够增强深度强化学习在空间感知决策中的表现。
---

## Abstract
Ring attractors, mathematical models inspired by neural circuit dynamics, provide a biologically plausible mechanism to improve learning speed and accuracy in Reinforcement Learning (RL). Serving as specialized brain-inspired structures that encode spatial information and uncertainty, ring attractors explicitly encode the action space, facilitate the organization of neural activity, and enable the distribution of spatial representations across the neural network in the context of Deep Reinforcement Learning (DRL). These structures also provide temporal filtering that stabilizes action selection during exploration, for example, by preserving the continuity between rotation angles in robotic control or adjacency between tactical moves in game-like environments. The application of ring attractors in the action selection process involves mapping actions to specific locations on the ring and decoding the selected action based on neural activity. We investigate the application of ring attractors by both building an exogenous model and integrating them as part of DRL agents. Our approach significantly improves state-of-the-art performance on the Atari 100k benchmark, achieving a 53\% increase in performance over selected baselines.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）
- **研究动机**：传统的深度强化学习（DRL）将动作表示为相互正交的向量，忽略了动作之间固有的空间关系和拓扑结构（如机器人关节旋转的连续性、游戏中的邻近战术动作）。这种表示限制了学习效率和泛化能力。
- **整体含义**：受神经科学中环吸引子（ring attractor）网络的启发（最初由Zhang (1996)提出，后由Kim et al. (2017)在果蝇脑中验证），作者提出将环吸引子显式集成到RL框架中。环吸引子能够以圆形拓扑结构稳定地编码空间信息、保持动作之间的连续性，并提供时间滤波（低通滤波）以稳定探索过程中的动作选择。该方法将动作映射到环上的特定位置，通过神经元动力学解码动作，从而实现空间感知和不确定性感知的决策。

### 2. 论文提出的方法论
- **核心思想**：利用环吸引子的循环连接、兴奋-抑制动力学和距离加权连接，在动作空间中建立一种内在的“空间组织”。通过将Q值或策略对数映射为环上高斯信号的幅度和方差，使RL代理能够利用动作间的相邻关系进行平滑过渡。
- **关键技术细节**：
  - **外生CTRNN模型（Section 3.1）**：使用连续时间循环神经网络（CTRNN）实现环吸引子。动作输入为高斯函数和：  
    `x_n(Q) = Σ_a [Q(s,a) / (√(2π) σ_a) · exp(-(α_n - α_a(a))² / (2σ_a²))]`  
    其中`α_n`为神经元偏好角度，`α_a(a)`为动作角度，`Q(s,a)`为Q值，`σ_a`为方差（可表示不确定性）。兴奋性神经元动力学（式6）和抑制性神经元动力学（式7）共同演化形成稳定激活峰。最后通过argmax将神经元活动解码为动作（式8）。
  - **不确定性量化（Section 3.1.3）**：采用贝叶斯线性回归（BLR）作为输出层，通过Thompson采样从后验分布中采样权重，计算Q值的均值`Q̄(s,a)`和方差`σ̄_a²`，输入到环吸引子中。实现了不确定性感知的动作选择。
  - **深度学习RNN模块（Section 3.2）**：将环吸引子建模为具有固定距离加权输入连接和可学习隐藏到隐藏连接的RNN层。输入信号`V(s)`和隐藏状态`U(v)`的权重由指数衰减距离函数`exp(-d(m,n)/λ)`定义，其中`d(m,n)`为环上神经元之间的圆形距离。该模块可作为即插即用层集成到DRL代理中（如BDQN、DDQN、EffZero、PPO等）。
  - **算法流程**：Algorithm 1给出了CTRNN环吸引子动作选择的步骤：计算Q值和不确定性 → 生成高斯输入信号 → 时域演化达到吸引子状态（T=50步） → 解码得到动作。

### 3. 实验设计
- **数据集/场景**：
  - **Atari 100k基准**（Bellemare et al., 2012）：共26个游戏，部分游戏具有强烈的空间成分（如Asterix、Boxing、Ms Pacman等），部分游戏动作空间维数较高（如Seaquest、BattleZone使用双环配置）。
  - **OpenAI Gym Super Mario Bros** (Kauten, 2018)：离散8动作空间。
  - **OpenAI Highway** (Leurent, 2018)：连续1D圆形动作空间（方向盘角度）。
- **基准与对比方法**：
  - **Atari 100k**：对比CURL, SPR, EffZero（复现的基线），以及作者提出的EffZeroRA（集成环吸引子）。
  - **Mario & Highway**：对比标准BDQN、BDQNRA（环吸引子）、BDQNRA-UA（不确定性感知）；以及DDQN vs DDQNRA。另外附录中还展示了PPO-RA vs PPO。
- **消融研究**：
  - CTRNN模型：比较正确动作分布 vs 随机打乱动作在环上的位置（Section A.4.1）。
  - DL RNN模型：移除圆形权重分布（变为标准RNN）后的性能（Section A.4.2）。
  - 此外还验证了预训练和训练后吸引子动力学的保持（Section A.5）。

### 4. 资源与算力
- 论文在**Atari 100k**实验中使用**10块NVIDIA A100 GPU**（每块80GB显存），**512GB RAM**，**128核Intel Xeon CPU**（2.4GHz）。每款游戏训练约**8-10小时**，总估算约**8000 GPU-hours**。
- 其他环境（Highway、Mario Bros）使用本地工作站：Intel Xeon 28核2.1GHz，125GB RAM，**双RTX A5000 GPU**（合计48GB），训练6-12小时/环境。
- CTRNN外生模型计算开销比基线平均高**297.3%**，而DL模块的开销在可接受范围内。

### 5. 实验数量与充分性
- **数量**：覆盖Atari 100k中的26款游戏（有效动作空间可映射为环的），以及额外的Mario Bros和Highway环境。每实验均**10个随机种子×3个样本/种子**。消融实验在多个环境中进行。
- **充分性**：实验设计较为全面，包括主实验、消融研究、吸引力动态分析、以及扩展到策略梯度方法（附录A.3），验证了环吸引子的普适性。对比基线均为当前最优或常用方法，复现了基线以公平比较。
- **客观公平**：使用相同计算资源和数据量，报告均值误差。消融研究有效隔离了关键组件。不足：主要专注于离散动作空间，未在连续控制任务（如MuJoCo）上系统验证。

### 6. 论文的主要结论与发现
- 环吸引子作为RL行为策略能显著**加速学习**并提高最终性能：在Atari 100k上平均提升**53%**（human-normalized score从0.959提升到1.454）。
- **空间性强的游戏**提升最大：Asterix提升110%，Boxing提升105%，Kung-Fu Master提升81%。
- **DL模块**可实现端到端训练且易于集成，计算开销远小于CTRNN外生模型。
- 不确定性感知版本（BDQNRA-UA）进一步优于仅使用固定方差的版本。
- 环吸引子同样适用于**策略梯度方法**（PPO-RA在Mario上提升71.4%）。

### 7. 优点
- **生物启发性强**：直接借用神经科学已验证的环吸引子模型，提供空间归纳偏置。
- **显式空间编码**：避免传统方法依赖代理自主发现动作关系，加速学习。
- **不确定性集成自然**：通过输入高斯信号的方差参数将不确定性量化融入环中，无需额外分离模块。
- **可复用模块化设计**：DL模块可作为输出层替换，兼容DQN、DDQN、EfficientZero、PPO等多种架构。
- **实验验证充分**：在多个基准和消融设计中证明了方法有效性，且代码已开源。

### 8. 不足与局限
- **适用范围限制**：环吸引子主要在具有空间或拓扑结构的动作空间中有效。若动作空间很小（|A|<3）或动作间无相关性（协方差矩阵接近单位阵），则环结构可能带来负收益。
- **CTRNN模型计算开销大**：外生模型比基线慢约300%，限制了实际部署；DL模块虽改善，但RNN本身仍有一定延迟。
- **实验覆盖**：未在真实机器人连续控制（如MuJoCo、PyBullet）、多智能体或大规模连续动作空间上进行验证，结论泛化性有待进一步测试。
- **不确定性量化方法简单**：使用贝叶斯线性回归作为输出层，对于深度网络不确定性估计的有效性可能不如更先进的贝叶斯方法（如MC Dropout、深度集成）。
- **超参数依赖**：时间常数τ、距离衰减λ、耦合强度κ等需要调谐，虽为可学习参数，但初始设置影响训练稳定性。
- **潜在偏差**：Atari 100k中部分游戏需要双环配置或中性动作特殊处理，设计过程可能引入了对游戏特性的适应性，存在一定过拟合风险。

（完）
