---
title: Globally Optimal Policy Gradient Algorithms for Reinforcement Learning with PID Control Policies
title_zh: 基于PID控制策略的强化学习全局最优策略梯度算法
authors: "Vipul Kumar Sharma, Wesley A. Suttle, S Sivaranjani"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=wW2qRfhT9d"
tags: ["query:aerial-arm"]
score: 7.0
evidence: 强化学习结合PID控制策略用于鲁棒的轨迹跟踪和控制
tldr: 针对强化学习中的比例积分微分（PID）控制策略，提出了具有全局最优性和收敛保证的策略梯度算法。该方法结合了PID控制的跟踪性能、稳态误差消除和鲁棒性优势，在控制任务上展示了超越传统无模型RL方法的性能，为将经典控制与RL相结合提供了新思路。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1443, \"height\": 352, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1406, \"height\": 355, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 529, \"height\": 419, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 529, \"height\": 419, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 519, \"height\": 421, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 521, \"height\": 420, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 579, \"height\": 431, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 530, \"height\": 419, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 580, \"height\": 442, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 521, \"height\": 417, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 629, \"height\": 477, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 631, \"height\": 514, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 707, \"height\": 523, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 646, \"height\": 515, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 640, \"height\": 497, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 660, \"height\": 513, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 640, \"height\": 506, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 658, \"height\": 513, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 646, \"height\": 495, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 646, \"height\": 509, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 646, \"height\": 479, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 647, \"height\": 475, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ww2qrfht9d/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1508, \"height\": 1165, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-ww2qrfht9d/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 566, \"height\": 277, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ww2qrfht9d/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 472, \"height\": 276, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ww2qrfht9d/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 566, \"height\": 319, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ww2qrfht9d/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 490, \"height\": 473, \"label\": \"Table\"}]"
motivation: PID控制策略在强化学习中未得到充分利用，现有PID设计依赖启发式方法。
method: 提出具有全局最优性和收敛保证的策略梯度算法，用于PID参数化控制策略的学习。
result: 在控制任务上展示了优于传统无模型RL方法的跟踪性能和鲁棒性。
conclusion: PID参数化结合RL能实现既具理论保证又具实际性能的控制策略。
---

## Abstract
We develop policy gradient algorithms with global optimality and convergence guarantees for reinforcement learning (RL) with proportional-integral-derivative (PID) parameterized control policies. RL enables learning control policies through direct interaction with a system, without explicit model knowledge that is typically assumed in classical control. The PID policy architecture offers built-in structural advantages, such as superior tracking performance, elimination of steady-state errors, and robustness to model error that have made it a widely adopted paradigm in practice. Despite these advantages, the PID parameterization has received limited attention in the RL literature, and PID control designs continue to rely on heuristic tuning rules without theoretical guarantees. We address this gap by rigorously integrating PID control with RL, offering theoretical guarantees while maintaining the practical advantages that have made PID control ubiquitous in practice. Specifically, we first formulate PID control design as an optimization problem with a control policy that is parameterized by proportional, integral, and derivative components. We derive exact expressions for policy gradients in these parameters, and leverage them to develop both model-based and model-free policy gradient algorithms for PID policies. We then establish gradient dominance properties of the PID policy optimization problem, and provide theoretical guarantees on convergence and global optimality in this setting. Finally, we benchmark the performance of our algorithms on the controlgym suite of environments.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：PID（比例-积分-微分）控制器是工业界最广泛使用的控制策略，具有优越的跟踪性能、消除稳态误差及对模型误差的鲁棒性，但其参数整定至今仍主要依赖启发式规则，缺乏理论上的最优性和收敛性保证。同时，强化学习中的策略梯度方法（Policy Gradient, PG）虽然在LQR等经典控制问题上取得了全局最优性理论进展，但鲜有研究将其与PID参数化框架结合。
- **整体含义**：本文旨在弥合PID控制与RL策略梯度理论之间的鸿沟。通过将PID控制设计形式化为一个优化问题，并证明其目标函数满足梯度优势（gradient dominance）性质，从而首次为PID策略提供了全局最优性和收敛性保证，同时保留PID在实际应用中的固有优势。

### 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：利用命题2.1将离散时间PID最优控制问题等价转化为扩展状态空间上的LQR问题（状态 `g_t = [x_t; z_t]`，其中 `z_t` 为积分状态），从而将PID参数 `K̃ = [K_P, K_I, K_D]^T` 映射到LQR反馈矩阵 `K`。在此基础上，推导出目标函数 `J(K̃)` 关于三个PID参数的精确梯度表达式（定理3.1），进而设计模型基和模型-free两类PG算法。

- **关键技术细节**：
    - **梯度表达式**（定理3.1）：给出 `∇_{K_P} J`、`∇_{K_I} J`、`∇_{K_D} J` 的闭式解，关键项包括误差矩阵 `E_K` 和状态协方差 `Σ_K`。
    - **模型基算法 PG4PID**（算法1）：先通过系统辨识（最小二乘法）估计系统矩阵 `A`、`B`，再迭代估计 `P_K`（Riccati方程解），然后利用梯度表达式进行梯度下降。
    - **模型-free算法 PG4PI**（算法2）：针对PI控制（固定 `K_D=0`）。引入以确定性策略 `μ_K̃(g)` 为均值的高斯随机策略 `π_K̃(u|g)`，通过策略梯度定理（式17）估计梯度。梯度计算中，仅需输出矩阵 `C`，无需 `A`、`B` 知识，实现了真正的模型-free学习（推论3.3）。
