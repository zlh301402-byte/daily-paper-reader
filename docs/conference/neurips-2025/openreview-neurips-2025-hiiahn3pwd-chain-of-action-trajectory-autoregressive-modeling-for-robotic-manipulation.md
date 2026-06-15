---
title: "Chain-of-Action: Trajectory Autoregressive Modeling for Robotic Manipulation"
title_zh: 行动链：用于机器人操控的轨迹自回归建模
authors: "Wenbo Zhang, Tianrun Hu, Hanbo Zhang, Yanyuan Qiao, Yuchu Qin, Yang Li, Jiajun Liu, Tao Kong, Lingqiao Liu, Xiao Ma"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=hiiaHn3pWd"
tags: ["query:aerial-arm"]
score: 7.0
evidence: 用于机器人操控的轨迹自回归建模，可迁移至空中机械臂
tldr: 现有策略预测动作的方法缺乏对整体轨迹的全局结构把握。本文提出行动链（CoA），一种基于轨迹自回归建模的视觉运动策略范式，通过显式地反向推理任务目标来生成完整轨迹。该方法采用自回归结构，首令牌编码目标关键帧，后续令牌条件生成。实验表明CoA在多种操控任务中实现了高效准确的轨迹生成。该工作为机器人操控提供了一种全局到局部的策略学习新思路。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-hiiahn3pwd/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 696, \"height\": 315, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hiiahn3pwd/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1454, \"height\": 548, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hiiahn3pwd/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1154, \"height\": 570, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hiiahn3pwd/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1439, \"height\": 616, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hiiahn3pwd/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1013, \"height\": 280, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hiiahn3pwd/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 997, \"height\": 330, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hiiahn3pwd/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1405, \"height\": 209, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hiiahn3pwd/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 857, \"height\": 470, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hiiahn3pwd/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 506, \"height\": 471, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-hiiahn3pwd/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 649, \"height\": 593, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hiiahn3pwd/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 615, \"height\": 502, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hiiahn3pwd/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1452, \"height\": 663, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hiiahn3pwd/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 338, \"height\": 214, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hiiahn3pwd/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 313, \"height\": 193, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hiiahn3pwd/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 735, \"height\": 647, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hiiahn3pwd/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1356, \"height\": 677, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hiiahn3pwd/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1450, \"height\": 190, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hiiahn3pwd/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1312, \"height\": 2192, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hiiahn3pwd/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 705, \"height\": 477, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hiiahn3pwd/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 926, \"height\": 738, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hiiahn3pwd/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 917, \"height\": 770, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hiiahn3pwd/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 934, \"height\": 746, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hiiahn3pwd/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1170, \"height\": 665, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hiiahn3pwd/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 500, \"height\": 554, \"label\": \"Table\"}]"
motivation: 现有动作预测方法缺乏全局轨迹结构，局部动作可能偏离整体目标。
method: 提出行动链（CoA），通过反向推理任务目标生成完整轨迹，采用自回归结构。
result: 在多种机器人操控任务中实现高效准确的轨迹生成。
conclusion: CoA为机器人操控提供了一种全局到局部的策略学习范式。
---

## Abstract
We present Chain-of-Action (CoA), a novel visuomotor policy paradigm built upon Trajectory Autoregressive Modeling. Unlike conventional approaches that predict next step action(s) forward, CoA generates an entire trajectory by explicit backward reasoning with task-specific goals through an action-level Chain-of-Thought (CoT) process. This process is unified within a single autoregressive structure: (1) the first token corresponds to a stable keyframe action that encodes the task-specific goals;  and (2) subsequent action tokens are generated autoregressively, conditioned on the initial keyframe and previously predicted actions. This backward action reasoning enforces a global-to-local structure, allowing each local action to be tightly constrained by the final goal. To further realize the action reasoning structure, CoA incorporates four complementary designs: continuous action token representation; dynamic stopping for variable-length trajectory generation; reverse temporal ensemble; and multi-token prediction to balance action chunk modeling  with global structure. As a result, CoA gives strong spatial generalization capabilities while preserving the flexibility and simplicity of a visuomotor policy. Empirically, we observe that CoA outperforms representative imitation learning algorithms such as ACT and Diffusion Policy across 60 RLBench tasks and 8 real-world tasks.

---

## 论文详细总结（自动生成）

# 论文总结：Chain-of-Action: Trajectory Autoregressive Modeling for Robotic Manipulation

## 1. 核心问题与整体含义（研究动机和背景）

- **现有范式缺陷**：当前主流的 visuomotor policy（如 ACT、Diffusion Policy）采用前向预测范式，即基于当前观测“向前”预测下一步动作。这种直觉方式存在根本性问题：训练目标仅优化单步预测准确性，而非确保长期任务成功，导致执行过程中**累积误差**逐渐偏离目标。
- **核心挑战**：如何在保持端到端训练简便性的同时，显式注入**全局任务目标**约束，使每个局部动作与最终意图对齐，从而提升空间泛化能力和抗分布偏移能力。
- **整体意义**：本文提出从“前向生成”转向“反向生成”的新范式——从任务目标（关键帧动作）开始向后推理生成完整轨迹，从根本上改变动作建模的因果结构，为解决长期规划与复合误差问题提供了全新思路。

## 2. 方法论：核心思想、关键技术细节

