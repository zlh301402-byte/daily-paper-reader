---
title: Certifying Stability of Reinforcement Learning Policies using Generalized Lyapunov Functions
title_zh: 使用广义李雅普诺夫函数认证强化学习策略的稳定性
authors: "Kehan Long, Jorge Cortes, Nikolay Atanasov"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=N67DlqK5C4"
tags: ["query:drone-arm"]
score: 6.0
evidence: 使用李雅普诺夫函数认证强化学习策略稳定性，适用于空中机械臂动力学与控制
tldr: 强化学习策略的稳定性保证是实际应用的关键，但传统Lyapunov方法难以构造。本文利用RL值函数并结合系统动力学残差项构造广义Lyapunov函数，为线性二次型调节器问题提供了稳定性证书。该方法可扩展到一般非线性系统。该工作为安全关键控制中RL策略的部署提供了理论基础。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-n67dlqk5c4/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 687, \"height\": 425, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-n67dlqk5c4/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 674, \"height\": 421, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-n67dlqk5c4/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 473, \"height\": 381, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-n67dlqk5c4/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 404, \"height\": 379, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-n67dlqk5c4/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 478, \"height\": 379, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-n67dlqk5c4/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1453, \"height\": 382, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-n67dlqk5c4/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 650, \"height\": 483, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-n67dlqk5c4/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 646, \"height\": 481, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-n67dlqk5c4/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1268, \"height\": 166, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-n67dlqk5c4/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1295, \"height\": 261, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-n67dlqk5c4/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1489, \"height\": 205, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-n67dlqk5c4/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1112, \"height\": 176, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-n67dlqk5c4/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1095, \"height\": 216, \"label\": \"Table\"}]"
motivation: 强化学习策略缺乏稳定性保证，传统Lyapunov方法难以应用于学习策略。
method: 利用RL值函数并结合动力学残差构造广义Lyapunov函数进行稳定性认证。
result: 在LQR问题上成功构造了稳定性证书，并扩展至一般系统。
conclusion: 为RL策略在控制系统中提供稳定性保证的理论基础。
---

## Abstract
Establishing stability certificates for closed-loop systems under reinforcement learning (RL) policies is essential to move beyond empirical performance and offer guarantees of system behavior. Classical Lyapunov methods require a strict stepwise decrease in the Lyapunov function but such certificates are difficult to construct for learned policies. The RL value function is a natural candidate but it is not well understood how it can be adapted for this purpose. To gain intuition, we first study the linear quadratic regulator (LQR) problem and make two key observations. First, a Lyapunov function can be obtained from the value function of an LQR policy by augmenting it with a residual term related to the system dynamics and stage cost. Second, the classical Lyapunov decrease requirement can be relaxed to a generalized Lyapunov condition requiring only decrease on average over multiple time steps. Using this intuition, we consider the nonlinear setting and formulate an approach to learn generalized Lyapunov functions by augmenting RL value functions with neural network residual terms. Our approach successfully certifies the stability of RL policies trained on Gymnasium and DeepMind Control benchmarks. We also extend our method to jointly train neural controllers and stability certificates using a multi-step Lyapunov loss, resulting in larger certified inner approximations of the region of attraction compared to the classical Lyapunov approach. Overall, our formulation enables stability certification for a broad class of systems with learned policies by making certificates easier to construct, thereby bridging classical control theory and modern learning-based methods.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：强化学习（RL）策略在控制应用中通常缺乏稳定性保证，而经典的李雅普诺夫（Lyapunov）方法要求严格的逐点下降条件，这在面对学习策略时难以构造稳定性证书。
- **研究动机**：RL值函数是一个自然的候选，但如何将其用于稳定性认证尚不清楚。本文旨在通过引入“广义Lyapunov函数”概念，将经典的单步下降条件放松为多步加权平均下降条件，从而使得稳定性证书更易构造，桥接经典控制理论与现代学习方法的鸿沟。
- **整体含义**：本文提出了一种利用RL值函数并结合残差项构造广义Lyapunov函数的框架，能够为LQR问题以及非线性系统的RL策略提供稳定性保证，并支持联合训练控制器与稳定性证书，获得更大的认证吸引域。

## 2. 方法论

### 核心思想
- 基于两个关键观察：
  1. 在LQR问题中，可以通过在值函数上添加一个与系统动力学和阶段成本相关的二次残差项来获得Lyapunov函数。
  2. 经典的Lyapunov下降条件可以放松为广义条件：仅要求多个时间步上的加权平均值下降（允许中间步骤的暂时上升）。
- 将这一思路推广到非线性系统：采用神经网络来表示残差项和状态相关的步权重，联合训练以最小化广义下降条件的违反损失。

### 关键技术细节
- **广义Lyapunov函数定义**（Definition 4.1）：存在整数 M>0 和状态相关非负权重 σ₁(x),…,σ_M(x) 满足平均权重 ≥1，且对于所有非零点，加权平均 V 在 M 步上比当前 V 严格减小。
- **LQR情形的LMI条件**（Theorem 4.4）：通过引入辅助二次函数 S₀ 和比较矩阵 S_i，得到一组线性矩阵不等式（LMI），当满足特定条件时，组合函数 V(x) = J*_γ(x) + (1/ϖ)xᵀS₀x 是一个广义Lyapunov函数，并可得到比经典方法更低的折扣因子下界。
- **非线性系统的方法**（Section 5）：
  - 候选函数：V(x;θ₁) = J^{πRL}_γ(x) + φ(x;θ₁)，其中 φ 为神经网络残差，并加入正定项确保原点处为零。
  - 步权重网络 σ(x;θ₂) ∈ R^{M}_{≥0}，输出经 softmax 缩放使得平均权重为1。
  - 损失函数：L = (1/N) Σ ReLU( F(x_k) )，其中 F(x_k) = (1/M)Σ σ_i V(x_{k+i}) - (1-ᾱ)V(x_k)，ᾱ∈(0,1) 为预设衰减参数。
