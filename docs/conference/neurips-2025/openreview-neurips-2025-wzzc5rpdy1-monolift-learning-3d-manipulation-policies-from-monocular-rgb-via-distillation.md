---
title: "MonoLift: Learning 3D Manipulation Policies from Monocular RGB via Distillation"
title_zh: MonoLift：通过蒸馏从单目RGB学习三维操作策略
authors: "Ziru Wang, Mengmeng Wang, Guang Dai, Yongliu Long, Jingdong Wang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=wZzC5rpDY1"
tags: ["query:aerial-arm"]
score: 7.0
evidence: 通过蒸馏从单目RGB学习三维操作策略
tldr: 提出MonoLift，一种三层知识蒸馏框架，从深度引导的教师模型向单目RGB学生模型转移空间、时间和动作层次知识。使学生模型能够仅使用单目RGB输入学习准确的三维操作策略，避免了深度传感器的开销和推理代价，在多种操作任务上实现了与深度教师模型相当的性能。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-wzzc5rpdy1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 722, \"height\": 542, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wzzc5rpdy1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1436, \"height\": 581, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wzzc5rpdy1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1445, \"height\": 360, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wzzc5rpdy1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 800, \"height\": 529, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wzzc5rpdy1/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1439, \"height\": 347, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wzzc5rpdy1/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1439, \"height\": 439, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wzzc5rpdy1/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1441, \"height\": 488, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-wzzc5rpdy1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1445, \"height\": 411, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wzzc5rpdy1/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 520, \"height\": 225, \"label\": \"Table\"}]"
motivation: 从单目RGB学习三维操作策略缺乏空间信息导致动作估计不准确，而深度输入引入额外开销。
method: 提出三层知识蒸馏框架，从深度引导教师模型蒸馏空间、时间和动作知识到单目RGB学生模型。
result: 在多种操作任务上仅用单目RGB达到与深度教师模型相近的性能。
conclusion: 蒸馏方法能有效从深度知识转移到单目RGB策略，实现低成本高效操作学习。
---

## Abstract
Although learning 3D manipulation policies from monocular RGB images is lightweight and deployment-friendly, the lack of structural information often leads to inaccurate action estimation. While explicit 3D inputs can mitigate this issue, they typically require additional sensors and introduce data acquisition overhead. An intuitive alternative is to incorporate a pre-trained depth estimator; however, this often incurs substantial inference-time cost. To address this, we propose MonoLift, a tri-level knowledge distillation framework that transfers spatial, temporal, and action-level knowledge from a depth-guided teacher to a monocular RGB student. By jointly distilling geometry-aware features, temporal dynamics, and policy behaviors during training, MonoLift enables the student model to perform 3D-aware reasoning and precise control at deployment using only monocular RGB input.
Extensive experiments on both simulated and real-world manipulation tasks show that MonoLift not only outperforms existing monocular approaches but even surpasses several methods that rely on explicit 3D input, offering a resource-efficient and effective solution for vision-based robotic control. The video demonstration is available on our project page: https://robotasy.github.io/MonoLift/.

---

## 论文详细总结（自动生成）

# 论文《MonoLift: Learning 3D Manipulation Policies from Monocular RGB via Distillation》详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）
- **问题**：从单目RGB图像学习三维操作策略虽然轻量、易于部署，但由于缺乏几何结构信息，导致动作估计不准确。现有方法依赖多视图、点云或RGB-D传感器，增加了硬件成本和部署复杂度；而集成预训练深度估计器虽能提供几何线索，但会引入较高推理代价。
- **动机**：能否在训练阶段利用深度估计器提供的伪深度图，通过知识蒸馏让学生模型在部署时仅使用单目RGB图像也能具备三维感知和精确控制能力，避免额外传感器和推理开销。
- **整体含义**：提出MonoLift框架，通过三级知识蒸馏（空间、时间、动作）将深度引导教师模型的能力迁移到单目RGB学生模型，实现资源高效的三维操作策略学习。

## 2. 论文提出的方法论：核心思想、关键技术细节
- **核心思想**：采用教师-学生蒸馏框架。教师模型在训练时使用RGB图像和伪深度图（由预训练深度估计器Depth Anything V2生成）进行特征融合和策略学习，学生模型仅使用RGB输入。通过三层蒸馏损失，将教师的空间理解、时间动态和动作分布知识转移到学生。
- **关键技术细节**：
    1. **空间表示蒸馏（Spatial Representation Distillation）**  
       - 教师模型：对RGB和伪深度图分别编码后，通过双路径跨模态融合模块（注意力机制和逐点平均）得到融合特征 \(F^{T}_{spa}\)。  
       - 学生模型：仅对RGB编码得到 \(F^{S}_{spa}\)。  
       - 损失：\(L_{SD} = \frac{1}{H} \sum \|F^{S}_{spa,t} - F^{T}_{spa,t}\|_2^2\)，对齐历史窗口内特征。
    2. **时间动态蒸馏（Temporal Dynamics Distillation）**  
       - 教师和学生共享Transformer解码器，对空间特征、动作token和语言token进行时序建模，输出上下文特征 \(F^{T}_{tem}, F^{S}_{tem}\)。  
       - 计算时间梯度（中心差分）\(G_t = \nabla_t F_t\)，对齐梯度：\(L_{TD} = \frac{1}{H-2} \sum \|G^S_t - G^T_t\|_2^2\)，使学生捕捉结构转变对应的运动模式。
    3. **动作分布蒸馏（Action Distribution Distillation）**  
       - 教师和学生通过MLP策略头输出高斯动作分布 \(A^T_t, A^S_t\)。  
       - 损失：\(L_{AD} = \text{KL}(A^T_t \| A^S_t)\)，使学生学习三维感知引导的动作分布。
    4. **总损失**：结合专家模仿损失 \(L_{actor}\)（最大似然）与上述蒸馏损失。
