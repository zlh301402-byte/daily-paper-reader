---
title: An Optimistic Algorithm for online CMDPS with Anytime Adversarial Constraints
title_zh: 具有任意时间对抗约束的在线CMDP的乐观算法
authors: "Jiahui Zhu, Kihyun Yu, Dabeen Lee, Xin Liu, Honghao Wei"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=fFgiXamW8E"
tags: ["query:aerial-arm"]
score: 4.0
evidence: 对抗性约束下的在线安全RL，可应用于机器人
tldr: 该论文提出乐观镜像下降原对偶算法（OMDPD），首次解决具有任意时间对抗约束的在线约束马尔可夫决策过程。算法实现最优遗憾量和强约束违反界限。虽未专门针对无人机，但其安全RL理论可适用于无人机臂的交互控制。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-ffgixamw8e/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1407, \"height\": 547, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ffgixamw8e/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 848, \"height\": 422, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ffgixamw8e/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1322, \"height\": 516, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-ffgixamw8e/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1748, \"height\": 370, \"label\": \"Table\"}]"
motivation: 现有安全RL方法在对抗性约束下表现不佳。
method: 使用乐观镜像下降和原对偶方法处理未知、时变的对抗约束。
result: OMDPD理论具备最优遗憾，实验验证鲁棒性。
conclusion: 该算法为动态环境中的安全RL提供了有效方案。
---

## Abstract
Online safe reinforcement learning (RL) plays a key role in dynamic environments, with applications in autonomous driving, robotics, and cybersecurity. The objective is to learn optimal policies that maximize rewards while satisfying safety constraints modeled by constrained Markov decision processes (CMDPs). Existing methods achieve sublinear regret under stochastic constraints but often fail in adversarial settings, where constraints are unknown, time-varying, and potentially adversarially designed. In this paper, we propose the Optimistic Mirror Descent Primal-Dual (OMDPD) algorithm, the first to address online CMDPs with anytime adversarial constraints. OMDPD achieves optimal regret $\tilde{\mathcal{O}}(\sqrt{K})$ and strong constraint violation $\tilde{\mathcal{O}}(\sqrt{K})$ without relying on Slater’s condition or the existence of a strictly known safe policy. We further show that access to accurate estimates of rewards and transitions can further improve these bounds. Our results offer practical guarantees for safe decision-making in adversarial environments.

---

## 论文详细总结（自动生成）

# 论文中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

在线安全强化学习（Safe RL）在自动驾驶、机器人、网络安全等动态环境中至关重要，其目标是学习最大化累积奖励同时满足安全约束的策略（建模为约束马尔可夫决策过程，CMDP）。现有方法在随机约束下能实现次线性遗憾，但面对未知、时变甚至对抗设计的约束时表现不佳。例如，在自动驾驶中交通流和天气变化、网络安全中攻防对抗都属于“任意时间对抗约束”，这要求算法在每一个回合都必须安全，不允许误差抵消（即采用强约束违反度量）。本文首次解决具有任意时间对抗约束的在线CMDP问题，提出乐观镜像下降原对偶（OMDPD）算法，在无需Slater条件或已知严格安全策略的情况下，实现了最优的遗憾和强约束违反界 $\tilde{\mathcal{O}}(\sqrt{K})$。

## 2. 论文提出的方法论：核心思想、关键技术细节

**核心思想**：结合乐观估计、镜像下降（OMD）和原对偶框架，构建一个代理目标函数，利用指数势函数（Lyapunov函数）动态追踪累积约束违反，通过“乐观预测”步和“修正更新”步交替进行策略学习，同时控制遗憾和违反。

