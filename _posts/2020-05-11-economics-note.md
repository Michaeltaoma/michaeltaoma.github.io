---
layout: post
updated: 2020-05-13 16:29
description: My Economics note
---
## Chapter 1: Analyzing Economic Problems
- Contrast the two main branches of economics—microeconomics and macroeconomics.
- *Describe the three main analytical tools of microeconomics—constrained optimization, equilibrium analysis, and comparative statics—and recognize examples of each of these tools.*
- Explain the difference between positive and normative analysis.

***Economics is the science that deals with the allocation of limited resources to satisfy unlimited human wants***

***That is why economics is often described as the science of constrained choice.***

- **Resource**
	- Labor(劳动力)
	- Managerial talent（人才管理）
	- Capital（资本）
		- 在经济学，资本， 是一种生产要素，为用于生产的耐久财，即资金、厂房、设备、材料等物质资源，用来生产其他商品或产生收入的累积物力与财务资源.
	- Raw Material
		- A raw material, also known as a feedstock, unprocessed material, or primary commodity, is a basic material that is used to produce goods, finished products, energy, or intermediate materials that are feedstock for future finished products. 

- 资本和原材料是一样的吗？原材料是资本的一部分吗？
	- 资本和原材料不一样，最大的区别在于**原材料会变成商品的一部分，而资本不会**，所以对于资本有更加精准的定义：具有以下特性的商品，即为资本：
		- 在制造其他商品时会使用到（因此是生产要素中的一项）
		- 不会变为其他商品中的一部分（和原料或半成品不同），在制造过程中也不会将此商品耗尽（不过资本会有折旧．也是企业支出的一部分）。
		- 需要经过生产制造流程才能得到（和生产要素中的“土地”不同，后者是指自然存在的资产，例如矿产）。 
	- 比如打印机本来属于资本，因为在制造其他商品时会用到，但是如果他同时是商品的一部分，那他就不是资本了

- Microeconomics: studies the economic behavior of individual economic decision makers, such as a consumer, a worker, a firm, or a manager. It also analyzes the behavior of individual households, industries, markets, labor unions, or trade associations. 微观经济学要解决的三个问题
	- What goods and services will be produced and in what quantities?
	- Who will produce the goods and services, and how?
	- Who will receive the goods and services?
- Macroeconomics: analyzes how an entire national economy performs. 所以宏观经济学的范围是卡死了，就是在国家的层面上讨论

### Three Key Analytical Tools
- 经济学模型往往会选择性的抽象化或者忽视一些生活中的细节，经济学模型只关心真正在作用的事物。
- 就和数学模型一样，经济学模型需要确定模型的输入和模型的输出
	-  **Exogenous variable**: the variable whose value is talem as given in a model. The value of an exogenous variable is determined by some process outside the model being examined. 感觉这个值跟函数的输入也不完全一样，因为作为一个函数他的输入对输出是有直接影响的，也就是说一个y之所以是y因为有这个函数模型加上这个x造成的，但这个exogenous variable可能只是众多变量的一种，并没有对结果造成影响，他的特点只有：determined outside。不过是不是只要放入了模型的，就暗示了会有影响呢？外生变量只对系统产生影响而不受系统影响
	- **Endogenous variable**: variable whose value is determined within the model being studied.也就是这个值在这个模型中决定的，可以看作是输出

#### Constrained Optimization
- 什么时候用：当决策者面对多种限制，并且需要作出决策时，这样的问题被称为Constrained Optimization Problems
- Constrained optimization problem可以被分为两部分
	- *Objective function*：The relationship that the decision maker seeks to "optimize"
		- 例子就是如果现在的问题是一个消费者想要通过购物去最大化自己的满足感。那么这里的objective function就是消费者在购买某一种商品之后他有多少满足感
		- 假设现在需要通过L和W去最大化Area（定位为LW）那么他的标识是 \\(\mathop{max}\limits_{(L,W)}(LW)\ subject\ to\ \{Set\ of\ constraint\} \\)
	- LW就是Objective Function
	- Set of constrains
