# 04 英文论文写作技巧

英文数学建模论文的核心目标不是展示复杂词汇，而是在有限篇幅内让评委迅速理解“研究了什么、为什么这样建模、模型是否可信、结论能否用于决策”。优秀论文应同时满足四项要求：结构清楚、逻辑闭合、表达准确、结果可验证。写作时应优先使用简洁、客观、可复现的学术英语，避免逐字翻译中文、堆砌形容词以及只讲方法不讲结果。

## 01_Summary

###  Summary 结构

国际数学建模竞赛中，Summary 通常是评委最先阅读、也可能是决定是否继续细读的部分。它不是 Introduction 的缩写，而是一篇能够独立成立的“微型论文”，应完整回答以下问题：

1. 研究对象和核心任务是什么？
2. 针对每项任务采用了什么模型或方法？
3. 得到了哪些关键、可量化的结果？
4. 如何验证模型的可靠性？
5. 模型具有什么实际意义或推广价值？

最常见且稳妥的是**五段式结构（Five-Part Structure）**。篇幅通常控制在一页以内。语言上以一般现在时描述论文内容和模型性质，以一般过去时描述已经完成的实验，以数字和指标代替空泛评价。

#### （1）第一部分：研究背景（Background）

第一段用于交代问题发生的现实场景，并指出为什么值得研究。一般控制在 **2～3 句话**，内容包括研究背景、实际矛盾和建模目标，不应写成百科式介绍。

推荐逻辑为：

> 现实背景 → 关键矛盾 → 决策或建模需求

例如：

> Urban traffic congestion has become a major challenge for rapidly growing cities, causing substantial time loss, energy consumption, and emissions. An effective signal-control strategy is therefore needed to balance traffic efficiency and environmental sustainability.

其中，`has become` 引出持续存在的问题，`is therefore needed` 自然过渡到研究需求。不要在此处展开历史沿革，也不要使用无法证明的绝对表述，如 `the most serious problem in the world`。

#### （2）第二部分：问题概括（Problem Statement）

这一部分应对赛题进行抽象和重组，而不是逐句翻译。应识别各小问背后的数学任务，例如预测、评价、优化、分类、仿真或决策，并说明任务之间的关系。

例如：

> This paper develops an integrated framework to estimate future demand, optimize resource allocation under capacity constraints, and evaluate the robustness of the resulting policy.

如果任务较多，可写：

> Specifically, we address four interrelated tasks: demand forecasting, risk assessment, allocation optimization, and policy evaluation.

不推荐写：

> Problem 1 asks us to predict... Problem 2 asks us to optimize...

这种写法只是复述题面，没有体现作者对问题结构的理解。更好的做法是用 `Based on the estimated demand...`、`The prediction is then used as an input to...` 等衔接语说明任务依赖关系。

#### （3）第三部分：模型介绍（Methodology）

这是 Summary 的主体。通常按照“任务—方法—关键设计—用途”的顺序介绍，每项任务用一至两句。应写明模型名称，但不要在摘要中展开推导。

基本模板为：

> For the first task, we construct a [model] to [purpose], in which [key factor] is incorporated to account for [reason].

> Based on the resulting estimates, a [model/algorithm] is developed to [purpose] subject to [major constraints].

例如：

> First, we construct a gradient-boosting regression model to forecast hourly demand, with lagged demand, weather conditions, and calendar effects used as predictors. Based on the forecasts, we formulate a multi-objective mixed-integer programming model that minimizes operating cost and unmet demand subject to capacity and service-level constraints.

模型名称必须与正文一致。若模型经过改进，应具体说明改进对象，如 `an entropy-weighted TOPSIS model`、`a rolling-horizon optimization framework`，避免无依据地使用 `novel`、`groundbreaking` 或 `perfect`。

#### （4）第四部分：结果展示（Results）

优秀 Summary 必须包含关键结果。结果应与赛题任务一一对应，并尽量给出数值、单位、比较基准和评价指标。只有“模型效果很好”不构成有效信息。

推荐表达：

> The forecasting model achieves an RMSE of 8.37 and reduces the error by 12.6% relative to the baseline model.

> Under the optimized scheme, total cost decreases from USD 1.24 million to USD 1.02 million, while the service coverage remains above 95%.

> When the key parameter varies by ±10%, the objective value changes by less than 3.2%, indicating satisfactory robustness.

报告结果时应注意：