- **联合训练控制器与证书**（Section 6）：
  - 将经典一步Lyapunov下降替换为广义多步条件，并引入稳定性损失 L_stab 和区域损失 L_region，通过约束优化最大化子水平集 S 的体积。
  - 训练后使用 α-β-CROWN 验证器进行形式验证，确认条件在域内成立。

## 3. 实验设计

- **使用的环境/场景**：
  - 两个标准RL基准：Gymnasium 的 Inverted Pendulum Swingup；DeepMind Control Suite 的 Cartpole Swingup。
  - 联合训练部分使用三个系统：Inverted Pendulum、Path Tracking、2D Quadrotor（6D状态空间）。
- **Benchmark**：对比了经典一步Lyapunov方法（M=1）与多步方法（M=2, M=3）的证书性能。
- **对比的方法**：
  - 对于固定策略证书：使用了PPO、SAC、TD-MPC等不同RL策略。
  - 对于联合合成：引用先前工作（Yang et al., 2024）的框架，并在其基础上替换为广义下降条件。
- **评估指标**：
  - 验证条件满足的比例。
  - 认证区域（ROA）体积（通过蒙特卡洛采样估计）。
  - 验证时间（秒）。

## 4. 资源与算力

- **文中说明**：所有实验在单台配备 NVIDIA RTX 4090 GPU、AMD Ryzen 9 7950X CPU、64 GB RAM 的工作站上运行。
  - 训练 Lyapunov 证书：Inverted Pendulum 约 40 分钟，Cartpole 约 4 小时。
  - 联合训练与验证：验证时间随 M 增大而增加（例如 M=1 约11.7秒，M=3 约39.2秒对于 Pendulum；2D Quadrotor 最大达5628.6秒）。
- **未说明**：未详细说明联合训练所需的超参数搜索算力消耗，但论文指出通过网格搜索选择固定步权重。

## 5. 实验数量与充分性

- **实验组数**：
  - 固定策略证书：两个环境 + 多个RL策略组合，表1展示10,000个测试状态（Pendulum）和1,000,000个（Cartpole），结果均为100%满足条件；表2展示了步权重分布。
  - 联合合成：三个系统 × 3种M值（1,2,3）各重复10次随机种子，报告均值和标准差（表3）。
- **充分性评价**：
  - 实验覆盖了线性（LQR示例）和非线性场景，涵盖了不同复杂度（从2D到6D状态）。
  - 对比了经典单步与多步方法，并展示了M增加带来的体积增益。
  - 实验设计相对客观，使用了标准基准和复现性细节。
  - 但仍有一定局限性：未包含高维系统（如人形机器人）或随机扰动场景。

## 6. 主要结论与发现

- **理论贡献**：首次证明通过将RL值函数与残差项结合并采用广义多步下降条件，可以更有效地构造稳定性证书。
- **LQR情形**：多步LMI方法能显著降低可认证的折扣因子下界（例如从0.8090降至0.6229，并随着M增大趋近于真值1/3）。
- **非线性RL策略**：在Inverted Pendulum和Cartpole Swingup任务中，训练后的广义Lyapunov函数能够成功认证稳定性，而经典方法往往失败。
- **联合合成**：多步训练得到的认证吸引域（ROA）体积显著大于经典单步方法（例如Inverted Pendulum: M=3时的89.2 vs M=1时的42.9）。验证时间随M增加而增加，但体积收益可观。
- **步权重学习**：权重主要集中在后半段（60-100%），表明网络学会容忍初期非单调变化而确保整体下降，这体现了广义条件的灵活性。

## 7. 优点

- **方法新颖**：提出将值函数与残差项结合构造广义Lyapunov函数，巧妙地利用RL已有的值函数，减少从零学习的难度。
- **理论扎实**：对LQR情形给出严格的LMI条件，并证明广义Lyapunov函数能保证渐近稳定性（定理4.2、6.2）。
- **实验全面**：覆盖多个RL策略、多个环境，并包含形式化验证（α-β-CROWN），强化了结果的可信度。
- **实用价值**：提供了开源代码，方法能直接应用于现有RL策略，降低稳定性认证的门槛。
- **效率提升**：相比于经典单步方法，广义方法能够认证更大的吸引域，且训练开销可接受。

## 8. 不足与局限

- **固定M值**：认证窗口长度M在训练时固定，如何自动确定最小必要M尚未解决。
- **高维系统**：未在人形机器人或灵巧手等高维系统上验证，可能存在扩展性挑战。
- **形式验证计算负担**：对于M>1，验证时间显著增加（尤其是6D quadrotor达到数千秒），可能限制实时应用。
- **状态依赖权重未完全验证**：虽然理论支持状态相关权重（如神经网络输出），但在联合合成部分实际使用了固定权重，未验证状态相关权重下的形式验证可行性；在固定策略证书部分使用了网络输出的权重，但形式验证仅针对联合部分。
- **假设限制**：假设平衡点已知且为原点；需要系统动力学函数已知（或可用差分模型）以进行多步滚动；对于随机策略仅使用确定性模式，未考虑随机性。
- **实验充分性**：消融实验较少，例如未比较不同残差网络结构和权重学习方法的影响；未与基于数据驱动的Lyapunov学习方法（如Chang et al., 2019）直接比较ROA体积。
- **偏差风险**：训练数据采样方式可能影响证书泛化，未讨论对未见状态的外推能力。

（完）
