---
title: "PlaySlot: Learning Inverse Latent Dynamics for Controllable Object-Centric Video Prediction and Planning"
title_zh: PlaySlot：学习逆潜在动态以实现可控的对象中心视频预测与规划
authors: "Angel Villar-Corrales, Sven Behnke"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=P9gwpJDo8i"
tags: ["query:aerial-arm"]
score: 4.0
evidence: 以对象为中心的视频预测与规划，可用于空中机械臂运动规划
tldr: 针对机器人规划依赖带标签数据的问题，提出PlaySlot模型。该模型从无标签视频中学习对象表征和潜在动作，并用于未来状态预测与规划。实验表明该方法能生成多种可能未来并实现可控规划，为空中机械臂的预测与路径规划提供了无监督方案。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-p9gwpjdo8i/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 865, \"height\": 594, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-p9gwpjdo8i/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1769, \"height\": 812, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-p9gwpjdo8i/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1787, \"height\": 601, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-p9gwpjdo8i/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 861, \"height\": 449, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-p9gwpjdo8i/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 833, \"height\": 849, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-p9gwpjdo8i/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 841, \"height\": 719, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-p9gwpjdo8i/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 853, \"height\": 992, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-p9gwpjdo8i/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 857, \"height\": 757, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-p9gwpjdo8i/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1720, \"height\": 506, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-p9gwpjdo8i/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1767, \"height\": 532, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-p9gwpjdo8i/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1786, \"height\": 595, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-p9gwpjdo8i/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1764, \"height\": 1085, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-p9gwpjdo8i/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1768, \"height\": 1647, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-p9gwpjdo8i/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1769, \"height\": 1911, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-p9gwpjdo8i/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1735, \"height\": 1768, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-p9gwpjdo8i/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1732, \"height\": 2207, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-p9gwpjdo8i/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1761, \"height\": 914, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-p9gwpjdo8i/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1753, \"height\": 1385, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-p9gwpjdo8i/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1690, \"height\": 2209, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-p9gwpjdo8i/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1760, \"height\": 1569, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-p9gwpjdo8i/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1715, \"height\": 1768, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-p9gwpjdo8i/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1781, \"height\": 335, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-p9gwpjdo8i/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 859, \"height\": 457, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-p9gwpjdo8i/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 879, \"height\": 278, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-p9gwpjdo8i/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 742, \"height\": 290, \"label\": \"Table\"}]"
motivation: 现有视频预测模型依赖精确动作标注，难以利用大量无标签数据。
method: 提出PlaySlot，从无标签视频中推断对象表征和潜在动作，并用于预测和规划。
result: 在多个视频预测和规划任务中，PlaySlot有效生成了准确且可控的未来帧。
conclusion: 无监督学习对象动态能有效支持机器人的预测与规划。
---

## Abstract
Predicting future scene representations is a crucial task for enabling robots to understand and
interact with the environment. However, most existing methods rely on videos and simulations
with precise action annotations, limiting their ability to leverage the large amount of avail-
able unlabeled video data. To address this challenge, we propose PlaySlot, an object-centric
video prediction model that infers object representations and latent actions from unlabeled
video sequences. It then uses these representations to forecast future object states and video
frames. PlaySlot allows the generation of multiple possible futures conditioned on latent actions,
which can be inferred from video dynamics, provided by a user, or generated by a learned action
policy, thus enabling versatile and interpretable world modeling. Our results show that PlaySlot
outperforms both stochastic and object-centric baselines for video prediction across different environments. Furthermore, we show that our inferred latent actions can be used to learn robot behaviors sample-efficiently from unlabeled video
demonstrations. Videos and code are available on our project website.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：大多数现有视频预测和世界模型方法依赖于带有精确动作标注的视频或仿真数据，限制了其利用大量无标签视频数据的能力。机器人等领域需要能够在无监督情况下从视频中学习场景动态、并支持可控预测与规划的模型。
- **整体含义**：本文提出 PlaySlot，一种面向对象的可控视频预测模型，能够从无标签视频中自动推断对象表示（slots）和潜在动作，并利用这些表示预测未来对象状态和视频帧，从而构建可解释、可控制的通用世界模型，并支持高效的行为学习。

## 2. 方法论：核心思想、关键技术细节

- **核心思想**：采用对象中心的表示（对象槽），结合逆动力学模块从连续帧中推断潜在动作，再利用条件对象中心预测器基于历史槽和潜在动作自回归预测未来对象状态和帧。
- **关键技术细节**：
  - **场景解析模块**：使用 SAVi（Kipf et al., 2022），通过槽注意力将单帧分解为 NS 个 DS 维对象槽，递归更新并解码为对象图像和掩码，通过加权求和重建帧。
  - **逆动力学模块 (InvDyn)**：
    - 输入连续两帧的对象槽，输出潜在动作向量。
    - 提出两种变体：InvDyn S（单智能体）使用 Transformer 编码器整合所有槽到一个潜在动作；InvDyn M（多智能体）使用共享 MLP 为每个槽输出独立潜在动作。
    - 潜在动作采用混合参数化：离散动作原型（通过向量量化 VQ 得到）+ 连续可变性嵌入，平衡控制性和表达能力。
  - **条件对象中心预测器 (cOCVP)**：基于 Transformer 编码器，输入历史槽、动作原型和可变性嵌入（投影相加），自回归预测下一时刻的对象槽。
  - **训练流程**：三个阶段：① 训练 SAVi 进行对象分解（重建损失）；② 冻结 SAVi，联合训练 InvDyn 和 cOCVP（包含帧重建损失、槽回归损失、向量量化损失）；③ 训练行为策略 fπ 和行为解码器 Da（模仿学习）。