- 百分比必须说明是相对变化还是百分点变化；
- 指标方向必须正确，例如 RMSE 越小越好，$R^2$ 越大通常表示拟合度越高；
- 避免仅报告训练集结果，应优先报告验证集、测试集或样本外表现；
- 优化结果应同时报告目标值与关键约束是否满足；
- 不应在摘要中引入正文未出现的新指标或新结论。

#### （5）第五部分：总结（Conclusion）

最后一段用于概括模型的综合价值，包括决策意义、适用条件和可推广性。表述应建立在结果之上，不要重复前文所有数字。

例如：

> The proposed framework provides a transparent and robust decision-support tool for urban traffic management. With problem-specific data and constraints, it can be adapted to other resource-allocation settings involving uncertain demand.

如果模型存在明确边界，可用一句话体现严谨性：

> The conclusions are most applicable to systems with demand patterns and capacity constraints comparable to those considered in this study.

### Summary 常用句式

##### 背景与目标：

- `Motivated by ..., this study investigates ...`
- `The central challenge is to balance ... against ...`
- `We develop an integrated framework for ...`
- `This paper aims to quantify ..., predict ..., and optimize ...`

##### 方法与衔接：

- `We first preprocess the data by ...`
- `To capture the nonlinear relationship between ... and ..., we employ ...`
- `The estimated results are subsequently incorporated into ...`
- `Subject to ..., the model determines ...`
- `The model is solved using ..., and its performance is evaluated through ...`

##### 结果与验证：

- `The results show that ...`
- `Compared with the baseline, the proposed method reduces ... by ...`
- `Cross-validation yields a mean ... of ...`
- `Sensitivity analysis confirms that ... remains stable when ...`
- `These findings suggest that ...`

### Summary 优秀案例

> Increasing uncertainty in regional water supply makes it difficult to maintain a reliable balance between consumption, ecological demand, and operating cost. This paper develops an integrated forecasting and optimization framework for long-term water-resource planning.
>
> We first clean the historical records and construct a seasonal gradient-boosting model to predict sector-level demand. The forecasts are then incorporated into a multi-objective linear programming model that minimizes total cost and water shortage while satisfying supply, capacity, and ecological-flow constraints. An entropy-weighted compromise method is used to select a balanced solution from the Pareto set.
>
> On the test set, the forecasting model achieves a mean absolute percentage error of 6.8%, outperforming the seasonal baseline by 14.2%. The selected allocation plan reduces expected shortage by 21.5% and cost by 8.7% relative to the current policy. Under ±10% perturbations in demand and unit cost, all essential constraints remain satisfied and the composite objective changes by less than 4.1%.
>
> The framework links prediction, optimization, and robustness evaluation in a transparent decision process. It can be adapted to other regions by updating local demand data, supply limits, and policy preferences.

这个案例的优点在于：任务链条完整，模型与任务对应，结果具有基准和指标，灵敏度分析支持可靠性结论，最后说明了推广时需要更新的条件。

### Summary 常见错误

1. **只写背景，不写结果。** 摘要应优先让位于方法和结论。
2. **照抄题目。** 应概括数学任务，而非逐句翻译题面。
3. **罗列模型名称。** 必须说明每个模型解决什么问题以及模型之间如何衔接。
4. **使用空泛形容词。** 将 `excellent`、`reasonable` 替换为具体指标或验证结果。
5. **结果没有比较对象。** `accuracy reaches 90%` 不足以证明改进，应给出基线或误差范围。
6. **时态混乱。** 论文内容常用一般现在时，具体实验过程和已获得的数据结果可用一般过去时。
7. **缩写未定义。** 首次出现时写全称，如 `mean absolute percentage error (MAPE)`。
8. **摘要与正文不一致。** 模型名、参数、数据范围和数值结论必须逐项核对。

## 02_Introduction

Introduction 的任务是把读者从现实问题引导到本文的建模方案。推荐结构为：背景与矛盾、问题重述、建模挑战、总体思路、主要贡献和文章结构。它应比 Summary 更充分，但仍需避免无关的宏观叙述。

### 背景介绍写法

背景部分应遵循“由宽到窄”的漏斗结构：先交代应用场景，再聚焦决策困难，最后提出需要解决的核心问题。事实性陈述若来自外部资料，应给出可靠来源；常识性背景不必堆积引用。

推荐模板：

