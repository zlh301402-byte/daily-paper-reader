---
title: "DexScale: Automating Data Scaling for Sim2Real Generalizable Robot Control"
title_zh: DexScale：自动化数据扩展以实现仿真到现实的泛化机器人控制
authors: "Guiliang Liu, Yueci Deng, Runyi Zhao, Huayi Zhou, Jian Chen, Jietao Chen, Ruiyan Xu, Yunxin Tai, Kui Jia"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=AVVXX0erKT"
tags: ["query:aerial-arm"]
score: 4.0
evidence: 面向机器人操作的仿真到现实数据扩展，适用于空中机械臂
tldr: 针对机器人操作中仿真数据与真实环境之间的差距，提出DexScale数据引擎。该引擎自动执行技能仿真与数据扩展，确保模拟技能在真实世界中的可用性。实验表明该方法显著提升了多种操作策略的泛化性能，为空中机械臂的仿真数据生成提供了可借鉴方案。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 805, \"height\": 450, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1604, \"height\": 593, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 852, \"height\": 294, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1757, \"height\": 624, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 681, \"height\": 504, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 847, \"height\": 1717, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1775, \"height\": 974, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1730, \"height\": 612, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1758, \"height\": 621, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1729, \"height\": 605, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1730, \"height\": 610, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-avvxx0erkt/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 835, \"height\": 435, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-avvxx0erkt/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1068, \"height\": 421, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-avvxx0erkt/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1638, \"height\": 239, \"label\": \"Table\"}]"
motivation: 真实机器人数据昂贵，仿真数据存在泛化差距。
method: 提出DexScale数据引擎，自动进行技能仿真与数据扩展，并集成有效性筛选机制。
result: 在多个操作任务上，使用DexScale数据训练的策略在真实世界中表现显著提升。
conclusion: 自动化仿真数据扩展能有效桥接仿真与现实的差距。
---

## Abstract
A critical prerequisite for achieving generalizable robot control is the availability of a large-scale robot training dataset. Due to the expense of collecting realistic robotic data, recent studies explored simulating and recording robot skills in virtual environments. While simulated data can be generated at higher speeds, lower costs, and larger scales, the applicability of such simulated data remains questionable due to the gap between simulated and realistic environments. To advance the Sim2Real generalization, in this study, we present DexScale, a data engine designed to perform automatic skills simulation and scaling for learning deployable robot manipulation policies. Specifically, DexScale ensures the usability of simulated skills by integrating diverse forms of realistic data into the simulated environment, preserving semantic alignment with the target tasks. For each simulated skill in the environment, DexScale facilitates effective Sim2Real data scaling by automating the process of domain randomization and adaptation. Tuned by the scaled dataset, the control policy achieves zero-shot Sim2Real generalization across diverse tasks, multiple robot embodiments, and widely studied policy model architectures, highlighting its importance in advancing Sim2Real embodied intelligence.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）
- **核心问题**：真实机器人数据采集成本高昂（设备、人力、标准化困难），仿真数据虽然可以低成本大规模生成，但存在两大瓶颈：①语义不匹配（仿真环境与目标任务场景不一致）；②仿真与现实差距（Sim2Real gap），导致仿真训练的策略难以零样本部署到真实世界。
- **研究背景**：大规模数据集是训练通用机器人控制策略的关键（如RDT、Open-VLA、ACT等），但现有真实数据集如Open X-Embodiment依赖昂贵设备。仿真生成数据（MimicGen、GenRobo等）可以无限生成，但部署成功率低。当前Sim2Real方法包括域随机化、域适应、知识蒸馏，但缺乏自动化和系统性数据扩展引擎。
- **整体含义**：提出DexScale——一个自动化数据引擎，通过集成真实数据到仿真、自动域随机化与适应、生成可扩展数据集，实现零样本Sim2Real部署，推动具身智能泛化。

## 2. 方法论：核心思想、关键技术细节、公式/算法流程
- **核心思想**：以“数据引擎”方式，将异构真实数据（场景图像、人类演示视频）投影到仿真环境，自动化生成大规模、多样化的技能轨迹数据集，使得模仿学习策略能够零样本迁移到真实世界。
- **关键技术细节**：
  - **异构数据投影**：
    - 场景投影：从RGB图像提取物体信息，匹配3D资产库（Objaverse-XL）中的“数字近亲”，构建交互式仿真场景；支持手动修正。
    - 动作-轨迹投影：从人类第一人称视频中提取手部动作和物体交互，通过关节重定向（手→机器人末端执行器，如夹爪）和3D网格/姿态联合优化，生成与物理一致的动作轨迹。
  - **环境仿真**：基于投影场景构建仿真环境，使用大语言模型（如GPT-4）辅助场景补全和配置；动作轨迹通过逆运动学（IK）和运动规划（RRT-Connect）生成，必要时支持强化学习（自动设计奖励函数）。
  - **Sim2Real数据扩展**：
    - **自动域随机化（DR）**：分为两类——
      - 动作不变DR（AI-DR）：改变不影响最优动作的无关特征（如光照、纹理），防止过拟合。
      - 语义感知DR（SA-DR）：改变影响动作的特征（如物体位姿、形状），需要策略微调（式(1)给出带约束的最优策略目标：最大化新环境下性能同时保持与原策略接近）。
    - 自动选择DR特征：利用大语言模型对DR因素排序，结合自动域随机化（ADR）算法更新参数分布p_φ(ξ)。
    - **域适应（DA）**：将观测映射到统一目标空间，包括面向对象的表示（提取物体点云）和姿态可供性表示（仅预测关键接触姿态，减少累积误差）。
  - **部署**：在扩展数据集D_DR+AR上训练模仿学习策略（ACT、扩散策略、VLA等），实现零样本部署。