- **公式/算法流程（文字说明）**：
  - 槽注意力更新：通过交叉注意力在槽和图像特征之间，槽维归一化竞争，经 GRU 和残差 MLP 更新。
  - 逆动力学：InvDyn S 将槽和 [ACT] token 输入 Transformer，输出高斯分布参数；潜在动作定义为相邻帧动态分布差值，再经 VQ 得到原型和可变性。
  - 预测过程：cOCVP 将历史信息和动作投影相加并加入时间位置编码，输出未来槽，自回归循环。

## 3. 实验设计

- **数据集/场景**：
  - **ButtonPress**（MetaWorld）：Sawyer 机器人按红色按钮，非对象中心任务，有复杂纹理。
  - **BlockPush**（MuJoCo）：机器人桌面推块到目标，测试关系推理和碰撞建模。
  - **GridShapes**：2D 形状在网格上随机移动（1~5 个对象），测试多智能体预测。
  - **Sketchy**：真实世界机器人数据集，机械手与物体交互。
- **Benchmark**：所有模型均用 6 帧种子预测后续 8 帧（评估 15 帧），使用 PSNR、SSIM、LPIPS 指标。
- **对比方法**：
  - 对象中心基线：SlotFormer、OCVP
  - 随机视频预测：SVG-LP
  - 可播放视频生成：CADDY
  - 控制性基线：使用真实动作的 Oracle 等。
  - 公平性：平衡参数数量（见表 3）。

## 4. 资源与算力

- 明确说明：模型使用 PyTorch 实现，在单个 NVIDIA A100 GPU 上训练。
- 训练细节：SAVi 训练 batch size 64，序列长度 8，学习率 1e-4，梯度裁剪 0.05；InvDyn 和 cOCVP 联合训练 batch size 64，学习率 2e-4，梯度裁剪 0.05；未报告总训练时长（小时/天）。

## 5. 实验数量与充分性

- **实验组数**：包含主定量实验（表 1，4 个数据集× 5+ 方法），定性对比（图 3，多组），消融实验（表 2：动作表示对比；图 4：多对象数量影响；表 4：动作原型数量），行为学习实验（图 7 两个环境× 多数据量× 对比方法），附录中还有更多定性结果和与 LAPO 的对比。
- **充分性分析**：实验覆盖多种场景（仿真和真实）、多对象数量、动作表示变体、下游任务（行为学习），对比方法类型全面。消融设计合理（连续 vs 离散 vs 混合 vs Oracle），公平性有参数控制。结论有统计（多个随机种子显示标准差）。整体充分、客观、公平。

## 6. 主要结论与发现

- PlaySlot 在 BlockPush 和 GridShapes 上显著优于所有基线，在 ButtonPress 和 Sketchy 上达到或超过最好性能。
- 混合动作表示（离散原型+连续可变性）比纯连续或纯离散更好，接近 Oracle（使用真值动作）性能。
- InvDyn M 能有效扩展至多个移动对象，而 InvDyn S 和 CADDY 在多对象场景下性能下降。
- 学习到的动作原型具有语义一致性（如“向右”“向上”）。
- 从无标签视频中推断的潜在动作可用于样本高效学习机器人行为（ButtonPress 和 BlockPush），优于 CADDY 和 LAPO，且接近使用真值动作的 Oracle 模型。

## 7. 优点（方法或实验设计亮点）

- **方法亮点**：
  - 对象中心表示带来可解释性（每个槽对应一个物体，可生成分割图）和泛化性（泛化到新组合、多物体）。
  - 逆动力学模块从无标签视频中学习，不需要动作标注，扩展数据来源。
  - 混合动作参数化平衡了离散控制（可解释、可干预）和连续灵活性（建模非确定性）。
  - 支持多种预测条件方式（推断、用户提供、策略生成），使模型可用于规划。
- **实验设计亮点**：
  - 在多个不同难度和类型的数据集上评估，包括真实机器人数据。
  - 消融实验系统，对比动作表示、对象数量扩展性。
  - 下游行为学习实验验证表示的实用价值。

## 8. 不足与局限

- **局限性（论文自述 + 分析）**：
  - 场景解析模块 SAVi 对复杂真实世界对象分解能力有限，限制 PlaySlot 到简单桌面场景。
  - 潜在动作是整体的，不能解耦同时发生的多个动作（如同时移动和旋转手臂），降低精细控制。
  - 在专家演示分布与训练分布差异大时（如 BlockPush 评估集），混合动作性能低于纯连续动作，表明原型泛化性有限。
  - 未在更复杂环境（如多任务、杂乱场景）评测。
  - 计算资源仅使用单 GPU，训练未报告时间，可能在大规模数据上扩展性未知。
- **实验覆盖不足**：未测试真实机器人实际部署（仅在仿真和 Sketchy 数据上评测），行为学习仅用简单任务，未涉及复杂规划。

（完）