> [Phenomenon] has created growing pressure on [system/stakeholder]. In practice, decision makers must determine [decision] while accounting for [conflicting factors]. This challenge is complicated by [uncertainty/nonlinearity/data limitation].

例如：

> The rapid growth of electric vehicles has increased the demand for accessible charging infrastructure. Planners must determine station locations and capacities while balancing construction cost, user convenience, and grid limitations. The problem is further complicated by spatially uneven and time-varying demand.

避免使用 `Nowadays, with the rapid development of society...` 这类信息量过低的套话。第一段结束时，读者应能明确知道决策者是谁、需要做什么决策、面临什么冲突。

### 问题重述写法

问题重述不是翻译题目，而是将自然语言任务转化为数学对象。应明确输入、输出、目标、约束和任务关系。例如：

> Given historical demand, geographic information, candidate sites, and budget limits, we seek to (1) estimate future spatial demand, (2) determine station locations and capacities, and (3) assess the robustness of the plan under uncertain growth rates.

重述时不应提前假定尚未论证的模型，也不要遗漏题目中的时间范围、空间范围、资源限制或评价要求。若某些概念存在歧义，应在假设部分给出操作性定义。

### 本文思路概括

总体思路应体现建模流程，而不是简单列出算法。常见完整流程为：

> 数据理解与预处理 → 特征或指标构建 → 子模型建立 → 模型求解 → 验证与比较 → 灵敏度或情景分析 → 决策建议

推荐表达：

> Our framework consists of three stages. First, we preprocess the raw data and identify the major drivers of demand. Second, we estimate future demand and feed the predictions into a capacitated location-allocation model. Finally, we evaluate the solution through out-of-sample testing, sensitivity analysis, and alternative policy scenarios.

若有创新点，应说明“改进了什么机制、解决了什么困难”，而不是只称模型新颖。例如：

> Unlike a static allocation model, our rolling-horizon formulation updates decisions as new demand information becomes available.

### 文章结构说明

结构说明放在 Introduction 末尾，通常一段即可：

> The remainder of this paper is organized as follows. Section 2 introduces the assumptions and notation. Section 3 presents the forecasting and optimization models. Section 4 reports the main results and validation tests. Section 5 examines sensitivity and robustness. Section 6 discusses the strengths and limitations, and Section 7 concludes with practical recommendations.

章节名称和编号必须与正文完全一致。篇幅较短时可以省略结构说明，以避免机械重复。

## 03_Assumptions_and_Notations

假设和符号的作用是划定模型边界、消除歧义并提高推导可读性。合理的假设应简化非核心因素，同时不破坏问题的主要机制。

### 假设写法

每条假设建议采用“假设内容—理由—可能影响”的结构，而非只写一句结论。

> **Assumption 1.** Demand within each planning period is represented by its expected value. This is reasonable because the available data are aggregated at the same temporal resolution. Short-term fluctuations are examined separately in the sensitivity analysis.

> **Assumption 2.** Travel cost is proportional to network distance rather than Euclidean distance. This choice better reflects actual accessibility while keeping the optimization model computationally tractable.

常见假设类别包括：

- 数据假设：缺失值机制、样本代表性、测量误差范围；
- 系统假设：研究期内规则或容量是否稳定；
- 行为假设：个体如何选择、需求如何响应价格或距离；
- 数学假设：变量连续性、独立性、分布形式或线性近似；
- 边界假设：忽略哪些次要因素以及适用范围。

避免使用 `We assume all data are accurate`。真实数据几乎不可能完全准确，更严谨的说法是：

> The reported data are assumed to be sufficiently reliable for aggregate-level analysis, and the influence of measurement error is evaluated through perturbation tests.

### 假设合理性说明

假设的合理性可以来自四类依据：题目明确给定、数据特征支持、领域常识支持、灵敏度分析表明影响有限。若假设可能显著影响结果，应将其列为局限性并进行情景分析。

判断假设质量可使用三个问题：

1. 去掉该假设后，模型是否无法识别或求解？
2. 该假设是否与数据或现实机制明显冲突？
3. 假设被轻微违反时，结论是否仍然稳定？

不要为了增加形式感而列出“忽略空气阻力”“不考虑突发灾害”等与问题无关的假设。

### 符号表写法

符号表应按参数、决策变量、中间变量和集合分类。每个符号至少说明含义，必要时注明单位、取值范围和索引。例如：