- 所以其实Objective function就一个简单的目标值足矣
- 然后textbook举了个例子来阐述constrained optimization是怎样把人们从不明显的错误中给纠正过来，个人认为是废话。不过课本根据这个问题提出了经济学上的一个重要观点：***The solution to any constrained optimization problem depends on the marginal impact of the decision variables on the value of the objective function.***这句话的意思就是变量对于价值的边际影响决定了cop的答案，边际影响指得是每提高一个unit的变量，价值的改变是多少。
- 然后根据例子，处理这种多变量的constrain optimization problem的时候，我们往往考虑增加边际影响更大的变量，边际影响指明了方向
- **The term marginal in microeconomics tells us how a dependent variable changes as a result of adding one unit of an independent variable**
- **Marginal Cost**: Marginal cost measures the incremental impact of the last unit of the independent variable (output) on the dependent variable (total cost). 这个和刚刚的边际影响是相反的，这个考虑的是当价值提高一个unit，那么成本（变量）会提高多少，一般就是价格

#### Equilibrium Analysis
- 什么叫做Equilibrium，Equilibrium平衡指的是in a system is a state or condition that will continue indefinitely as long as exogenous factors remain unchanged—that is, as long as no outside factor upsets the equilibrium.
- 在一个竞争市场里面，平衡点出现在当市场clears的时候，即是需求曲线和供给曲线相交的时候
- 提出了一个很高级的说法：了解为什么系统处于平衡，帮助我们了解为什么系统不处于平衡

#### Comparative Statics
- used to examine how a change in an exogenous variable will affect the level of an endogenous variable in an economic model. 对于经济模型来说，这个模型分析方法是用来分析外生变量的变化会如何影响内生变量 
- 它主要是这么运作的：A “before and after” analysis 通过对比前后两种经济模型来得出结论
	- Initial：根据外生变量的初始值，得出内生变量的值
	- After；根据变化之后的外生变量的值，得出内生变量的值

- 所以如果是comparative statics应用在constrained optimization problem的话，他要考虑的是，当外生变量的值变化时，从外生变量中生成的最优的内生变量会如何变化，也就是改变状态会如何影响选择

#### Positive and Normative Analysis
- Positive Analysis: *attempts to explain how an economic system works or to predict how it will change over time.*他问的问题是针对现象的：当怎么怎么样，会怎么怎么样？他的关注点是后面的会发生什么
- Normative Analysis: *typically focus on issues of social welfare, examining what will enhance or detract from the common good. In so doing, they often involve value judgments.*他问的问题则是针对行为的：我们该做什么。所以认为positive analysis是normative analysis的子问题，也就是说positive analysis可以归约到normative analysis.
	- Normative economics focuses on the value of economic fairness, or what the economy "should be" or "ought to be."
- While positive economics is based on fact and cannot be approved or disapproved, normative economics is based on value judgments.
- 看到了一个反对最低工资上调的说法：上调最低工资其实是把收入转移给了没有技术的员工。如果想要把收入转移给某类人，还有一种做法是从一般税收收入中支付转移的费用。这样做有两个好处:一是将负担分摊到所有纳税人身上，二是让政客们为自己的行为负责。但是通过提高最低工资的办法，只会让这个担子全压在雇主身上，如果最低工资上调，雇主只可以多付工资，每年的成本上涨，这上涨的成本无异于前种办法的征税，唯一的区别是政策设计者可以告诉你他没有提高税收
- Positive analysis attempts to explain how an economic system works and to predict how the endogenous variables will change as exogenous variables change. Normative analysis considers prescriptive questions such as “What should be done?” Normative studies introduce value judgments into the analysis.

## Chapter 2: Demand and Supply Analysis

- Describe the **three main building blocks of supply and demand analysis**––demand curves, supply curves, and the concept of market equilibrium. 
- Analyze how changes in exogenous variables shift the demand and supply curves and thus change the equilibrium price and quantity.
- Explain the concept of **price elasticity.**
- Calculate the price elasticity of demand for specific demand curves.
- Explain how price elasticity of demand is related to total revenue.
- Discuss the factors that determine the price elasticity of demand.
- **Contrast the market-level price elasticity of demand with the brand-level price elasticity of demand.** 
- Explain and contrast **other elasticities**: the income elasticity of demand, the cross-price elasticity of demand, and the price elasticity of supply.
- Indicate why the short-run price elasticities of demand and supply may differ from the long-run price elasticities of demand and supply.  
- Use **“back-of-the-envelope”** techniques to determine key properties of demand and supply curves with only fragmentary data on prices, quantities, or elasticities.

