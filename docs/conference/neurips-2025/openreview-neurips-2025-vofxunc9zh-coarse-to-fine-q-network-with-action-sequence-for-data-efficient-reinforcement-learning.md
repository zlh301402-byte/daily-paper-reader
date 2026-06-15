---
title: Coarse-to-fine Q-Network with Action Sequence for Data-Efficient Reinforcement Learning
title_zh: 基于动作序列的粗到细Q网络用于数据高效强化学习
authors: "Younggyo Seo, Pieter Abbeel"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=VoFXUNc9Zh"
tags: ["query:drone-arm"]
score: 7.0
evidence: 用于机器人手臂控制的强化学习
tldr: 该论文提出一种基于动作序列的粗到细Q网络（CQN-AS），通过预测动作序列的Q值来提升强化学习的数据效率。在稀疏奖励的人形控制和桌面操作任务上，CQN-AS显著优于多个基线方法，展示了其在机器人手臂控制等连续控制场景中的潜力。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-vofxunc9zh/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1393, \"height\": 445, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vofxunc9zh/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1408, \"height\": 452, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vofxunc9zh/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1401, \"height\": 441, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vofxunc9zh/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1424, \"height\": 192, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vofxunc9zh/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1433, \"height\": 1060, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vofxunc9zh/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1440, \"height\": 862, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vofxunc9zh/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1431, \"height\": 600, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vofxunc9zh/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1382, \"height\": 1122, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vofxunc9zh/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1407, \"height\": 609, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-vofxunc9zh/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1383, \"height\": 566, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vofxunc9zh/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1017, \"height\": 496, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vofxunc9zh/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1395, \"height\": 1181, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vofxunc9zh/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1409, \"height\": 821, \"label\": \"Table\"}]"
motivation: 现有强化学习算法在稀疏奖励环境中样本效率低，受行为克隆中动作序列预测的启发，提出将动作序列引入Q值学习。
method: 提出CQN-AS，训练一个输出动作序列Q值的评论家网络，显式学习执行动作序列的后果。
result: 在多种稀疏奖励的人形控制和桌面操作任务上，CQN-AS优于多个基线。
conclusion: 动作序列预测可以显著提升强化学习的数据效率，尤其适用于复杂机器人控制任务。
---

## Abstract
Predicting a sequence of actions has been crucial in the success of recent behavior cloning algorithms in robotics. Can similar ideas improve reinforcement learning (RL)? We answer affirmatively by observing that incorporating action sequences when predicting ground-truth return-to-go leads to lower validation loss. Motivated by this, we introduce Coarse-to-fine Q-Network with Action Sequence (CQN-AS), a novel value-based RL algorithm that learns a critic network that outputs Q-values over a sequence of actions, i.e., explicitly training the value function to learn the consequence of executing action sequences. Our experiments show that CQN-AS outperforms several baselines on a variety of sparse-reward humanoid control and tabletop manipulation tasks from BiGym and RLBench.

---

## 论文详细总结（自动生成）

### 中文总结

#### 1. 论文的核心问题与整体含义
- **研究动机**：在机器人领域，行为克隆算法通过预测动作序列（action sequence）显著提升了策略对多模态、噪声专家轨迹的近似能力。受此启发，论文探索在强化学习中也引入动作序列，以提高样本效率和解决稀疏奖励任务中的探索困难。
- **核心观察**：作者发现，在预测地面真实回报（return-to-go）时，以动作序列作为输入比单步动作能获得更低的验证损失。但尝试在AC算法（如SAC、TD3）中直接使用动作序列时，出现了严重的值函数高估值问题，导致性能崩溃。这是因为增大的动作空间使评论家更易受函数近似误差影响，而演员会利用该误差过度最大化Q值。
- **整体含义**：论文论证了动作序列对值学习的积极作用，并针对高维动作空间的值函数不稳定问题，提出了一种仅依赖评论家的算法——CQN-AS，在多种机器人操作任务上实现了数据高效的学习。

#### 2. 方法论
- **核心思想**：将粗到细Q网络（CQN）扩展为输出动作序列的Q值，即训练一个评论家网络显式预测执行一段连续动作的长期结果。
- **关键技术细节**：
  - **粗到细离散化**：将连续动作空间在多个层级（L层）上逐步离散化并“放大”到更高分辨率的子区间，每个层级通过选择Q值最高的bin来缩小搜索范围。
  - **动作序列Q值**：评论家为序列中的每个步骤k和每个层级l输出一个Q值向量（对应B个bin）。所有步骤的Q值并行计算，避免时序依赖。
  - **网络架构**：对每步特征使用共享MLP提取，再通过GRU聚合历史信息，最后通过共享映射层得到每个序列步骤的Q值。
  - **目标函数**：包含N步回报的TD误差，并累积所有层级和所有序列步骤的损失。使用延迟目标网络稳定训练。
  - **动作执行**：采用“时序集成”（temporal ensemble）——每一步都重新计算动作序列，并加权平均历史预测，赋予近期动作更高权重，从而生成平滑的机器人动作。
  - **训练数据**：从回放缓冲区采样时，以动作序列形式组织，对于序列末尾不足的部分用“空动作”（位置控制重复最后一步、力矩控制归零）填充。
- **算法流程**（文字说明）：
  1. 编码观察（视觉+本体），得到特征h_t。
  2. 对于每个粗到细层级l和序列步骤k，构造输入特征并经过MLP+GRU得到聚合表示。
  3. 通过线性投影输出B个bin的Q值，选择Q值最高的bin并“放大”至下一层级。
  4. 最终层级的最后一步动作构成当前环境动作，并通过时序集成平滑执行。
  5. 使用N步回报和TD损失优化所有层级与所有步骤的Q网络。

