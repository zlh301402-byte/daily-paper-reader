---
title: Active Fine-Tuning of Multi-Task Policies
title_zh: 多任务策略的主动微调
authors: "Marco Bagatella, Jonas Hübotter, Georg Martius, Andreas Krause"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=hlyBdwHBeC"
tags: ["query:drone-arm"]
score: 4.0
evidence: 多任务机器人策略的主动微调，有助于机械臂控制的高效学习
tldr: 针对多任务机器人学习中的演示预算分配问题，提出AMF算法。该算法通过自适应选择信息量最大的任务进行演示收集，最大化多任务策略性能。实验表明该方法在有限演示下显著优于随机采集，为空中机械臂的多任务学习提供了高效策略。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-hlybdwhbec/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 834, \"height\": 248, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hlybdwhbec/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1779, \"height\": 528, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hlybdwhbec/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 322, \"height\": 318, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hlybdwhbec/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1738, \"height\": 1009, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hlybdwhbec/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 672, \"height\": 465, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hlybdwhbec/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 981, \"height\": 452, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hlybdwhbec/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1773, \"height\": 2301, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hlybdwhbec/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1768, \"height\": 629, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hlybdwhbec/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1412, \"height\": 626, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hlybdwhbec/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 867, \"height\": 557, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hlybdwhbec/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1412, \"height\": 515, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hlybdwhbec/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 765, \"height\": 536, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hlybdwhbec/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1765, \"height\": 468, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hlybdwhbec/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1752, \"height\": 655, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hlybdwhbec/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1439, \"height\": 1001, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hlybdwhbec/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1438, \"height\": 1002, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hlybdwhbec/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1783, \"height\": 1004, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hlybdwhbec/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1787, \"height\": 1005, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hlybdwhbec/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1732, \"height\": 448, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hlybdwhbec/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1754, \"height\": 934, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hlybdwhbec/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 878, \"height\": 1127, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-hlybdwhbec/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 851, \"height\": 503, \"label\": \"Table\"}]"
motivation: 在多任务机器人学习中，如何有限演示预算下最优分配任务是一大挑战。
method: 提出AMF算法，基于信息增益自适应选择需要演示的任务。
result: 在多种多任务环境中，AMF策略性能显著优于均匀分配和随机选择。
conclusion: 主动选择演示任务能有效提升多任务策略的样本效率。
---

## Abstract
Pre-trained generalist policies are rapidly gaining relevance in robot learning due to their promise of fast adaptation to novel, in-domain tasks.
This adaptation often relies on collecting new demonstrations for a specific task of interest and applying imitation learning algorithms, such as behavioral cloning.
However, as soon as several tasks need to be learned, we must decide *which tasks should be demonstrated and how often?*
We study this multi-task problem and explore an interactive framework in which the agent *adaptively* selects the tasks to be demonstrated.
We propose AMF (Active Multi-task Fine-tuning), an algorithm to maximize multi-task policy performance under a limited demonstration budget by collecting demonstrations yielding the largest information gain on the expert policy.
We derive performance guarantees for AMF under regularity assumptions and demonstrate its empirical effectiveness to efficiently fine-tune neural policies in complex and high-dimensional environments.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：在多任务机器人学习场景下，如何利用有限数量的专家演示预算，自适应地选择要演示的任务，以最大化微调后多任务策略的性能。
- **研究动机**：预训练的通用策略（generalist policies）在机器人领域日益重要，但其微调通常需要为新任务收集演示。当涉及多个任务时，随机或均匀地分配演示预算效率低下，尤其当预训练分布与目标任务分布不匹配时。例如，家庭机器人出厂时带有预训练策略，但用户需要机器人主动请求演示来弥补自身不足，此时应优先请求哪些任务的演示？
- **整体含义**：首次从信息论角度系统研究了多任务策略的主动微调问题，提出了可证明的收敛性保证，并扩展到了高维神经网络策略，为高效的多任务机器人学习提供了新范式。