## 3. 实验设计：数据集/场景、基准、对比方法
- **数据集与场景**：
  - 通用性实验：针对8种Sim2Real域差距（光照、物体纹理、桌面纹理、背景纹理、干扰物、相机位置/朝向/视场角、物体姿态、物体形状），在抓取任务和开箱任务上评测。
  - 可扩展性实验：4种任务——①物体抓取（单臂机器人Rokae SR3）；②纸箱开箱（AUBO I5）；③桌面餐具重排（双臂WidowX 250 S）；④倒水（相同平台）。每个任务使用不同模型架构：Transformer策略（抓取）、扩散策略（开箱）、VLA模型（桌布重排）。
- **基准（baseline）**：
  - 对比数据集变体：Skills Only（仅技能轨迹）、Skills+DR（仅域随机化）、Skills+DA（仅域适应） vs 完整DexScale。
  - 额外对比：手工设计的DR（根据Xie et al. 2024经验排名选择前3特征：相机朝向、桌面纹理、干扰物）。
- **评价指标**：模拟环境100次试验成功率、真实环境10次试验成功率。

## 4. 资源与算力
- **明确提及**：
  - 抓取任务训练：4台NVIDIA A800 GPU，每策略训练36小时，PyTorch 2.0.1。
  - 开箱任务训练：1台NVIDIA A100 GPU，48小时，PyTorch 2.0.1。
  - 桌面重排任务训练：1台NVIDIA A100 GPU，40,000次迭代（未明确总时长）。
- **未明确的部分**：数据生成本身（仿真环境运行）的算力消耗未提及，仅说明系统支持多线程和高性能渲染引擎。

## 5. 实验数量与充分性
- **实验数量**：
  - 通用性实验：8种域差距×4种数据集变体（Skills Only, Skills+DR, Skills+DA, DexScale）=32组条件，每组模拟100次+真实10次，共3200模拟试次+320真实试次。
  - 手工DR对比：1种条件（抓取任务），4种特征组合（1个、2个、3个特征），共4组。
  - 可扩展性实验：4种任务，每种部署在不同机器人上，展示定性结果（未报告具体成功率数字，但表3给出了成功率的示意数据？实际表3文本未在提取中显示清晰具体数字，但文字描述“一致优于基准”）。
  - 消融实验：在通用性实验中自然包含（Skills+DR vs Skills+DA vs 完整）。
- **充分性评价**：实验设计较为充分，覆盖了多种域差距类型、多种模型架构、多种机器人硬件，并进行了消融和对比。但是：
  - 真实环境试次数较少（仅10次），统计显著性可能不足。
  - 可扩展性任务缺乏量化成功率，仅给出定性结论。
  - 未对比其他Sim2Real工具（如GenAug、MimicGen等）的直接性能。

## 6. 主要结论与发现
- **DexScale显著桥接Sim2Real差距**：相比仅技能、仅DR或仅DA，完整DexScale在几乎所有域差距下成功率最高，尤其对于物体姿态和形状变化（如物体姿态：DexScale真实成功率40% vs Skills Only 10%）。
- **自动DR优于手工设计**：手工DR逐步增加特征时成功率从0.62/0.10提升至0.79/0.56，但自动DR（DexScale）达到更高（抓取任务模拟0.73-0.83，真实0.3-0.6）。
- **跨任务、跨模型、跨硬件可扩展**：在抓取、开箱、重排、倒水四种任务上均实现零样本部署，支持Transformer、扩散策略、VLA等架构，以及三种不同机器人。
- **域适应提升鲁棒性**：去除DA后，对于需要几何理解的任务（如物体姿态/形状）性能下降明显。

## 7. 优点（亮点）
- **自动化程度高**：从真实数据投影、场景构建、DR特征选择到数据扩展，全过程无需人工干预（除非场景自动生成不符合要求，提供手动调整接口）。
- **统一框架**：集成多种接入方式（RGB图像、视频、语言描述），适用多种学习算法（模仿学习、强化学习、运动规划）。
- **理论分类清晰**：将DR分为AI-DR和SA-DR，并给出形式化定义，有助于理解不同随机化对策略的影响。
- **实用性强**：在真实机器人上成功部署多个任务，且代码开源、有项目网页。
- **结构设计可复用**：面向空中机械臂等类似场景时，其“数据投影+自动扩展”方法可迁移。

## 8. 不足与局限
- **真实实验规模有限**：每种域差距仅10次真实试验，误差大；部分任务（倒水、重排）没有量化成功率。
- **未与其他Sim2Real系统直接对比**：如GenSim、RoboGen等生成式方法，或RMA等适应方法，缺乏横向基准。
- **依赖大型模型**：场景补全依赖GPT-4，DR特征排序依赖LLM，存在成本与推理延迟。
- **域适应阶段需要物体掩膜**：在真实环境下需依赖SAM2、Florence-2等模型，增加了部署复杂性。
- **未讨论长序列任务**：当前实验均为短时操作（<100步），论文结尾提到未来扩展至更复杂任务。空中机械臂场景可能涉及更长时序、动态环境，需验证。
- **失败案例分析不充分**：虽然提到四种失败模式（不可观测抓取方向、错误抓取姿态、深度预测错误、跨块抖动），但未统计频率或提出解决方案。

（完）