#### 3. 实验设计
- **数据集与场景**：
  - **BiGym**：25个稀疏奖励移动双臂操作任务，由人类遥控提供17–60条噪声演示。使用RGB图像（3个视角，84×84）和本体感受状态。动作模式为绝对关节位置控制，作为浮动基座（用经典控制器替代步行）。
  - **RLBench**：20个稀疏奖励桌面操作任务，使用100条通过运动规划生成的干净合成演示。使用RGB图像（4个视角，84×84）和低维状态（关节位置+夹爪状态），动作模式为增量关节位置控制。
  - **HumanoidBench**：8个稠密奖励类人运动任务（如站立、行走、跑步等），只使用低维状态（本体+任务特权信息），无演示、无辅助BC损失。
- **基准方法**：
  - **RL基线**：CQN（骨干算法）、DrQ-v2+（优化版确定性actor-critic）、SAC（HumanoidBench）。
  - **BC基线**：ACT（Transformer预测动作序列，使用时序集成）。
- **实验设置**：所有RL算法均从头开始训练，但演示驱动设置下用少量演示初始化回放缓冲区并加入辅助BC损失（CQN-AS采用大间隔BC损失，actor-critic采用L2损失）。每种条件在BiGym上运行8次、RLBench上4次、HumanoidBench上8次，报告成功率或累积回报的均值和置信区间。

#### 4. 资源与算力
- **硬件**：
  - BiGym和HumanoidBench：单张NVIDIA A5000 GPU（24GB VRAM）。
  - RLBench：单张NVIDIA RTX 2080Ti GPU。
- **训练时间**：
  - BiGym每任务（100K步）约16小时。
  - HumanoidBench每任务（10M步）约40小时。
  - RLBench每任务（30K步）约6.5小时。
- **相对开销**：CQN-AS比CQN内存增加13%、推理速度慢40%、整体训练慢约33%。

#### 5. 实验数量与充分性
- **实验数量**：共涉及53个任务（BiGym 25 + RLBench 20 + HumanoidBench 8），加上多种消融实验（动作序列长度、N步回报、时序集成开关及参数、有无RL目标等），总计超过100组独立实验。所有主实验报告了多随机种子的均值与置信区间（8或4次），随机性覆盖充分。
- **充分性评价**：
  - **覆盖全面**：涵盖了稀疏奖励、稠密奖励、人类演示、合成演示、多模态视觉/低维状态、位置控制/力矩控制等多种设置。
  - **对比公平**：与CQN保持相同超参数，与DrQ-v2+和ACT使用官方实现，仅替换关键组件（动作序列）。
  - **消融深入**：分析了动作序列长度、N步回报、时序集成、RL vs. 纯BC等关键因素，并指出了失败案例（力矩控制类人运动）。
  - **局限**：缺乏真实机器人实验，部分细小物体任务仍难以解决，扭矩控制场景表现退化。整体实验设计客观、充分，能有力支撑主要结论。

#### 6. 主要结论与发现
- **动作序列提升值学习**：在稀疏奖励的人形操作和桌面操作任务上，CQN-AS显著优于CQN、DrQ-v2+等RL基线，并在大部分任务上快速匹配并超越BC方法ACT。
- **Critic-only设计的必要性**：标准actor-critic算法在引入动作序列时会因值函数高估而失败，而CQN-AS作为纯评论家算法，避免演员利用函数近似误差，训练稳定。
- **时序集成**：帮助生成平滑动作，提升精细控制性能，但在需要快速反应的任务中可能有害。
- **N步回报敏感**：过大的N步回报引入方差，降低性能，最佳取值通常在1–4之间。
- **局限**：在扭矩控制（如DMC运动任务）上，CQN-AS表现不如CQN，作者推测因为原始扭矩序列缺乏关节位置序列的语义结构。

#### 7. 优点
- **方法创新性**：成功将行为克隆中的动作序列预测思想融入强化学习值函数，并通过离散化+crtic-only设计克服了高维动作空间的稳定性问题。
- **实验扎实**：覆盖两大主流机器人学习基准（BiGym、RLBench）及人形控制基准，与多种先进方法（CQN、DrQ-v2+、ACT、SAC）对比，消融分析详尽。
- **分析深入**：通过初步观察（图2a）揭示动作序列提升返回值预测，并通过值函数高估实验（图2b-c）解释为什么要采用critic-only架构。
- **代码开源**：提供完整代码，便于复现和进一步研究。

#### 8. 不足与局限
- **缺乏真实机器人验证**：所有实验均在仿真环境中进行，真实世界噪声、延迟和分布外情况未覆盖。
- **细小物体交互困难**：在涉及杯子、餐具等精细物体的BiGym任务上成功率很低，表明当前架构对细节感知和操控能力不足。
- **扭矩控制退化**：在关节力矩控制的任务（如DMC运动任务）上，CQN-AS反而不如基础CQN，限制了其在需要连续力控制场景的应用。
- **计算开销增加**：需同时维护多层级和序列步的Q网络，导致33%的速度下降和13%的内存增加，可能影响资源受限场景的部署。
- **超参数敏感**：动作序列长度、N步回报、时序集成系数m等对最终性能影响较大，需要针对任务调整，增加调参成本。
- **未探索更高级视觉编码器**：尝试ResNet-18但因显存和速度瓶颈无法高效运行，限制了对高维视觉输入的泛化能力。

（完）