## 2. 方法论：核心思想、关键技术细节、算法流程

- **核心思想**：基于贝叶斯观点，将专家策略视为高斯过程，利用互信息（信息增益）衡量每次演示对策略不确定性的减少量，从而自适应选择信息量最大的任务进行演示。
- **关键技术细节**：
  - **信息增益准则**：在每个交互轮次，选择任务 \( c_n \) 最大化期望条件互信息：
    \[
    c_n = \arg\max_{c'\in\mathcal{C}} \mathbb{E}\left[\sum_{t=0}^{H-1} I(\pi(s_t,c); \tau(c') \mid \text{历史数据})\right]
    \]
  - **实用近似**：由于状态占用分布未知，采用重要性采样估计期望；策略的不确定性通过核方法（GP）或神经网络的梯度嵌入（loss gradient embeddings）近似。
  - **AMF-GP**：当策略可用GP建模时，直接计算后验方差作为熵。
  - **AMF-NN**：对于神经网络策略，采用线性化近似（即用最后一层梯度作为特征，构造核函数）来估计条件熵，并利用当前策略估计重要性权重。
  - **遗忘缓解（Adaptive Prior）**：保留一个冻结的预训练策略副本（prior），学习一个任务相关的混合系数 \(\alpha(c)\)，将微调策略与prior的输出线性组合，防止灾难性遗忘。损失函数包含BC损失和保守正则项。
- **算法流程**（Algorithm 1）：
  1. 输入初始策略 \(\pi_0\)，预算 \(N\)，目标任务分布 \(\mu_c\)。
  2. 初始化空数据集。
  3. 对于 \(n=0,\dots,N-1\)：
     - 根据公式(2)（即互信息准则）计算最优任务 \(c_n\)。
     - 收集该任务的演示轨迹 \(\tau_n\)。
     - 每 \(B\) 轮进行一次策略更新（用最近数据微调神经网络）。
  4. 输出最终策略 \(\pi_N\)。

## 3. 实验设计：数据集/场景、基准、对比方法

- **实验环境**：
  - **2D Integrator**（GP实验）：点质量从原点出发，任务为到达圆上的不同目标点；连续任务空间；奖励为负欧氏距离。
  - **FrankaKitchen**：5个操作任务（开关旋钮、开关柜门、微波炉门等），状态输入和RGB图像输入。
  - **Metaworld**：4个任务（移动杯子到两个位置、打开/关闭水龙头）。
  - **Robomimic**：4个长时域、高精度操作任务（人类演示），使用扩散策略（diffusion policy）。
  - **WidowX**（Octo通用策略）：使用预训练的Octo-small模型，自蒸馏收集成功轨迹。
- **基准方法**：
  - **Uniform**：随机均匀选择任务（固定采样顺序）。
  - **Uniform with adaptive prior**：均匀任务选择加上自适应prior。
  - **Rebalancing**（特权基线）：假设知道预训练任务分布，主动平衡演示次数（仅作为参考）。
  - 不确定性估计消融：对比“Last-layer gradient”和“Last-layer Dropout”两种熵估计方式。
- **评估指标**：多任务成功率（multi-task success rate），以及单任务成功率、演示次数等。
- **预训练设置**：预训练演示数量约15个，分为“无错配”（均匀分配所有任务）和“错配”（只演示一半任务）。

## 4. 资源与算力

- 文中在附录M.4中说明：
  - AMF-NN的每次实验运行在GPU加速下最多**5小时**。
  - 数据选择本身每轮**少于1秒**。
  - AMF-GP实验可在**10分钟内**在CPU上完成。
- **未明确说明GPU型号和数量**，仅提及“with GPU acceleration”，推测为常见科研级GPU（如NVIDIA RTX 3090或A100等，但未指定）。

## 5. 实验数量与充分性