### 2.1 Demand, Supply, and Market Equilibrium
- 目标分析市场：
	- Perfectly Competitive Market
	- 完全竞争市场comprise large numbers of buyers and sellers。
	- 存在许多的买家/卖家，所以单个的买家/卖家无法决定价格，他们只能接受市场决定的整体的价格(*price-taking*)
- 一个市场可以被以下三个维度划分：
	- Commodity: 在贩卖/购买的是什么货物
	- Geography: 市场的地点在哪里
	- Time
- **Market Demand Curve**: 就是市场需求曲线，A curve that shows us the quantity of goods that con- sumers are willing to buy at different prices. 
- **Derived Demand**: Demand for a good that is derived from the produc- tion and sale of other goods. Derived demand is demand for a factor of production or intermediate good that occurs as a result of the demand for another intermediate or final good. 也就是说derived demand这个需求是基于别的最终产品的需求上的，比如我想要的是玉米汁，但是玉米是玉米汁的原材料，所以我对玉米的需求是基于我对玉米汁的需求
- **Direct Demand**: Demand for a good that comes from the desire of buyers to directly consume the good itself. 就是我对于玉米的需求来源于我本身想要消费玉米，而像在上面举的例子里面的direct demand就是我对于玉米汁的需求
- When we draw the demand curve, we assume that all other factors that affect the quantity demanded are fixed. Demand curve只探讨价格和需求的关系
- **Law of demand**: The inverse relationship between price and quantity demanded, holding all other factors that influence demand fixed也就是价格越高，需求就越小，但是有些杠精就会跑出来说了，哎呀奢侈品就不一样，价格越高越多人喜欢，需求就更大，不过其实这样想的话，因为我们多考虑了一个变量“优越感”，优越感越高需求越大，而价格越高优越感越干，因为需求曲线只在乎价格上的影响，所以如果我们控制优越感不变，价格越高，需求还是越少的
- **Market Supply Curve**：A curve that shows us the total quantity of goods that their suppliers are willing to sell at different prices. 就是简单的市场供给曲线。Supply里面包括当年生产的也包括之前的库存
- **Law of supply**：The positive relationship between price and quantity supplied, when all other factors that influence supply are held fixed. 意即价格越高，供给者会供给的产品越多
- **Factors of production**：Resources such as labor and raw materials that are used to produce a good.
- 很多东西，包括上面的生产要素，都可以影响供给的量，比如别的产品的价格也会影响供给的量。和供给曲线一样，supply curve也只探讨价格和供给的关系
- **Market Equilibrium**：The point where the quantity demanded equals the quantity supplied, so the market clears
- **Excess Supply**：当价格偏高，生产者愿意供给比需求者需求更多的商品 A situation in which the quantity supplied at a given price exceeds the quantity demanded. 在这种情况下，价格会变低，趋于平衡
- **Excess Demand**：当价格偏低，消费者需求比生产者愿意供给的更多的商品 A situation in which the quantity demanded at a given price exceeds the quantity supplied 在这种情况下，价格会变高，趋于平衡
- **价格属于外生变量还是内生变量**：值得注意的一个问题是，价格和数量都属于内生变量，因为价格“无法被单一的经济决定者所决定”，他是一个必须要通过供给曲线和需求曲线来决定的值，他是由模型产生的值，所以价格属于内生变量，并且这个模型基本上只在乎处于平衡状态下的数量和价格
- 题型：根据书上的边做边学，这方面的题型有：
	- 给你需求数量关于价格的表达式/供给数量关于价格的表达式，再给你个函数取值，求数量/价格的值（弱智问题）
	- 和上面一样，给你提供两个表达式，然后求他们的市场平均状态（价格+供给），这个就令两个表达式相等求得价格再带回去就好了
