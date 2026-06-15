---
title: "Off-Policy Actor-Critic for Adversarial Observation Robustness: Virtual Alternative Training via Symmetric Policy Evaluation"
title_zh: 面向对抗观测鲁棒性的离策略演员-评论家：通过对称策略评估的虚拟替代训练
authors: "Kosuke Nakanishi, Akihiro Kubo, Yuji Yasui, Shin Ishii"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=3vjsUgCsZ4"
tags: ["query:drone-arm"]
score: 6.0
evidence: 面向对抗鲁棒性的离策略RL方法，可应用于机器人臂控制的强化学习
tldr: 针对强化学习在对抗观测下的脆弱性问题，现有方法依赖于交替学习导致样本效率低下。本文提出一种离策略方法，通过虚拟替代训练和对称策略评估消除主-敌依赖，实现高效的稳健策略学习。该方法可增强机械臂等控制任务在噪声环境中的可靠性。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-3vjsugcsz4/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1731, \"height\": 889, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3vjsugcsz4/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1787, \"height\": 1051, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3vjsugcsz4/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1787, \"height\": 496, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3vjsugcsz4/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1776, \"height\": 679, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3vjsugcsz4/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 910, \"height\": 821, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3vjsugcsz4/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 909, \"height\": 784, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-3vjsugcsz4/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1775, \"height\": 1100, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3vjsugcsz4/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1247, \"height\": 717, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3vjsugcsz4/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1764, \"height\": 248, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3vjsugcsz4/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1771, \"height\": 173, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3vjsugcsz4/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1769, \"height\": 194, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3vjsugcsz4/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1770, \"height\": 186, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3vjsugcsz4/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1775, \"height\": 1004, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3vjsugcsz4/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1776, \"height\": 322, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3vjsugcsz4/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1775, \"height\": 224, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3vjsugcsz4/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1772, \"height\": 220, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3vjsugcsz4/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1776, \"height\": 198, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3vjsugcsz4/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1038, \"height\": 378, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3vjsugcsz4/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1641, \"height\": 277, \"label\": \"Table\"}]"
motivation: 强化学习容易受到输入观测的对抗扰动，现有鲁棒方法通常需要交替学习，样本效率低。
method: 提出离策略虚拟替代训练框架，通过对称策略评估解耦主-敌交互，支持经验回放。
result: 在多个MuJoCo控制任务上，该方法在对抗攻击下显著提升了鲁棒性，同时保持了较高的样本效率。
conclusion: 离策略鲁棒RL方法能有效抵御观测干扰，适用于物理控制系统的安全部署。
---

## Abstract
Recently, robust reinforcement learning (RL) methods designed to handle adversarial input observations have received significant attention, 
motivated by RL's inherent vulnerabilities. 
While existing approaches have demonstrated reasonable success, 
addressing worst-case scenarios over long time horizons 
requires both minimizing the agent's cumulative rewards for adversaries and training agents to counteract them through alternating learning. 
However, this process introduces mutual dependencies between the agent and the adversary, 
making interactions with the environment inefficient and hindering the development of off-policy methods.
In this work, we propose a novel off-policy method that eliminates the need for additional environmental interactions by reformulating adversarial learning as a soft-constrained optimization problem. 
Our approach is theoretically supported by the symmetric property of policy evaluation between the agent and the adversary.
The implementation is available at https://github.com/nakanakakosuke/VALT_SAC.

---

## 论文详细总结（自动生成）

### 论文详细中文总结

#### 1. 论文的核心问题与整体含义（研究动机和背景）

深度强化学习（DRL）在复杂控制任务中取得了显著成功，但研究发现其容易受到输入观测的微小对抗扰动（adversarial perturbations）的影响，导致性能急剧下降。现有针对观测鲁棒性的方法（如 ATLA、PA-ATLA）采用交替训练（alternating training）的方式，即同时训练一个智能体（victim agent）和一个最优对手（adversary），通过博弈达到鲁棒策略。然而，这种交替训练存在两个关键问题：一是对手的训练同样需要与环境交互，导致样本效率低下（相当于双倍交互次数）；二是这种相互依赖使得离策略（off-policy）方法难以应用，因为对手策略会随智能体策略更新而改变，破坏了经验回放的稳定性。

本文旨在解决上述问题，提出一种无需额外环境交互、适用于离策略演员-评论家（off-policy actor-critic）框架的鲁棒强化学习方法。

