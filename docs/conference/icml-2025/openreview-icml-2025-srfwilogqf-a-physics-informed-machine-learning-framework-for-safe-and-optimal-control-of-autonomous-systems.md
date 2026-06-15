---
title: A Physics-Informed Machine Learning Framework for Safe and Optimal Control of Autonomous Systems
title_zh: 面向自主系统安全最优控制的物理信息机器学习框架
authors: "Manan Tayal, Aditya Singh, Shishir Kolathaya, Somil Bansal"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=SrfwiloGQF"
tags: ["query:aerial-arm"]
score: 4.0
evidence: 适用于自主系统的安全最优控制框架
tldr: 该论文融合约束强化学习与形式化方法（HJ可达性、控制障碍函数），提出物理信息机器学习框架，在保证安全的同时优化性能。方法在安全关键场景下提供正式安全保证，避免过度保守。虽未特定于空中机器人，但其思想和工具可直接用于无人机臂的物理交互控制。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-srfwilogqf/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1478, \"height\": 796, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-srfwilogqf/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1764, \"height\": 734, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-srfwilogqf/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 847, \"height\": 676, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-srfwilogqf/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 837, \"height\": 680, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-srfwilogqf/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1769, \"height\": 461, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-srfwilogqf/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1781, \"height\": 688, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-srfwilogqf/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1738, \"height\": 502, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-srfwilogqf/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1757, \"height\": 850, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-srfwilogqf/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1201, \"height\": 887, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-srfwilogqf/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1770, \"height\": 463, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-srfwilogqf/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1773, \"height\": 466, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-srfwilogqf/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1770, \"height\": 466, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-srfwilogqf/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1075, \"height\": 860, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-srfwilogqf/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 544, \"height\": 249, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-srfwilogqf/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1072, \"height\": 643, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-srfwilogqf/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1074, \"height\": 646, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-srfwilogqf/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1077, \"height\": 990, \"label\": \"Table\"}]"
motivation: 安全与性能在自主系统控制中常相互冲突，现有方法难以兼顾。
method: 将CRL与HJ可达性分析、CBF结合，构建联合优化框架。
result: 在安全关键场景下实现了安全与性能的平衡。
conclusion: 结合学习与形式化方法是实现安全最优控制的有效途径。
---

## Abstract
As autonomous systems become more ubiquitous in daily life, ensuring high performance with guaranteed safety is crucial. However, safety and performance could be competing objectives, which makes their co-optimization difficult. Learning-based methods, such as Constrained Reinforcement Learning (CRL), achieve strong performance but lack formal safety guarantees due to safety being enforced as soft constraints, limiting their use in safety-critical settings. Conversely, formal methods such as Hamilton-Jacobi (HJ) Reachability Analysis and Control Barrier Functions (CBFs) provide rigorous safety assurances but often neglect performance, resulting in overly conservative controllers. To bridge this gap, we formulate the co-optimization of safety and performance as a state-constrained optimal control problem, where performance objectives are encoded via a cost function and safety requirements are imposed as state constraints. 
We demonstrate that the resultant value function satisfies a Hamilton-Jacobi-Bellman (HJB) equation, which we approximate efficiently using a novel physics-informed machine learning framework. In addition, we introduce a conformal prediction-based verification strategy to quantify the learning errors, recovering a high-confidence safety value function, along with a probabilistic error bound on performance degradation. Through several case studies, we demonstrate the efficacy of the proposed framework in enabling scalable learning of safe and performant controllers for complex, high-dimensional autonomous systems.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）
- **核心问题**：自主系统中安全（safety）与性能（performance）通常是相互冲突的目标。例如，仓库机器人既需要高效导航（性能），又必须避免碰撞（安全）。现有方法难以同时兼顾两者：
  - **学习型方法**（如约束强化学习CRL）性能强但缺乏正式安全保证，因为安全以软约束形式嵌入，可能产生不安全行为。
  - **形式化方法**（如Hamilton-Jacobi可达性分析、控制障碍函数CBF）提供严格安全保证，但往往忽略性能，导致控制器过于保守（如过度缓慢）。