#### Shifts in Supply and Demand
- **Shift in either supply or demand**:
	- 首先这个东西要知道，只有exogenous variable的变化会shift曲线，单是价格的变化体现在曲线的上面
	- *To do a comparative statics analysis*:
		1. Determine how a particular exogenous variable affects demand/supply curve
			- 比如如果人们的工资上涨了了，那么demand curve就会右移
			
			<img src="assets/post_pics/Snipaste_2020-05-18_10-07-01.png">

			- 又比如工人的wage rate变高了（这个rate貌似对应的是产品quantity而言），那么供给者生产成本变高了，所以供给曲线会向左移（供给的变少了）
	- 然后根据这个观察图的变化，得出了以下几个废话结论
		- Increase in demand + unchanged supply curve = higher equilibrium price and larger equilibrium quantity
		- Decrease in supply + unchanged demand curve = higher equilibrium price and smaller equilibrium quantity
		- Decrease in demand + unchanged supply curve = lower equilibrium price and smaller equilibrium quantity
		- Increase in supply + unchanged demand curve = lower equilibrium price and larger equilibrium quantity
	- 题型：根据书上的“边做边学”：
		- 给你一个表达式，这个表达式往往不是只关于价格，而是像下面这个一样
		- \\( Q^{d} = 500-50P+10I \\)
		- 都知道I是一个另外的因素，他就会告诉你一个I的取值，然后叫你求市场平衡状态
		- 或者是告诉你一个I的大致走向（上升还是下降），叫你探讨这个新的I会如何影响市场的平衡状态，这个东西基本上大致都能直接看出来
- **Shift in both supply and demand**:
	- 有些时候，不单单只是需求曲线/供给曲线单一会被影响，而是两条线都会一起移动，但是因为两条线都是一起移动，所以具体的移动之后对价格/数量造成的影响依然是要具体问题具体分析，要看因素对需求/供给造成的影响的具体大小才可以分析

	<img src="assets/post_pics/Snipaste_2020-05-18_11-06-35.png">

- Price Index感觉是个不会考的内容，不过还挺有意思：
	- 怎么看Price index：Values of the index are calcu- lated as a computer’s price that month as a percentage of the price of a comparable computer at the end of 1988. For example, suppose that the computer priced in December 1988 was $5,000. The index’s value at the end of 1990 was about 90, so a comparable computer would have cost about $4,500 (90 percent of $5,000) that month.
	- 这样子的逻辑是依照Bureau of Labor Statistics（BLS）

### 2.2 Own-Price Elasticiyty of Demand 价格弹性
- **The price elasticity of demand measures the sensitivity of the quantity demanded to price**
- 需求的价格弹性：需求的数量随商品价格的变动而变化的弹性。
- Notation：\\( \epsilon_{Q, P} \\)表示的是percentage change in quantity demanded Q brought by a 1 percent change in price P.

$$
\begin{aligned}
& \epsilon_{Q, P} = \frac{percentage\ change\ in\ quantity}{percentage\ change\ in\ price}\\
\end{aligned}
$$

$$
\begin{aligned}
& (Q的变化量相对于当下Q的比例)percentage\ change\ in\ quantity=\frac{\Delta Q}{Q}  100%\\
\end{aligned}
$$

$$
\begin{aligned}
& (P的变化量相对于当下的P的比例)percentage\ change\ in\ price=\frac{\Delta P}{P}  100%\\
\end{aligned}
$$

$$
\begin{aligned}
& \epsilon_{Q,P} =\frac{\Delta Q}{\Delta P}\frac{P}{Q}
\end{aligned}
$$

- 具体的例子：For example, suppose that when the price of a good is $10 (P=10), the quantity demanded is 50 units (Q=50), and that when the price increases to $12 ( \\( \Delta P=+2 \\) ), the quantity demanded decreases to 45 units ( \\( \Delta Q=-5 \\) ). 那么直接强行带入公式就好了

$$
\begin{aligned}
& \epsilon_{Q,P} =\frac{\Delta Q}{\Delta P}\frac{P}{Q} = \frac{-5}{2}\frac{10}{50} = -0.5
\end{aligned}
$$