| Symbol | Definition | Unit/Domain |
|---|---|---|
| $i\in I$ | Index of demand nodes | — |
| $j\in J$ | Index of candidate facilities | — |
| $d_i$ | Predicted demand at node $i$ | users/day |
| $c_j$ | Capacity of facility $j$ | users/day |
| $x_j$ | Whether facility $j$ is selected | $\{0,1\}$ |
| $y_{ij}$ | Demand assigned from node $i$ to facility $j$ | $\mathbb{R}_{\ge 0}$ |

符号表中只列频繁使用或可能混淆的符号。局部使用一次的符号可在公式后直接定义。所有单位必须统一，货币应注明币种和价格基准，时间变量应明确分钟、小时或年份。

### 变量解释规范

变量首次出现时，应在公式前后立即解释，不能只依赖符号表。英文表述可采用：

> where $x_j$ is a binary decision variable equal to 1 if candidate site $j$ is selected and 0 otherwise; $y_{ij}$ denotes the amount of demand at node $i$ assigned to site $j$.

规范要求包括：

- 标量用斜体，小写粗体通常表示向量，大写粗体表示矩阵；
- 集合、索引、参数和决策变量避免使用同一字母；
- 同一符号在全文中保持唯一含义；
- 下标顺序与业务含义一致，如 $y_{ijt}$ 表示节点 $i$、设施 $j$、时期 $t$；
- 无量纲指标与有单位变量不能直接相加，除非先归一化或赋权；
- `probability`、`rate`、`percentage` 应明确取值是 $[0,1]$ 还是 $[0,100]$。

## 04_Model_Construction

模型建立部分应让评委能够重现从现实问题到数学表达的过程。建议每个子模型都按照“目标—输入—机制—数学表达—求解—输出”的顺序展开。

### 模型建立段落结构

一个清晰的子模型通常包含以下内容：

1. **建模目标。** 说明该模型解决哪一任务，输出将用于何处。
2. **基本思想。** 用一段自然语言解释模型为何适合当前数据和机制。
3. **变量与参数。** 定义决策量、输入量和必要的中间量。
4. **核心方程。** 给出目标函数、约束或估计方程。
5. **求解方法。** 说明算法、停止准则和关键设置。
6. **输出解释。** 说明结果怎样传递给下一子模型或支持决策。

开头示例：

> To determine the number and locations of facilities, we formulate a capacitated location-allocation model. The model minimizes the weighted sum of construction cost and user travel cost while ensuring that assigned demand does not exceed facility capacity.

这一段同时交代了模型类别、目标和核心约束，比直接写 `We use linear programming` 更有信息量。

### 公式解释写法

公式必须是论证的一部分，而不是孤立陈列。推荐采用“先解释目的—给出公式—逐项解释—说明性质”的顺序。例如：

> We minimize the total system cost, which consists of fixed construction cost and demand-weighted travel cost:
>
> $$
> \min Z=\sum_{j\in J}f_jx_j+\lambda\sum_{i\in I}\sum_{j\in J}d_i r_{ij}y_{ij},
> $$
>
> where $f_j$ is the fixed cost of opening facility $j$, $r_{ij}$ is the travel distance from node $i$ to site $j$, and $\lambda$ converts travel distance into a comparable monetary cost. The first term penalizes infrastructure expenditure, whereas the second represents user-side access cost.

约束也应说明现实含义：

> The capacity constraint
> $$
> \sum_{i\in I}d_i y_{ij}\le c_jx_j,\quad \forall j\in J,
> $$
> ensures that demand can be assigned to a site only when it is opened and that the assigned amount does not exceed its capacity.

注意事项：

- 所有公式应编号，正文用 `Equation (5)` 或 `Eqs. (5)–(7)` 引用；
- 目标函数中的权重必须说明来源、尺度和解释；
- 归一化公式必须避免分母为零；
- 概率模型需说明分布假设和参数估计方法；
- 机器学习模型需说明输入特征、目标变量、数据划分和评价指标；
- 不要把软件输出直接当作模型推导。

### 算法流程写法

算法流程应可执行、可复现。除了流程图或伪代码，还应给出输入、输出、初始化、迭代规则、停止条件和复杂度或运行设置。

英文模板：

> **Input:** cleaned dataset $D$, parameter set $\Theta$, and maximum iteration number $K$  
> **Output:** optimized decision vector $x^*$
>
> 1. Initialize a feasible solution and set $k=0$.
> 2. Evaluate the objective value and constraint violations.
> 3. Generate candidate solutions using the neighborhood operator.
> 4. Update the incumbent solution according to the acceptance rule.
> 5. Stop if the relative improvement is below $10^{-4}$ for 50 consecutive iterations or if $k=K$; otherwise return to Step 2.