### 核心思想
- **反向自回归建模**：将轨迹生成过程反转——首令牌为任务关键帧动作（keyframe action），随后自回归地生成前序动作，形成一条从目标到当前状态的动作链。这强制实现了“全局→局部”的结构，每个局部动作受最终目标紧密约束。
- **统一框架**：全部过程在一个 Transformer 编解码器内完成，无需额外的分层规划器或中间模态。

### 关键技术细节（四大组件）
1. **连续动作令牌表示**：避免离散化引入的精度损失；同时引入**潜在一致性损失** $ \|\hat{x}_t - f_{enc}(a_t)\| $ 来正则化连续潜空间，防止误差在自回归中累积。
2. **多令牌预测（MTP）**：在训练时，解码器最后 K 层各自预测未来第 k 步动作，增强局部连续性；推理时移除。
3. **动态停止机制**：根据当前预测动作与执行状态的欧氏距离自动终止生成，支持变长轨迹输出，无需离散 EOS 令牌。
4. **反向时间集成**：针对反向生成设计集成策略——以关键帧为锚点对齐多条反向轨迹并求均值，提升闭环执行稳定性。

### 算法流程（文字描述）
- **训练**：从专家演示中采样子轨迹（当前步到下一个关键帧），观测取自初始步。动作序列经编码后反转顺序，输入解码器。损失包括动作回归损失和潜在一致性损失。
- **推理**：以 SOS 令牌为初始查询，迭代预测前序动作，直到动态停止条件满足。输出完整反向轨迹，再正向执行。

## 3. 实验设计

### 数据集/场景
- **模拟环境**：RLBench（基于 CoppeliaSim），7 自由度 Franka Emika Panda 机器人，4 个 RGB 摄像头（128×128）。
- **真实世界**：Fetch 机器人（7 自由度臂 + 移动基座），单 RGB 摄像头（640×480 缩放至 224×224），8 个厨房操作任务。

### Benchmark 与对比方法
- **主 benchmark**：自建的 **RLBench-60**（60 个多样化任务），对比 ACT 和 Diffusion Policy。
- **辅助对比**：RLBench-10 与 Octo 对比；RLBench-18 与 3D 方法（PerAct、3D Diffuser Actor、RVT-2）对比。
- **训练数据**：每个任务 100 条演示，评价 25 次。

## 4. 资源与算力

- **GPU**：单块 NVIDIA H100 GPU 训练每个任务（附录 D）。
- **训练迭代**：CoA 和 ACT 为 20,000 次，Diffusion Policy 为 100,000 次，Octo 为 2,000 次。
- **未明确**：每任务具体训练时长（小时数）、总 GPU 时数未报告。

## 5. 实验数量与充分性

- **实验数量充分**：共涵盖 60 个模拟任务主对比、2 个辅助子集对比、空间泛化深入分析（插值/外插、方差相关性、注意力可视化）、5 组消融实验、8 个真实世界任务。
- **公平性**：CoA 与 ACT 共享几乎相同架构和训练配置，仅改变建模范式，对比客观。
- **不足**：未报告误差棒或统计显著性检验（如 95% 置信区间），且单次运行（无随机种子重复）可能削弱结论稳健性。

## 6. 主要结论与发现

- **性能提升显著**：CoA 在 RLBench-60 上平均成功率 0.552，较 ACT（0.389）提升 16.3%，较 DP（0.326）提升 23.2%。在 81.7% 的任务上优于 ACT，80.0% 的任务上优于 DP。
- **空间泛化更强**：在空间插值和外插测试中，CoA 性能下降幅度远小于前向方法；与任务空间方差的相关性分析显示 CoA 对分布偏移更鲁棒。
- **注意力分析验证**：解码器自注意力图显示明显的链式依赖和长期关键帧关注，证明模型执行了全局→局部的结构化推理。
- **消融确认每个组件必要**：反向顺序、潜在一致性损失、MTP 头数、反向集成均对性能有显著贡献。

## 7. 优点

1. **创新性范式**：提出反向自回归生成，直接解决前向预测的“短视”根本问题，思想简洁有力。
2. **组件设计完整**：四项技术合理解决连续空间自回归的稳定性、变长生成、集成策略等实际难点，形成完整可部署方案。
3. **实验全面深入**：不仅在大规模 benchmark 上领先，还通过空间泛化分析和注意力可视化揭示原因，说服力强。
4. **架构兼容性**：CoA 可兼容现有视觉编码器，易于推广到 VLA 模型等扩展场景。
5. **实际验证**：在真实机器人上取得 15% 绝对提升，证明泛化性。

## 8. 不足与局限

1. **关键帧依赖**：当前依赖启发式规则（夹爪状态变化、关节速度近似零）分割轨迹，对复杂/连续任务可能不通用；作者也指出未来需学习无监督关键帧。
2. **与 3D 方法差距**：在 RLBench-18 上，CoA（37.33%）仍远低于 3D 方法（RVT-2 平均 81.4%），说明在需要精确 3D 感知的任务上仍受限于 RGB-only 输入。
3. **统计报告不足**：未提供误差棒、置信区间或多随机种子平均，削弱结果可靠性。
4. **计算效率未深入**：虽提及单 H100 训练，但推理速度、模型参数量、内存占用等细节缺失。
5. **任务覆盖偏重桌面操作**：未涉及移动操作、动态环境或接触丰富任务，泛化边界尚不清晰。

（完）