- **算法流程**（文字说明）：
    - **PG4PID**：初始化PID参数 → 收集轨迹数据 → 估计 `A`, `B` → 对每个迭代步：由当前 `K̃` 通过式(6) 计算 `K` → 估计 `P_K` → 计算梯度 → 梯度下降更新各PID参数。
    - **PG4PI**：初始化 `K_P`, `K_I` → 对每个迭代步：采样初始状态 `g_0` → 按随机策略 `π_K̃` 生成N步轨迹并累计代价 `C_t` → 计算得分函数 `∇_{K_i} log π` → 利用 `C_t` 与得分函数的乘积作为梯度估计 → 更新参数。

### 3. 实验设计：数据集/场景、benchmark、对比方法

- **数据集/场景**：使用 **controlgym** 环境库中的两个线性系统：
    - **Chemical Reactor**（8维状态空间）。
    - **LA University Hospital**（48维状态空间）。两者均为跟踪问题（单位阶跃参考输入）。
- **Benchmark**：以“负代价”（即奖励）作为绩效指标；同时评估跟踪误差、状态轨迹、对模型误差的鲁棒性。
- **对比方法**：
    - **PPO**（Proximal Policy Optimization）：使用Stable-Baselines3实现，策略网络将状态映射到PID参数。
    - **LQR策略梯度方法**（文献[18]）：分别实现模型基和模型-free版本的LQR PG（零阶方法）。
    - **本文提出的**：PG4PID（模型基）、PG4PI（模型-free）。

### 4. 资源与算力

- 文中在附录A.4中说明：实验在一台**Windows笔记本**上运行，配置为 **6核 i7-8750H CPU @ 2.20GHz**、**NVIDIA GeForce RTX 2070 GPU**、**32GB RAM**。
- **未明确说明**训练总时长、单次运行时间、GPU使用细节（是否利用了GPU加速）、总计算预算等。由于是控制环境模拟，计算量相对轻量，但算力信息不够详尽。

### 5. 实验数量与充分性

- **实验数量**：
    - 对于PG4PID和PG4PI的奖励曲线：**100次独立运行**，图中给出均值和标准差。
    - 对于PPO：**4次独立运行**。
    - 消融研究：对PG4PI的噪声方差σ（0.0001至3）进行了多组测试。
    - 鲁棒性实验：添加模型误差 `||ΔA||=0.5` 进行对比。
- **充分性与公平性**：
    - 实验覆盖了两个不同维度的环境，展示了方法的可扩展性。
    - 对比了主流RL算法PPO和经典LQR，但PPO仅运行4次，统计可靠性略低于100次的主算法。
    - 消融研究覆盖了σ的合理范围，证实σ对收敛影响不大（σ<2时稳定）。
    - **不足之处**：仅使用仿真线性系统，未在真实硬件或非线性系统上验证；环境数量偏少（仅2个），结论的泛化性有限。

### 6. 论文的主要结论与发现

- **收敛速度快**：PG4PID和PG4PI均在很少的样本内（10个episode）使奖励快速收敛到接近0，即实现系统稳定和跟踪。
- **全局最优性**：理论证明PID优化问题满足梯度优势，因此算法能收敛到全局最优。
- **跟踪性能显著优于PPO和LQR**：PID策略可实现零稳态误差（完美跟踪单位阶跃），而PPO收敛慢且误差大，LQR存在非零稳态误差。
- **鲁棒性**：模型-free的PI策略对系统矩阵的微小摄动（`||ΔA||=0.5`）仍保持稳定，而模型基LQR在此扰动下失稳。
- **算法效率**：模型-free算法为一阶方法（利用策略梯度定理），优于仅能使用零阶方法的LQR零阶PG。

### 7. 优点：方法或实验设计上的亮点

- **理论贡献突出**：首次将PG全局收敛性理论扩展到PID控制框架，证明了梯度优势，给出了模型基的线性收敛率和模型-free的样本复杂度上界。
- **精确梯度推导**：提供了PID参数的闭式梯度表达式（定理3.1），为后续优化奠定基础。
- **模型-free方法创新**：通过随机策略（高斯噪声）成功实现了对确定性PI策略的模型-free学习，且仅需已知输出矩阵C，避免了完全系统辨识。
- **算法设计简洁实用**：PG4PI仅需采集轨迹和计算简单得分函数，易于实现。
- **实验对比充分**：跟踪误差、状态轨迹、鲁棒性等多角度验证；消融研究考察了关键超参数σ的影响。
- **实际意义**：弥合了控制理论与强化学习之间的鸿沟，使经典PID控制器获得了现代RL理论保障。

### 8. 不足与局限：包括实验覆盖、偏差风险、应用限制等

- **实验覆盖有限**：
    - 仅测试了两个线性控制环境，缺乏非线性系统或更高维系统的验证。
    - 无真实机器人或物理平台实验，实际应用中的噪声、时延、非理想性未考虑。
- **模型-free方法仅支持PI**：固定 `K_D=0`，无法利用微分项，限制了在全PID场景下的通用性。
- **理论假设较强**：
    - 需要输出矩阵 `C` 已知（虽合理但限制了纯黑箱场景）。
    - 收敛分析依赖局部Lipschitz性质（而非全局Lipschitz），理论推导较复杂。
    - 样本复杂度结果依赖于假设4.5（梯度方差随N衰减）和假设4.6（梯度范数有界），实践中可能需要大N或梯度裁剪。
- **偏差风险**：
    - PPO仅运行4次，统计效力不足，可能低估PPO性能。
    - 未报告超参数调优细节（如学习率、rollout长度N），复现性可能受影响。
- **应用限制**：
    - 系统需为线性、离散时间、单输入单输出（文中声称可扩展到多变量但未验证）。
    - 目标函数为二次型（LQR形式），不直接支持更复杂的目标（如约束、混合H2/H∞）。
- **算力细节缺失**：未报告训练时间、GPU使用情况，不利于计算成本评估。

（完）