如果使用随机算法，应报告随机种子、种群规模、迭代次数，并通过多次独立运行报告均值和标准差。若使用成熟求解器，应说明求解器、最优性间隙和运行环境，而不是宣称“得到全局最优”却不给证据。

### 模型递进写法

多问赛题的高分论文不是若干模型的拼接，而是一条有数据流和逻辑流的建模链。需要明确前一模型的输出如何成为后一模型的输入：

> The demand estimates obtained in Section 4.1 serve as parameters in the allocation model. To prevent forecast uncertainty from being ignored, we construct three demand scenarios using the prediction intervals and solve the allocation problem under each scenario.

常见递进关系包括：

- 描述性分析识别因素，预测模型量化未来状态；
- 预测结果进入优化模型，优化结果进入仿真模型；
- 评价模型筛选方案，敏感性分析检验排序稳定性；
- 基础模型提供基准，改进模型解决其局限；
- 确定性模型给出中心方案，鲁棒或随机模型处理不确定性。

每节结尾可用两三句小结，说明主要输出及其对下一节的作用，避免章节之间突然跳转。

## 05_Results_and_Analysis

结果部分应区分“结果是什么”和“为什么会这样”。前者是客观报告，后者是机制解释。不能只展示图表，也不能对每个数字逐项复述。

### 结果呈现方式

结果呈现应与任务和指标对应：预测任务报告误差和样本外表现，分类任务报告混淆矩阵及类别指标，评价任务报告得分和排序，优化任务报告决策变量、目标值和约束满足情况。

推荐先给核心结论，再给证据：

> The optimized plan selects Sites 3, 7, and 11, achieving a total cost of USD 1.02 million and a coverage rate of 96.4%. Table 4 shows that all capacity and budget constraints are satisfied.

模型比较应使用相同的数据划分、相同指标和相同预算。若数据不平衡，不能只报告 accuracy；应同时考虑 precision、recall、F1-score 或 AUC。预测问题应根据业务意义选择 MAE、RMSE、MAPE 或 $R^2$，并说明 MAPE 在真实值接近零时可能失真。

### 图表分析写法

每个图表都应具有独立可理解的标题、坐标轴、单位、图例和数据来源。正文采用“指向—发现—解释”三步法：

> Figure 6 compares the predicted and observed hourly demand on the test set. The model captures both the morning and evening peaks, although it slightly underestimates the highest evening peak. This deviation may result from rare event-driven demand that is not fully represented by the available predictors.

不要写 `From the figure, we can clearly see...` 后重复坐标上的所有数值。应提炼趋势、拐点、异常值、组间差异和决策含义。图表设计还应遵守：

- 折线图用于连续趋势，柱状图用于类别比较，散点图用于相关关系；
- 饼图只适合类别很少且确需表达整体占比的场景；
- 三维图若不能增加信息，应改用二维图；
- 不截断纵轴来夸大差异，若必须截断要显著标注；
- 颜色应可区分，并兼顾灰度打印和色觉障碍；
- 图题置于图下，表题置于表上，全文编号连续。

### 结果解释写法

解释应围绕模型机制和数据证据展开，而不是把相关性写成因果性。推荐结构为：

> 主要发现 → 数学或业务机制 → 与预期/基线比较 → 异常或不确定性

例如：

> Site 7 receives the largest capacity allocation because it combines high surrounding demand with short average travel distance. Although Site 11 has a higher construction cost, it is retained in the optimal solution because it covers an otherwise underserved region. This trade-off explains why the lowest-cost sites alone do not form the best network.

若结果与预期不一致，应诚实分析数据范围、参数设定、约束激活或模型偏差，而非删除异常结果。

### 现实意义分析

现实意义要把数学输出翻译成可执行建议，并明确适用条件、受益者和代价。例如：

> The results suggest that the city should prioritize Sites 3 and 7 in the first construction phase because together they cover 81% of projected demand. Site 11 can be added when the annual budget exceeds USD 0.9 million, primarily to improve geographic equity rather than total cost efficiency.

建议应避免超出模型证据。若模型只研究成本与覆盖率，就不能直接断言方案必然提高公众满意度。政策建议最好同时说明实施顺序、触发条件和需要监测的指标。