- **研究动机**：弥合上述两类方法的鸿沟，提出一个既能保证严格安全又能优化性能的可扩展框架。
- **整体含义**：通过将问题建模为**状态约束最优控制问题（SC-OCP）**，利用**原像图（epigraph）重构**转化为无约束问题，并用**物理信息机器学习（PIML）**高效求解高维HJB方程，最后通过**共形预测（conformal prediction）**量化学习误差，实现高置信度的安全与性能保证。

## 2. 方法论：核心思想、关键技术细节、公式或算法流程
- **核心思想**：将安全与性能联合优化转化为SC-OCP，通过原像图引入辅助变量 z（最小允许成本），将状态约束转化为辅助值函数 \(\hat{V}(t,x,z)\) 的非正约束。\(\hat{V}\) 满足一个HJB偏微分方程，用神经网络近似求解。
- **关键技术细节**：
  1. **问题形式化**：  
     原始SC-OCP：\(\min_u \int_t^T l(x) ds + \phi(x(T))\)，满足 \(g(x(s))\le 0\)。  
     原像图重构：\(V(t,x)=\min_{z\ge0} z\)，满足 \(\hat{V}(t,x,z)\le 0\)。  
     其中 \(\hat{V}(t,x,z)=\min_u \max\{C(t,x,u)-z,\; \max_{s\in[t,T]} g(x(s))\}\)。
  2. **HJB PDE**：\(\hat{V}\) 是如下PDE的唯一连续粘性解：  
     \(\min\{ -\partial_t\hat{V} - \min_u\langle \nabla_{\hat{x}}\hat{V},\hat{f}(\hat{x},u)\rangle,\; \hat{V} - g(x)\}=0\)，  
     边界条件：\(\hat{V}(T,\hat{x})=\max\{\phi(x(T))-z,\; g(x)\}\)，其中 \(\hat{x}=[x,z]^T\)。
  3. **物理信息学习**：用神经网络 \(\hat{V}_\theta\) 近似，损失函数包括PDE残差和边界条件损失，采用课程学习（curriculum learning）从终端时间往回训练。
  4. **安全验证**（共形预测）：  
     定义 \(\delta^* = \min_{\hat{x}} \{\hat{V}_\theta(0,\hat{x}) : \hat{V}^{\hat{\pi}_\theta}(0,\hat{x})\ge0\}\)，用共形预测从有限样本估计 \(\delta\)，提供 \(\ge 1-\beta_s\) 置信度下安全概率 \(\ge 1-\epsilon_s\) 的保证（Theorem 3.1）。
  5. **性能量化**（共形预测）：  
     对安全集 \(S^*\) 中的状态，计算归一化误差 \(p = |V_\theta - V^{\pi_\theta}|/C_{\max}\)，用共形预测给出高置信度下的误差上界 \(\psi\)（Theorem 3.2）。
- **算法流程**（参见Figure 1）：  
  Step 1: 训练 \(\hat{V}_\theta\)；  
  Step 2: 安全验证（Algorithm 1）得到校正值 \(\delta\)；  
  Step 3: 通过求解原像图问题 \(V_\theta(t,x)=\min_z z\) 满足 \(\hat{V}_\theta(t,x,z)\le\delta\)，并导出最优策略 \(\pi_\theta\)；  
  Step 4: 性能量化（Algorithm 2）得到误差上界 \(\psi\)。

## 3. 实验设计
- **使用的场景/数据集**：三个仿真案例，系统维度逐次增加：
  - **2D 船导航（Boat Navigation）**：船在水流中避开圆形障碍到达目标，状态2维。
  - **8D 追逃（Pursuer Vehicle tracking Evader）**：加速度驱动的追逐者避开5个障碍追踪移动逃逸者，状态8维。
  - **20D 多智能体导航（Multi-Agent Navigation）**：5个智能体（各4维状态）各自到达目标并避免相互碰撞，状态20维。