- 并且根据Law of demand，这个需求价格弹性必须是负的。
- 根据算出来的需求价格弹性的不一样，可以为需求价格弹性分类：

<img src="assets/post_pics/Snipaste_2020-05-18_11-49-26.png">

- 在看图的时候，如果横轴代表quantity，纵轴代表price，那么如果一条曲线的需求价格弹性越小（越elastic），那么他会显得更加水平（价格稍有变化会对数量带来很大的影响）；而数值比较大的（越不elastic）的曲线，则会显得更加垂直，价格的变化，对曲线不会带来太大的影响
- 当一条曲线完全水平的时候，就是perfectly elastic -> 只要价格变化，将不会有任何quantity，或者可以理解成，在价格P之下，任何数量的产品都可以被出售；当一条曲线完全垂直的时候，就是perfectly inelastic -> 不管价格如何变动，数量都恒定
- 题型：给定Q，P还有Q和P的变化量，计算需求价格弹性 ->直接套公式

#### Elastic along specific demand curves
- **Linear Demand Curve**: 需求曲线是一条直线，表示为\\( Q=a-bP \\)，其中a代表了其他所有影响的因素，b则代表了需求数量会如何按照价格来变化
- **Inverse demand curve**：有一条需求曲线，inverse demand curve就是基于这条需求曲线的一个price as a function of quantity。就是\\( P=\frac{a}{b}- \frac{1}{b}Q \\)
	- 其中，**choke price**指的是\\( \frac{a}{b} \\)这个值，它的意义是当需求数量变为0时，他的价格为这个
- **计算弹性公式在下面，最关键的就是要记住计算这个其实就是斜率（需求价格曲线）乘上比例**
- **Modified price elastic of demand**: 根据以上的种种公式，可以推出一个恒定的价格需求弹性的公式：
	- 所以其实这个东西的意义就是，\\( \frac{P}{Q} \\)这个函数的变化率，几何意义的话可以想成是一个曲面，再对这个曲面求导是要得到他的割面，而这个割面就代表了需求价格弹性
	- **所以在计算的时候，拿到任何一个P关于Q的函数，或者是Q关于P的函数，都要先找到Q关于P的函数（如果直接给了当然更好），然后求出\\( \frac{DQ}{DP} \\)，再简单的带入表达式\\( \frac{DQ}{DP}\frac{P}{Q} \\)即可，有时候可以运用多种法则还可以化简**

$$
\begin{aligned}
& \epsilon_{Q,P} =\frac{\Delta Q}{\Delta P}\frac{P}{Q} = -b\frac{P}{Q}
\end{aligned}
$$

- 又根据以上这个公式，得出了下面这张图，下面这张图的意义是，在线上不同的点的弹性各不一样，具体请看下图

<img src="assets/post_pics/Snipaste_2020-05-18_14-07-23.png">

- 以上的两个region：Elastic region和Inelastic region分别代表了需求价格弹性在不同的区间中取的需求价格弹性，注意了，这个midpoint指的是价格midpoint
- **斜率和弹性的区别以及为什么不用斜率**：斜率衡量的是绝对变化（unit of percentage），而需求价格弹性衡量的是百分比变化（1 percentage change in price）。那么为什么不用斜率呢？斜率衡量的单位是一个商品的一个unit，但是不同的商品的单位不一样，所以如果对比商品之间，连单位都无法控制一样的话，就没什么意义
- **Constant Elasticity Demand Curve**：需求曲线是一个幂函数：\\( Q=aP^{-b} \\)，这样的需求曲线，他的需求价格弹性恒定是\\( -b \\).
- **题型**：告诉你一条直线需求曲线/幂函数需求曲线，然后给你P和Q的取值，让你算具体的需求弹性，也很简单，看上面的公式就好
- **total revenue**: Selling price times the quantity of product sold.
- **解读弹性**：Consider the estimated elasticity of 0.107 for cigarettes in Table 2.1, which indicates that a 10 percent increase in the price of cigarettes would result in a 1.07 percent drop in the quantity of cigarettes demanded.
- 影响需求弹性的因素：
	- Demand tends to be more price elastic when there are good substitutes for a product
	- Demand tends to be more price elastic when a consumer’s expenditure on the product is large (either in absolute terms or as a fraction of total expenditures)
	- Demand tends to be less price elastic when the product is seen by consumers as being a necessity. 