## 06_Sensitivity_Analysis

灵敏度分析用于检验参数变化是否导致结论显著改变。它回答的是“参数改变时输出怎样变化”，而鲁棒性更强调“在一组不确定条件下，方案是否仍可接受”。两者相关但不能混为一谈。

### 灵敏度分析写法

首先选择真正重要且存在不确定性的参数，如需求增长率、目标权重、成本系数、折现率或阈值。基本步骤为：

1. 设定基准参数和合理变化范围；
2. 每次改变一个参数，或采用全局采样同时改变多个参数；
3. 重新计算目标值、决策变量和关键约束；
4. 比较输出的变化幅度、趋势和方案结构；
5. 解释哪些参数最敏感以及管理含义。

局部灵敏度可定义为弹性：

$$
S_{y,p}=\frac{\Delta y/y}{\Delta p/p},
$$

其中 $p$ 为参数，$y$ 为输出。$|S_{y,p}|>1$ 表示输出相对变化大于参数相对变化。对于非线性或交互作用明显的模型，宜采用 Monte Carlo、Latin hypercube sampling、Sobol 指数等全局方法。

### 参数扰动说明

扰动范围必须有依据，可来自历史波动、置信区间、题目设定或专家范围。不要机械地对所有参数都使用 ±10%。

推荐表达：

> Based on the historical variation observed from 2018 to 2024, the annual demand-growth rate is varied from 2% to 8%, with 5% used as the baseline. All other parameters are held constant in the one-at-a-time analysis.

若同时扰动多个参数，应说明采样分布、样本数和相关性假设：

> We generate 5,000 scenarios using Latin hypercube sampling. Demand growth follows a truncated normal distribution, whereas unit cost follows a triangular distribution. Their rank correlation is set to 0.35 based on the historical data.

### 结果稳定性解释

稳定性不能只凭曲线“看起来平滑”来判断。应定义判据，例如：

- 目标值变化不超过预设容忍度；
- 最优方案的核心决策不变；
- 排名的 Spearman 相关系数保持在某阈值以上；
- 关键约束在绝大多数情景中仍满足；
- 预测误差在不同数据划分中保持一致。

示例：

> When the demand-growth rate varies from 3% to 7%, the selected sites remain unchanged and total cost varies by less than 4.6%. Once the rate exceeds 7%, Site 9 must be added to maintain the 95% coverage requirement. Thus, the current plan is stable under moderate demand uncertainty, but an expansion trigger should be set near a 7% growth rate.

这种表述不仅说明稳定范围，还识别了阈值及相应决策。

### 图表表达方式

单参数分析可使用折线图、龙卷风图或二维热力图；多参数和随机情景可使用箱线图、置信带、概率分布图或响应面。图中应标注基准值、可接受区间和关键阈值。

正文分析示例：

> As shown in Figure 9, the objective value is most sensitive to demand growth and relatively insensitive to maintenance cost. The sharp increase beyond a growth rate of 7% occurs because the capacity constraint becomes binding and an additional facility must be opened.

不要只报告“结果变化很小，因此模型稳定”。应说明变化量、稳定区间、最敏感参数以及结构变化的原因。

## 07_Strengths_and_Weaknesses

本节不是自我表扬或自我否定，而是对方法适用性进行客观审计。优缺点应具体对应模型设计、数据、验证和应用边界。

### 优点写法

优点最好采用“设计特征—带来的价值—证据”的结构。例如：

> **Integration of prediction and optimization.** The framework passes out-of-sample demand estimates directly to the allocation model, avoiding the inconsistency of treating future demand as known. Scenario tests further show that the selected plan remains feasible under moderate forecast errors.

可从以下方面总结：

- 机制合理：关键现实约束被明确建模；
- 数据处理充分：缺失、异常、尺度和共线性得到处理；
- 方法匹配：模型复杂度与任务、样本量相适应；
- 结果可解释：变量、权重和决策之间关系清楚；
- 验证完整：具有基线比较、样本外验证或敏感性分析；
- 可迁移：明确指出更换数据和参数后可用于哪些相似问题。

避免写 `Our model is highly accurate and perfect`。应改为：

> The model achieves a test-set MAPE of 6.8% and consistently outperforms three benchmark methods.

### 缺点写法

缺点要真实但可控，说明它可能造成的影响和适用边界：