- **实验组数**：
  - GP实验：在2D integrator上测试了12种不同预训练分配（从1/12到12/12任务），每种10个随机种子。
  - 神经网络实验（AMF-NN）：在FrankaKitchen和Metaworld上测试了两种模态（状态/RGB）、两种预训练分布（错配/无错配）、多种不确定性估计方法、多种遗忘缓解方案；在Robomimic和WidowX上各测试一种设置。总共超过**20组独立实验**，每组10个种子。
  - 消融实验：不确定性估计对比（图5）、遗忘缓解对比（图12）、重要性权重分析（附录K）、单任务性能分析（附录J）等。
- **充分性评价**：
  - 实验覆盖了从低维到高维、从稀疏到稠密、从GP到神经网络、从脚本演示到人类演示、从简单MLP到扩散策略等多种场景，较为全面。
  - 各实验均重复10个随机种子，报告均值和90% bootstrap置信区间，统计严谨。
  - 对比了多种基线（uniform、rebalancing、不同不确定性估计）并控制了自适应prior变量，公平性较好。
  - 不足之处：未在更大规模通用策略（如RT-2）上进行测试，仅用Octo-small做了有限验证；缺少真实机器人实验。

## 6. 论文的主要结论与发现

- **AMF显著优于均匀采样**，尤其在预训练分布与目标分布不匹配时：错配条件下，AMF能更快提升多任务成功率，而均匀采样可能因遗忘而性能下降。
- **自适应prior有效缓解遗忘**：通过线性组合微调策略和冻结的预训练策略，任务相关权重自适应增长，避免了对已掌握任务的性能退化。
- **信息增益准则自动实现“重平衡”**：即使不了解预训练分布，AMF倾向于选择预训练中欠采样的任务或更困难的任务，与特权基线rebalancing性能相当（图14）。
- **理论保证**：在正则假设下（Lipschitz平滑、RKHS等），AMF收敛到专家策略，性能差距以 \(O(\gamma(H_n)/\sqrt{n})\) 衰减。
- **适用性广泛**：可应用于不同策略类（GP、MLP、扩散策略）和不同数据源（脚本、RL、人类演示）。

## 7. 优点：方法或实验设计上的亮点

- **理论驱动**：从信息论第一原理导出任务选择准则，并给出了完备的收敛性证明（定理4.2），这是该领域首个此类保证。
- **实用性强**：解决了神经网络策略微调中的两大挑战——不确定性估计（梯度嵌入核近似）和灾难性遗忘（自适应prior），提出了可直接应用的解决方案。
- **实验全面**：覆盖了多种环境、策略架构、预训练分布、输入模态，消融实验深入，统计可靠。
- **可复现性**：开源代码，并在附录中详细说明了实现细节（超参数、重要性采样技巧等）。

## 8. 不足与局限

- **实验覆盖局限**：
  - 未在真正大规模通用策略（如RT-2、π0）上进行评估，仅用Octo-small做了有限验证（图10），结论的泛化性有待进一步验证。
  - 所有实验均为模拟环境，真实机器人上的效果未知。
- **对不确定性估计的依赖**：AMF-NN的性能高度依赖梯度嵌入核近似的质量，但该近似在复杂策略中可能不准确；消融实验（图5）显示其他估计方法（如Dropout）效果较差，说明方法对其敏感。
- **遗忘缓解的局限性**：自适应prior假设策略输出为高斯分布，当策略为扩散策略等非参数化分布时，需要特殊处理（文中采用确定性近似）。此外，混合系数学习可能不稳定。
- **计算开销**：虽然数据选择本身很快，但每次微调需要3000步梯度更新，总体训练时长（最多5小时）可能在实际部署中受限。
- **应用限制**：仅适用于有限任务空间（文中实验为4-5个任务），对于极大规模任务空间（如数百个）的可扩展性未研究。
- **偏差风险**：信息增益准则可能偏向于初始不确定性高的任务，若某些任务虽不确定性低但权重高，可能被忽视。

（完）