**关键技术细节**：
- **乐观估计**：使用UCB型置信区间构建奖励和成本的乐观估计（$\tilde{r}_k, \tilde{d}_k$），以及转移核的置信集 $\mathcal{B}_k$。
- **代理目标函数**：定义 $f_k(q) = \alpha \big( -\tilde{r}_k^\top q + \Phi'(\lambda_k)[\tilde{d}_k^\top q]^+ \big) - \frac{1}{2}\|q - q_k\|^2$，其中 $\Phi(x) = \exp(\beta x)-1$ 为指数势函数，$\lambda_k$ 为对偶变量（累积违反）。
- **乐观OMD更新**：每个回合k，先求解乐观占用量 $\hat{q}_{k+1}$（预测步），再基于预测梯度求解 $q_{k+1}$（修正步）。学习率 $\eta_k$ 自适应于历史梯度变化。之后从 $q_{k+1}$ 恢复策略并执行，更新估计和置信集。
- **对偶变量更新**：$\lambda_{k+1} = \lambda_k + \alpha [\tilde{d}_{k+1}^\top q_{k+1}]^+$（随机成本）或 $[d_{k+1}^\top q_{k+1}]^+$（对抗成本）。

**理论保证**：通过引理链证明，在规划保守估计下，最优解是可行解，且算法实现 $\tilde{\mathcal{O}}(\sqrt{K})$ 遗憾和强违反。若奖励和转移可精确估计（如生成模型），遗憾可进一步改进为 $\mathcal{O}(1)$。

## 3. 实验设计

- **数据集/场景**：合成CMDP环境，状态空间 $\mathcal{S}=\{0,1,2,3,4\}$（5个离散状态），动作空间 $\mathcal{A}=\{0,1,2\}$（3个动作），回合长度 $H=5$。奖励 $r\in[0,1]^{H\times S\times A}$ 均匀采样。成本在随机设置下固定均匀采样，在对抗设置下从离散集 $\{-1.0,-0.6,-0.2,0.0,0.2,0.6,1.0\}$ 中独立采样。转移动力学由 Dirichlet(0.5) 生成。
- **Benchmark**：论文未列出具体对比方法（表1对比了其他工作的理论结果但不包含实验对比）。实验仅绘制了OMDPD算法自身在随机和对抗约束下的累积违反曲线。
- **对比方法**：未进行与其他算法的实验对比。

## 4. 资源与算力

论文未提及任何关于GPU型号、数量或训练时长等算力信息。实验环境描述仅涉及合成MDP小规模模拟，推测在普通CPU上即可完成。

## 5. 实验数量与充分性

- **实验数量**：仅一个实验场景（$K=3000$ episodes），绘制了累积违反曲线（图2）。未见多种参数设置、不同规模、消融实验或与baseline对比。
- **充分性评价**：实验设计较为有限。仅验证了算法在给定小规模合成环境下的违反增长呈次线性趋势，缺乏对遗憾的实证验证、参数敏感性分析、不同状态/动作空间规模测试、以及与其他方法的公平对比。因此实验充分性不足，主要贡献在于理论保证而非实验验证。

## 6. 论文的主要结论与发现

- 提出首个处理任意时间对抗约束的在线CMDP算法OMDPD，在不要求Slater条件或已知安全策略下，实现最优 $\tilde{\mathcal{O}}(\sqrt{K})$ 遗憾和强约束违反界。
- 当奖励和转移可精确估计（如生成模型）且奖励固定时，遗憾可降至 $\mathcal{O}(1)$。
- 实验结果（图2）验证了违反的次线性增长趋势。

## 7. 优点

- **理论创新**：首次将在线CMDP的对抗约束（不允许误差抵消的强违反）纳入统一框架，并去掉了Slater条件等强假设。
- **算法设计巧妙**：融合乐观镜像下降、指数势Lyapunov函数和自适应学习率，实现对梯度变化的利用，从而在固定奖励时达到常数遗憾。
- **边界最优性**：证明了遗憾和违反的阶为 $\tilde{\mathcal{O}}(\sqrt{K})$，与下界匹配。

## 8. 不足与局限

- **实验不充分**：仅在一个人工合成小规模环境上测试，无与现有方法的实验对比（如Müller et al., 2023; Stradi et al., 2024c），也未提供遗憾的实证结果。缺乏消融研究和参数鲁棒性分析。
- **算法复杂性**：需要维护置信集和求解占用度量优化问题，在大规模状态/动作空间下计算成本可能很高。
- **假设局限**：虽然去除了Slater条件，但仍依赖状态和动作空间离散且有穷（finite countable）；转移核、奖励、成本边界假设（[0,1]或[-1,1]）在真实应用中需验证。
- **反馈模式差异**：对抗成本设置下要求全成本向量反馈（full-information），而奖励为bandit反馈，这种不对称假设在部分实际场景可能不成立。
- **缺乏对遗憾上界中常数项和隐藏项（如SAH项）的实证评估**，理论界可能在实际规模下较大。

（完）