- **基准方法（Benchmark）**：
  - **CRL类**：SAC-Lagrangian、PPO-Lagrangian（OmniSafe库）、Constrained Policy Optimization (CPO)。
  - **采样优化类**：Model Predictive Path Integral (MPPI)。
  - **安全过滤类**：MPPI-CBF（船用Neural CBF，追逃用Collision Cone CBF，多智能体用Neural CBF）。
  - **网格法（仅2D船）**：Level Set Toolbox计算真值值函数。
- **评价指标**：累计成本、安全率（100%表示无状态进入失效集）、计算时间（在线和离线）。

## 4. 资源与算力
- **硬件**：11th Gen Intel Core i9-11900K @ 3.50GHz × 16 CPU，128GB RAM，NVIDIA GeForce RTX 4090 GPU。
- **训练时长**：
  - 2D 船：离线训练约122分钟（网格法需390分钟）；训练epochs：50k预训练 + 200k主训练。
  - 8D 追逃：60k预训练 + 300k主训练。
  - 20D 多智能体：60k预训练 + 400k主训练。
- **在线推理**：每步约2ms，适用于实时系统。
- **验证采样**：每个案例使用Ns=Np=300k样本进行共形验证。

## 5. 实验数量与充分性
- **实验数量**：三个不同维度和复杂度的场景，每个场景均报告了累计成本、安全率、计算时间，并与5~6种基准方法对比。附录还包含2D船与真值的MSE对比（0.36）、α-β-ϵ关系验证（Figure 9）。总实验量较为充分。
- **充分性与客观性**：
  - 所有基准使用了公开/公认的实现（OpenAI安全RL库、OmniSafe、自定义MPPI等）。
  - 超参数在附录C中详细列出，便于复现。
  - 安全性指标基于共形预测给出统计保证，且通过3M随机初始状态模拟验证了经验违反率低于理论界（Figure 9）。
  - 但**缺乏消融实验**（如不使用共形预测验证会怎样、不同网络结构的影响等），也未测试对动态不确定性（如模型误差）的鲁棒性。

## 6. 主要结论与发现
- **安全与性能可同时优化**：所提方法在所有场景下实现100%安全率，同时累计成本显著低于所有基准（例如，2D船比MPPI低32.67%，比SAC-Lag低7.5%等）。
- **可扩展性**：从2D到20D，计算时间仅亚线性增长，而网格法在8D以上不可行。
- **高置信度保证**：共形预测提供了理论验证（如 \(\beta_s=10^{-10}\) 时，安全概率≥1-0.001），且经验结果支持理论。
- **成本-安全权衡**：方法优于CRL（安全不足）和纯安全滤镜（过度保守）的折衷。

## 7. 优点
- **创新性融合**：将状态约束最优控制、原像图重构、物理信息神经网络和共形预测系统结合，首次实现高维系统下同时提供安全保证和性能优化。
- **理论保障**：提供概率性安全与性能边界，且经验上保守但有效。
- **高效可扩展**：离线训练后在线推理极快（2ms），适用于实时控制；神经网络并行化使其维度增加时计算时间增长慢。
- **实用导向**：案例涵盖运动学、动力学、多智能体，展示广泛适用性。

## 8. 不足与局限
- **模型已知假设**：论文假设动力学模型 \(f\) 已知，虽提及可学习，但未在不确定/未知动态下验证。
- **共形预测的i.i.d.假设**：安全验证和性能量化依赖于训练/校准样本为独立同分布，实际部署时可能不成立。
- **仿真环境验证**：所有实验在仿真中进行，未涉及真实硬件或噪声、延迟等现实问题。
- **缺少消融研究**：未单独分析每个组件（如原像图变换、PIML损失权重、共形预测阈值）的贡献。
- **计算资源需求**：离线训练需数小时（GPU），对于频繁更换环境/任务可能不够灵活。
- **安全保证的统计性质**：共形预测提供的是概率保证而非确定性保证，对于零容忍安全场景仍存风险。
- **未讨论在线适应**：框架假设安全约束和成本函数固定，无法应对动态变化的环境或新信息。

（完）