- **Market-level VS Brand-level**：这个也很好理解，就是在市场层面的需求价格弹性绝对不等于在单一品牌层面的需求价格弹性。假设只有一个品牌的香烟涨价了，那么很有可能对于这个品牌的需求大大降低，但香烟整体的需求是不弹性的，这个品牌的消费者大可以去买别的品牌的香烟，Even if demand is inelastic at the market level, it can be highly elastic at the individual brand level. 而且根据观察可以得出的是，如果一个品牌的替代者越多，那么他的需求价格弹性的绝对值就越高。

### 2.3 Other Elasticities
- **Income Elasticity of Demand**: 顾名思义：the ratio of the percentage change of quantity demanded to the percentage change of income, holding price and all other determi- nants of demand constant.当工资变化percentage，需求会如何变化

$$
\begin{aligned}

& \epsilon_{Q, I}=\frac{\Delta Q}{\Delta I}\frac{I}{Q}

\end{aligned}
$$

- 这个东西一般是正的，这个也好理解：当工资上升，人们也更乐意买更多的东西。但这个也不绝对，例如有研究表明，在亚洲的某些国家，对于米饭需求工资弹性是负的

- **Cross-Price Elasticity of Demand**：The cross-price elasticity of demand for good i with respect to the price of good j is the ratio of the percentage change of the quantity of good i demanded to the per- centage change of the price of good j。这个探讨的实际上是两种商品之间的关系-> 当商品j的价格上升的时候，对于商品i的需求的变化

$$
\begin{aligned}

& \epsilon_{Q_i, P_j} = \frac{\Delta Q_{i}}{\Delta P_j}\frac{P_j}{Q_i}

\end{aligned}

$$

- 如果这个弹性是正数，说明当一个产品的价格上升，另一个产品的需求上升，那么说明这两个产品属于互相替代的关系：demand substitutes：Two goods related in such a way that if the price of one increases, demand for the other increases.
- 如果这个弹性是负数的话，就说明这两个东西是互补品：demand complements：Two goods related in such a way that if the price of one increases, demand for the other decreases.
- **Long-run demand curve**：The demand curve that pertains to the period of time in which consumers can fully adjust their pur- chase decisions to changes in price.
- **Short-run demand curve**：the demand curve that pertains to the period of time in which consumers cannot fully adjust their purchasing decisions to changes in price.
- **Durable Good**：Goods, such as automobiles or airplanes, that provide valuable services over many years.
- 总而言之，短期需求曲线探讨的是消费者无法完全作出消费决定，而在长期的需求曲线中，消费者有时间做出完整的消费决定，对于短期和长期的需求价格曲线，他们的弹性的比较是可以讨论的：
	- 长期需求曲线弹性大于短期需求曲线弹性：这种情况一般发生在诸如石油、天然气等产品，这些产品中，对他们的需求往往基于对其他固定资产的需求（汽车），所以在短期内很难改变，但在长期内可以改变，所以长期需求曲线弹性大于短期需求曲线弹性
	- 长期供给曲线弹性大于短期供给曲线弹性：这种情况发生在短期内，生产者因为种种原因无法生产他想要的那么多的产品，但在长期可以，所以长期他对价格的敏感度就高于短期
	- 长期需求曲线弹性低于短期需求曲线弹性：一般使用在durable good上面。比如如果飞机的价格上升了，那么在长期需求中，这对于航空公司来说是必需品，所以必须得换；但是对于短期来说，航空公司可能决定这个飞机多开几年，所以短期内的需求可能会下降的比长期的需求要多
	- 长期供给曲线弹性高于短期需求曲线弹性：一般出现在可以再次使用/二手市场出售的商品中，在短期内，这个商品价格上升，would elicit an increased supply from two sources: additional new aluminum and recycled aluminum made from scrap. However, in the long run, the stock of scrap aluminum will diminish, and the increase in quantity supplied induced by the increased price will mainly come from the produc- tion of new aluminum.