- **算法流程**（文字说明）：  
  训练时，学生和教师模型同时前向传播。教师输入RGB+伪深度，学生输入RGB。两者共享图像编码器、Transformer解码器和策略头（但教师有融合模块）。计算 \(L_{SD}, L_{TD}, L_{AD}\) 和 \(L_{actor}\)，联合优化学生网络。推理时仅使用学生模型（RGB输入），无需深度估计器。

## 3. 实验设计
- **数据集/场景**：
    - **LIBERO-90**：8个代表性任务（来自两个场景），含视觉歧义场景。
    - **Meta-World**：15个操作任务（7 easy / 5 medium / 3 hard），需精细控制。
    - **LIBERO-Long**：长时域多阶段任务。
    - **真实世界实验**：Franka Research 3机械臂，6个操作任务（按按钮、推盒子、抽纸巾、摘葡萄放盘、举杯倒水、叠毛巾），每个任务10条演示轨迹。
- **Benchmark**：与三类方法对比：
    - 单目RGB直接映射法：RT-1、MT-ACT。
    - 单目RGB隐式三维法：GROUND、MT-R3M。
    - 显式三维输入法：3D-VLA（RGB-D）、SPA（多视图RGB）。
- **对比基线**：同一实验设置，报告平均成功率及标准差。

## 4. 资源与算力
- 论文未明确说明使用的GPU型号、数量或具体训练时长。仅提及在单个GPU上训练，并指出学生模型部署效率（推理时间18.1ms，参数量8.5M）。**未给出完整算力信息**。

## 5. 实验数量与充分性
- **实验数量**：
    - 模拟环境：LIBERO-90（8任务，表1）、Meta-World（15任务，图3）、LIBERO-Long（多场景，图4）共约23+个任务。
    - 真实世界：6个任务。
    - 消融实验：三级蒸馏逐项消融（图5a）、蒸馏迁移性测试（RT-1+TriKD，图5b）、深度质量影响（三种Depth Anything版本+真实深度，图5c）。
    - 部署效率对比（表2）。
    - 各实验均报告多次运行（至少3个随机种子）的平均值和标准差。
- **充分性与客观性**：实验覆盖了不同难度、不同维度（空间歧义、精细控制、长时域、真实世界）的任务，对比基线多样且具有代表性，消融设计合理。**实验充分、客观、公平**。

## 6. 论文的主要结论与发现
- MonoLift在LIBERO-90上以80.8%平均成功率超越所有单目方法，并超过部分显式三维方法（如3D-VLA 68.7%、SPA 61.2%）。
- 在Meta-World上平均成功率达87.8%，尤其困难任务提升显著。
- 在LIBERO-Long上平均71.7%，显著优于无蒸馏变体（46.5%）和MT-ACT、RT-1。
- 真实世界实验中，MonoLift在6个任务上平均成功率高于消融变体，尤其高精度任务（按按钮100% vs 20%）。
- **三级蒸馏互补**：空间蒸馏解决状态歧义，时间蒸馏稳定过渡，动作蒸馏提供几何感知行为。
- 蒸馏方法可迁移至其他框架（如RT-1），提升性能。
- 深度估计质量越高，蒸馏效果越好；使用vitl深度估计器可达到接近真实深度训练的性能。

## 7. 优点
- **方法创新**：首次提出针对单目RGB操作策略的三级知识蒸馏框架，联合空间、时间和动作层次，克服单目缺乏结构信息问题。
- **高效部署**：仅需单目RGB输入，推理时无需深度估计器，延迟低（18.1ms）、参数量少（8.5M），适合资源受限场景。
- **实验充分**：涵盖模拟和真实环境，多种任务类型，消融和迁移性分析完备。
- **性能优异**：不仅超越同类单目方法，甚至部分超越需要显式三维输入的基线。
- **开源友好**：提供了项目页面和视频演示。

## 8. 不足与局限
- **深度估计误差未建模**：教师使用的伪深度图可能包含噪声（遮挡、反射、透明物体等），蒸馏时未考虑不确定性，可能影响复杂场景下的鲁棒性。
- **实验资源未明确**：未报告GPU型号、数量及具体训练时长，不利于复现比较。
- **真实世界任务规模有限**：仅6个任务，每任务仅10条演示，泛化性和跨任务能力有待更大规模验证。
- **对变形物体效果弱**：在“叠毛巾”任务中，MonoLift性能与消融变体差异不大（均20%），说明深度信号对非刚性物体帮助有限。
- **未与其他蒸馏方法比较**：未与针对操作的其他蒸馏策略（如隐式三维表征蒸馏）进行对比。

（完）