#### 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：将对抗学习重新表述为一个**软约束优化问题**（soft-constrained optimization），并通过**对称策略评估**（Symmetric Policy Evaluation）证明：对手的价值函数可以通过智能体的价值函数直接获得，从而无需显式训练对手策略。
- **关键技术细节**：
  - **软约束对手 (Soft Constrained Adversary)**：在最优对手的优化目标中引入 \(f\)-散度正则项和熵正则项，将硬约束（L∞范数球）松弛为软约束。目标函数为：
    \[
    \tilde{J}[\nu,\pi] = J[\nu,\pi] + \alpha_{\text{ent}} H(\pi\circ\nu) + \alpha_{\text{attk}} D_f(\nu\|p)
    \]
    其中 \(\nu\) 是对手分布，\(\pi\) 是智能体策略，\(p\) 是先验分布（如均匀分布），\(\alpha_{\text{ent}}, \alpha_{\text{attk}}\) 是系数。
  - **对称策略评估**：证明当对手的Q函数满足 \(Q^\nu(s,\tilde{s}) = \mathbb{E}_\pi[-Q'^\pi(s,\tilde{a})]\) 时，智能体的软最差贝尔曼算子 \(T^{\pi\nu_{\text{soft}}}\) 和对手的软最优贝尔曼算子 \(T^{\nu_{\text{soft}}_\pi}\) 互为收缩算子，且它们的值函数满足：
    \[
    V^{\nu^{\star}_{\text{soft}}}_\pi(s) = -V^{\pi\nu^{\star}_{\text{soft}}}(s)
    \]
    即对手的最优价值函数可由智能体的最差价值函数取反得到，从而无需独立训练对手。
  - **两种软优化方法**：
    1. **VALT-SOFT**：采用KL散度作为 \(f\)-散度，推导出解析解：
       \[
       \nu^{\star}_{\text{soft}}(\tilde{s}|s) = \frac{p(\tilde{s}|s) \exp\big( -\mathbb{E}_\pi[Q^\pi_\nu(s,\tilde{a})] - \alpha_{\text{ent}} H(\pi) \big) / \alpha_{\text{attk}}}{Z}
       \]
       并通过一个参数化模型 \(\nu_{\text{model}}\) 来近似该分布，通过最小化KL散度来学习。
    2. **VALT-EPS**：采用 \(\alpha\)-散度（\(\alpha \ll 1\)），近似得到最坏情况下的点质量分布与均匀分布的混合：
       \[
       \nu^{\star}_{\text{soft}}(\tilde{s}|s) \approx \begin{cases}
       \kappa_{\text{worst}} + \frac{1-\kappa_{\text{worst}}}{|\tilde{S}_\epsilon|}, & \tilde{s} = \arg\min_{\tilde{s}'\in B_\epsilon} V^\pi(s,\tilde{s}') \\
       \frac{1-\kappa_{\text{worst}}}{|\tilde{S}_\epsilon|}, & \text{otherwise}
       \end{cases}
       \]
       实际实现中，最坏状态通过PGD（投影梯度下降）近似获得。
  - **策略改进**：固定对手后，采用最大熵策略改进，损失函数为：
    \[
    \pi_{\text{new}} = \arg\min_{\pi\in\Pi} D_{\text{KL}}(\pi\circ\nu_{\text{fix}} \| \pi^{\star}_{\text{old}}\circ\nu_{\text{fix}})
    \]
    并证明改进定理（Policy Improvement Theorem）。
- **算法流程**（基于SAC框架）：
  1. 初始化智能体Q网络、策略网络、目标网络、经验回放缓冲区。
  2. 与环境交互收集数据，存储到回放缓冲区。
  3. 采样小批量数据，使用软最差贝尔曼更新（结合VALT方法）更新Q网络。
  4. 使用固定对手的改进目标更新策略网络。
  5. 自动调节熵系数。
  6. （可选）更新对手模型（VALT-SOFT）或跳过（VALT-EPS使用PGD直接计算）。

#### 3. 实验设计

- **数据集/场景**：使用OpenAI Gym MuJoCo的四个连续控制任务：HalfCheetah, Hopper, Walker2d, Ant。攻击规模分别为 \(\epsilon=0.15, 0.075, 0.05, 0.15\)（L∞范数）。
- **Benchmark与对比方法**：
  - **On-Policy方法**（PPO变体）：PPO, Robust-PPO, ATLA-PPO, PA-ATLA-PPO, WocaR-PPO。
  - **Off-Policy方法**（SAC变体）：SAC, Robust-SAC, SAC-PPO（自行实现的交替训练基线），以及本文提出的VALT-EPS-SAC和VALT-SOFT-SAC。
- **攻击方法**：包括启发式攻击（Uniform, MAD, PGD(minV/minQ), RobustSarsa）和基于学习的攻击（SA-RL, PA-AD，分别用PPO和SAC实现）。

#### 4. 资源与算力

论文在附录G中给出了计算资源与时间信息：
- 所有实验在**Tesla V100 32GB GPU**上进行。
- 训练时间（小时）示例（HalfCheetah/Hopper/Walker2d/Ant）：
  - SAC: 4.2/2.1/6.2/12.8
  - Robust-SAC: 7.7/3.7/11.2/23.4
  - SAC-PPO: 13.5/10.3/17.8/47.9
  - VALT-EPS-SAC: 9.7/4.8/14.1/30.1
  - VALT-SOFT-SAC: 10.1/5.0/14.8/31.0
- 报告了每个10k步的计算时间分解，分析指出VALT方法由于PGD计算带来额外开销，但仍在可接受范围内。

#### 5. 实验数量与充分性

- 主要实验包括四个任务上的训练曲线（图2）和完整的鲁棒性评价表格（表1），涵盖多种攻击。
- 消融实验（附录E）：
  - 有无正则化项的比较（表7）。
  - 策略评估（PE）和策略改进（PI）中是否使用对手的消融（表8、图4）。
  - 行为策略中对手比例的影响（表10、表11）。
- 实验数量较为充分，覆盖了主要对比方法和多种攻击设置；消融实验验证了各组件的必要性。但每个任务仅使用单一随机种子（median seed）报告最终结果（原文说明：从8个种子中取中位数种子，然后评估20个episode），未报告所有种子的统计显著性或区间估计，这是一个局限。

#### 6. 论文的主要结论与发现

- 本文提出的VALT方法（VALT-EPS和VALT-SOFT）在保持与SAC相当的样本效率的同时，显著提升了对抗观测下的鲁棒性，尤其在更具挑战的任务（HalfCheetah, Ant）上表现突出。
- 相比交替训练方法（ATLA-PPO、SAC-PPO），VALT无需额外环境交互，样本效率提升3-10倍（与PPO相比）或1.5-4倍（与WocaR-PPO相比）。
- 实验表明，在政策改进中引入对手是离策略方法成功的关键（消融实验显示w/o PI导致训练崩溃）；而政策评估中的对手有助于提升最差情况下的鲁棒性。
- SAC固有的最大熵框架提供了基础鲁棒性，但结合VALT后可进一步抵御更强攻击。

#### 7. 优点

- **理论创新**：提出了对称策略评估定理，从理论上证明对手价值函数可由智能体价值函数导出，从而避免显式训练对手，是解决交替训练样本低效问题的关键。
- **框架通用性**：基于软约束优化，可适配多种 \(f\)-散度，提供了两种实用变体（SOFT和EPS），适用于不同场景需求。
- **实验设计全面**：涵盖了多种主流On-Policy和Off-Policy基线、多种攻击方式，以及详细的消融实验和计算时间分析，验证了方法的有效性和效率。
- **代码开源**：提供了可复现的代码实现。

#### 8. 不足与局限

- **计算开销**：VALT-EPS需要PGD计算，VALT-SOFT需要训练对手模型（尽管不如交替训练大），但相比原始SAC仍有额外计算成本（约2-3倍时间）。
- **行为策略偏差**：论文指出“行为策略与当前策略之间的分布不匹配”是离策略鲁棒学习的挑战，虽然采用固定比例混合策略（如50:50）取得了较好效果，但缺乏自适应的矫正机制。
- **任务依赖**：不同任务对对手比例、正则化系数等超参数敏感，需要调参（如Ant任务需要50%混合，HalfCheetah需100%对手比例），尚未实现完全自动化的自适应调整。
- **实验统计性不足**：最终结果仅报告中位数种子的均值和标准差，未展示所有种子分布或进行统计显著性检验，可能不足以完全反映方法稳定性。
- **离散动作域未验证**：论文仅在连续控制任务上实验，尽管附录F讨论了离散动作域的扩展框架，但缺乏实际实验验证。
- **高维观测局限性**：在Ant（111维状态）上，VALT-SOFT在无正则化时性能退化（表7），表明对高维输入空间的对抗训练仍不稳定，依赖正则化来稳定。
- **缺乏与其他近期方法的比较**：与WocaR-RL的比较限于PPO版本，未与最新的离策略鲁棒方法（如基于风险敏感或离线RL的方法）进行直接对比（论文说明问题设定不同）。

（完）