> The demand model relies on annual aggregate data and therefore cannot capture short-term event-driven fluctuations. Consequently, the allocation results are more suitable for strategic planning than for real-time operation.

高质量局限性通常涉及：

- 数据覆盖范围有限或存在测量偏差；
- 某些行为关系被简化为线性或静态关系；
- 参数依赖历史环境，遇到结构突变可能失效；
- 求解算法只保证近似最优；
- 未显式考虑某类不确定性、公平性或动态反馈。

不要写会直接摧毁全文可信度的句子，如 `The data may be completely wrong` 或 `The assumptions are unrealistic`。也不要列出与模型无关的泛泛缺点。

### 改进方向写法

每项改进应与前述局限一一对应，并说明需要新增什么数据或方法：

> With access to hourly mobility records, the demand component could be extended to a spatiotemporal model. A distributionally robust formulation could then incorporate forecast uncertainty without assuming a precisely known probability distribution.

有效改进方向包括增加数据粒度、引入动态决策、构造鲁棒优化、加入公平约束、采用因果识别、开展外部验证等。不要只写 `More factors will be considered in future work`。

### 避免减分的表达方式

建议使用审慎、证据导向的表达：

- 用 `performs well under the tested scenarios`，不用 `works well in all situations`；
- 用 `provides an approximate solution`，不用 `finds the global optimum`，除非有理论或求解器证明；
- 用 `is associated with`，不用 `causes`，除非完成因果识别；
- 用 `suggests`、`indicates`，不用 `proves`；
- 用 `the model does not explicitly account for...`，不用 `the model ignores reality`；
- 用 `can be extended by...`，不用 `can easily solve any similar problem`。

## 08_Conclusion

Conclusion 应回答“我们做了什么、发现了什么、这意味着什么”。它不能只是 Summary 的复制，也不应在此处引入新模型、新数据或未经分析的新结论。

### 结论总结

推荐按照“目标—方法—核心发现—可靠性—意义”的顺序写两至四段：

> This study develops an integrated forecasting and optimization framework for regional charging-station planning. A gradient-boosting model is used to estimate spatial demand, and a capacitated multi-objective model determines station locations and sizes under budget and grid constraints.
>
> The forecasting model achieves a test-set MAPE of 6.8%. Compared with the current plan, the optimized solution reduces total cost by 8.7% while increasing demand coverage to 96.4%. Sensitivity analysis shows that the selected sites remain unchanged for demand-growth rates between 3% and 7%.
>
> These results demonstrate that combining demand uncertainty with explicit operational constraints can produce a more reliable infrastructure plan.

结论中的数字应精选最能回答赛题的三至五项，不要把结果表完整搬过来。

### 政策建议

政策建议必须由模型结果直接支持，并尽可能包含行动主体、优先级、条件和监测指标。例如：

> We recommend that the municipal authority construct Sites 3 and 7 in the first phase and reserve Site 11 for the second phase. Expansion should be triggered when annual demand growth exceeds 7% or when the utilization rate remains above 85% for three consecutive months.

如果涉及多目标权衡，应说明建议反映了何种偏好：

> The recommended solution is a compromise between cost efficiency and geographic equity; a decision maker placing greater weight on equity may choose the adjacent Pareto solution at an additional cost of 3.1%.

避免把模型输出包装成唯一正确政策。对价值判断或权重选择应明确说明。

### 模型推广

推广性应说明保持不变的框架和必须重新估计的部分：

> The framework can be transferred to other cities because its prediction, allocation, and robustness modules are modular. However, local demand patterns, travel networks, construction costs, capacity limits, and policy weights must be recalibrated before implementation.

只有当问题结构相似、输入数据可获得、关键假设基本成立时，推广才合理。不要使用 `universally applicable` 等绝对表达。

### 未来工作

未来工作应从局限性自然延伸，优先选择对结论影响最大的改进：

> Future work should incorporate real-time mobility data and endogenous user choice into a dynamic allocation model. External validation in cities with different spatial structures would also help assess the transferability of the proposed framework.

全文结束前可用一句简洁的价值判断收束：

> Overall, the proposed framework offers a transparent basis for balancing efficiency, cost, and resilience in long-term infrastructure planning.

最终检查时，应确认 Conclusion 与 Summary、Results 的数值完全一致，建议没有超出模型范围，未来工作与已承认的局限相呼应，并且全文没有使用无法由证据支持的绝对化措辞。
