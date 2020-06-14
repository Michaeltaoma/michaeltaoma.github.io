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

- “经济法律和推理仅仅是材料的一部分，在解决实际问题和制定可能成为生活指南的规则时，良心和常识必须加以利用。”

但是，《经济学人》也不得不考虑道德力量。确实有人试图就“经济人”的行为建立一种抽象的科学，经济人不受道德的影响，谨慎而积极地追求金钱利益，但机械地和自私地。但是它们没有成功，甚至没有完全执行;因为他们从来没有真正把经济人看作完全自私的人。最可靠的人莫过于有经济头脑的人，他为了养家糊口而无私地吃苦耐劳、牺牲牺牲;他的正常动机一直被默认为包括家庭感情在内。但是，如果把这些动机也包括在内，为什么不把所有其他的利他动机也包括在内呢?到目前为止，任何阶级、任何时间、任何地点的所有其他利他动机的行为都是一致的，因此可以归结为普遍规律。”

## Chapter 3: Consumer Preferences and the Concept of Utility

- 在这个章节里面，主要探讨的是消费者的喜好，忽视掉商品的价格，我们不谈钱，只谈感情，这一章和下一章结合在一起会探讨一个问题：在经济条件允许的情况下，消费者会怎么选择商品
- Represent consumer preferences in terms of market baskets of goods and services
- Apply three basic **assumption** about consumer preferences: Preferences are complete, preferences are transitive, and more is bettwe
- Distinguish between **ordinal and cardinal ranking of preferences**
- Apply utility functions as a tool for representing preferences and analyze the concept of **marginal unitility** and the principle of diminishing marginal utility
- Apply utility functions in the analysis of preferences with a **single good and with multiple goods.**
- Construct indifference curves as a way of representing util- ity functions in simplified form. 
- Analyze the concept of the **marginal rate of substitution of one good for another.**
- Describe and compare some **special utility functions.**

### 3.1 Representation of preferences
- **Market basket(bundle)**: A collecition of goods and services that an individual might consume.注意这个colletion里面清楚表明了商品/服务的数量的，是个非常具体，一点都不抽象的类目
	
	<img src="assets/post_pics/Snipaste_2020-05-21_20-15-57.png">

- **Consumer Preferences**：指的是给定两个basket，假定basktes都不需要任何cost的情况下，消费者会如何rank这两个basket
- **Assumptions about consumer preferences**（首先必然是消费者是理智的）
	- Preferences are complete：消费者必须“有能力”去找到自己最喜欢的那个，**注意**：equally喜欢也是允许的
	- Preferences are transitive: 就是说如消费者偏好A多过B，偏好B多过D，那么他必定偏好A多过D
	- More is better：两个basket，如果能控制剩余的商品数量一样，那么消费者必然偏好剩下的商品更多的那个basket，根据这个原则在上面那张图里面，消费者在全局必然最偏好A
- 以上的assumption在现实生活中往往不那么显然的存在，这是因为现实生活中变化太多了
- **Ordinal Ranking**: give us information about the order in which a consumer ranks baskets。只包含简单的次序，也就是说只能看出来消费者更加喜欢哪个，却很难看出来消费者有多喜欢。
- **Cardinal Ranking**: give us information about the intensity of a consumer’s preferences。Cardinal ranking还给了喜欢的强度，我们不仅知道消费者在A和B之间更喜欢B，我们甚至还知道消费者喜欢B多过A多多少

### 3.2 Utility Functions

- **Utility Function**: A utility function measures the level of satisfaction that a consumer receives from any basket of goods. We can represent the utility function with algebra or a graph.
	- \\( U(y)=\sqrt(y) \\)就是一个简单的utility function的例子，他衡量的是某人购买了y件产品，他的utility值是多少
- **Marginal Utility**：又到了导数的概念，marginal utility指的是rate of change in U respect to change in y。就是how the level of satisfaction will change in response to a change in the level of consumption

$$
\begin{aligned}
& MU = \frac{dU}{dy}
\end{aligned}
$$

	因为这个不需要化简单位，所以在图像上，marginal utility就是在utility function函数上某一点的切线斜率

- 然后根据这个导数又得出了一个经济学的理论：The additional satisfaction that ppl receives from consuming more of a good depends on how much of the good she already consumed

	<img src = "assets/post_pics/Snipaste_2020-05-21_20-51-52.png">

- 在经济学中所有的边际关系都是像这样用导数来衡量的

- **Principle of diminishing marginal utility**：After some point, as consumption of a good increases, the marginal utility of that good will begin to fall. 这个也很符合人类的行为，因为当我们越多的消费一个东西的时候，每多消费这样的东西带来的效益就没有之前那么高了


### Preferences with multiple goods: Marginal Utility, Indifference Curves and the marginal rate of substitution
- 单个产品的utility function作用并没有很大，我们在生活中往往需要衡量多个商品对自己的utility，假设for any basket(x, y)，utility function是\\( U = \sqrt{(xy)} \\)，那么他的utility function的图如下
	
	<img src="assets/post_pics/Snipaste_2020-05-24_21-50-08.png">

- **多个产品的边际效用的计算**：计算多个产品边际效用很简单：控制住n-1个产品的consumption为常量就好了：The marginal utility of any one good is the rate at which total utility changes as the level of consumption of that good rises, holding constant the levels of consumption of all other goods.
- \\( \sqrt{xy} = \sqrt{x} \times \sqrt{y} \\)
- 在计算的时候，给定一个basket，只可以分别计算他们各商品的MU
- 如果\\( U = \sqrt{xy} \\), 那么\\( MU_{x} = \frac{\sqrt{y}}{2\sqrt{x}} \\)，\\( MU_{y} = \frac{\sqrt{x}}{2\sqrt{y}} \\)
- 注意，这个理论基础比较虚，要根据实际的效用函数来看他的mu的性质

- **Indifference Curve**: A curve connecting a set of consumption baskets that yield the same level of satisfaction to the consumer.

<img src="assets/post_pics/Snipaste_2020-05-24_22-35-16.png">

- 所以对于布兰登来说，他indifferent in A，B和C，因为他们都有同样的效用值
- 上面那个也被称为indifference map
- indifference curve的四个性质：
	- When the consumer likes both goods (i.e., when MUx and MUy are both positive), all the indifference curves will have a negative slope
		- 这个证明也很简单，Points to the northeast or southwest of A cannot be on the same indifference curve as A because they will be preferred to A or less preferred than A, respectively. Thus, points on the same indifference curve as A must lie either to the northwest or southeast of A.
	- Indifference curves cannot intersect
	- Every consumption basket lies on one and only one indifference curve
	- Indifference curves are not “thick.”

- **Marginal rate of substitution**：The rate at which the consumer will give up one good to get more of another, holding the level of utility constant. 比较关键的概念是他hold the level of utility constant -> 在utility值保持不变的情况下，消费者愿意放弃多少某商品从而获得更多的商品，虽然说我们这一章讲的preference都是不计成本的，但问题是utility值现在变成了一个限制
	- a consumer’s **marginal rate of substitution** of **hamburgers for lemonade** is the **rate at which the consumer would be willing to give up glasses of lemonade to get more hamburgers, with the same overall satisfaction.**
	- 表现在indifference map上面就是，一条indifference curve的斜率
	- 假设现在两个商品分别是x和y，那么\\( \frac{dy}{dx} \\)代表了**The rate of change of y relative to the change of x = Marginal rate of substitution of x for y** -> 为了得到x，需要放弃多少y，可以这么理解：change of y relative to x，说明y的变化随着x而变化，说明我们是自己控制x，“为了得到x”就对应了这个性质

- **Indifference Map for consumer is given exogenously and remains fixed**
- 非常重要的公式，这个公式的推导是根据在indifference curve上的x和y的任何增量都不会影响u的值：
	- \\( \Delta U = MU_{x}(\Delta x) + MU_{y}(\Delta y) \\)
	- \\( 0 = MU_{x}(\Delta x) + MU_{y}(\Delta y) \\)
	- \\( -MU_{x}(\Delta x) = MU_{y}(\Delta y) \\)
	- 根据以上推理出来最终的MRS的公式是：
	
	$$
	\begin{aligned}
	& MRS_{x, y} = \frac{dy}{dx} = -\frac{dy}{dx} = \frac{MU_{x}}{MU_{y}}
	\end{aligned}
	$$

- **negative of the slope of the indifference curve on a graph with x on the horizontal axis and y on the vertical axis**

- **Diminishing Marginal rate of substitution**: A feature of consumer pref- erences for which the marginal rate of substitution of one good for another good diminishes as the consumption of the first good increases along an indifference curve.一开始的时候，因为消费者消费x的数量不多，所以消费者很乐意去拿许多的y去换一个x，但是他占有x的数量越来越多，占有y的数量越来越少，消费者会不那么乐意用那么多的y去换一个x了。根据indifference也可以看出这个性质

- **Draw indifference graph**: 给定一个utility function，给定一个utility值，要如何画indifference graph->只需要找出适当的x，y组合令utility值等于要求的utility值，这样就可以找出一个点，然后继续找下一个点，多找几个点就可以把线给描出来了
	
	- 如果问你可不可以和纵轴/横轴相交，用原函数式+x或y等于0去反推
- 做这种题目要时刻记住：只要MUx和MUy都是positive，那么他们的indifference curve就一定是negative slope

### 3.3 Special Preferences

- **Perfect Substitutes**：**Two goods are perfect substitutes when the marginal rate of substitution of one for the other is a constant**。也就是说，不管他已经获得了多少某种产品，消费者都会愿意用一定数量的产品去交换一定数量的另外一种产品。这类商品之间的MRS是个常量
	- More generally, indifference curves for perfect substitutes are straight lines, and the marginal rate of substitution is constant, though not necessarily equal to 1
	- 比如一个人愿意用2个P换取1个W，那么他的Utility function就是：U = P + 2W

- **Perfect Complements**：(in consumption) Two goods that the consumer always wants to consume in fixed proportion to each other. 比如一双袜子：左边袜子和右边袜子
	
	<img src="assets/post_pics/Snipaste_2020-05-25_11-42-23.png">

	- 以上这个例子就是perfect complement的例子：\\( U(R, L) = 10min(R, L) \\)

- **The Cobb-Douglas utility function**: 形如\\( U=\sqrt(xy) \\)或者是\\( U = xy \\)这样子的utility function都被称为cobb-douglas utility function, 更general的表示是\\( U=Ax^{\alpha}y^{\beta} \\), 其中\\(A, \alpha, \beta \\)都属于positive constant
	- 这类的utility function都有其三个性质：
		- The marginal utilities are positive for both goods.
		- Since the marginal utilities are both positive, the indifference curves will be downward sloping.
		- The Cobb–Douglas utility function also exhibits a diminishing marginal rate of substitution.(也就是说他的函数会慢慢变平，趋于饱和)
- **Quasilinear utility function**：A utility function that is linear in at least one of the goods consumed, but may be a nonlinear function of the other good(s).

	<img src="assets/post_pics/Snipaste_2020-05-25_11-55-19.png">

	- The distinguishing characteristic of a quasilinear utility function is that, as **we move due north on the indifference map, the marginal rate of substitution of x for y remains the same. That is, at any value of x, the slopes of all of the indifference curves will be the same, so the indifference curves are parallel to each other.**
	- At any value of x, the slope of all of the indifference curves(and hence the MRS_{x, y})will be the same 

## 4 Consumer Choice
- Theory of Consumer Choice, explaining how consumers allocate their limited incomes among available goods and services.
- Write the equation of the budget constraint and graph the budget line.
- Illustrate graphically how a change in income or a change in a price affects the budget line.
- Describe the conditions for optimal consumer choice.
- Illustrate graphically the tangency condition for optimal consumer choice.
- Solve for an optimal consumption basket, given information about income, prices, and marginal utilities.
- Explain why the optimal consumption basket solves both a utility maximization problem and an expendi- ture minimization problem.
- Explain why the optimal consumption basket could occur at a corner point.
- Illustrate the budget line and optimal consumer choice graphically when one of the goods a consumer can choose is a composite good.
- Describe the concept of revealed preference.
- Employ the concept of revealed preference to determine whether observed choices are consistent with utility maximization.

### 4.1 The Budget constraint
- **The budget cnsrtaint** defines the set of baskets that a consumer can purchase with a limited amount of income. 
- 假设I是income，那么：The budget line indicates all of the combinations of food (x) and clothing ( y) that Eric can purchase if he spends all of his available income on the two goods. It can be expressed as
	
	$$
		P_{x} x + P_{y} y = I
	$$

<img src = "assets/post_pics/Snipaste_2020-05-25_19-54-09.png">

- 显而易见的是，只要在budget line，x轴，和y轴包围的空间里面，他随便选，但在这个空间之外，就是不行的了，而budget constraint的式子是\\( P_{x}x + P_{y} y \leq I \\)
- **budget line的斜率**: Thus, the slope of the budget line tells us **how many units of the good on the vertical axis a consumer must give up to obtain an additional unit of the good on the horizontal axis.** 和MRS有点像，不过又不尽一样，因为MRS控制的是utility相等，而这个控制的是开销相等
- 如果收入变多了，那么budget line向上平行移动

	<img src="assets/post_pics/Snipaste_2020-05-25_20-02-54.png">

- 如果一个商品的价格改变了的话，这个budget line会“旋转”，像下面这样：

	<img src+"assets/post_pics/Snipaste_2020-05-25_20-05-36.png">

- Thus, an increase in the price of one good moves the intercept on that good’s axis toward the origin. Conversely, a decrease in the price of one good would move the intercept on that good’s axis away from the origin.
- **假设工资和商品的价格同时涨到了本来的2倍，那么这对于budget line没有任何影响**

### 4.2 Optimal Choice
- **Optimal Choice**: Consumer choice of a basket of goods that (1) maximizes satisfaction (utility) while (2) allowing him to live within his budget constraint. 分为两个部分来讨论最佳选择：在不超过自己工资承受范围的情况下的同时最大化效用值
- optimal choice绝对在budget line上
- 整理一下，这个optimal choice的问题是：

$$
\begin{aligned}
& \mathop{max}_{(x, y)} U(x, y) \\
& subject\ to:\ P_{x}x + P_{y}y \leq I
\end{aligned}
$$

- 大致分了一下endogenous/exogenous
	- Endogeneous Variable: x, y
	- Exogeneous Variable: Prices, Income

<img src="assets/post_pics/Snipaste_2020-05-25_20-39-14.png">

- Diminishing MRS的图上表示是：because the indifference curves are bowed in toward the origin (in economic terms, because there is diminishing marginal rate of substitution of x for y)

- 同时，有个算式是：\\( \frac{MU_{x}}{MU_{y}} = \frac{P_{x}}{P_{y}}  \\) **The optimum occurs at a point where the budget line is tangent to the indifference curve.**：学到后面就会发现optimal点出现在切点仅仅是对于Cobb而言
- \\( \frac{MU_x}{P_x} = \frac{MU_y}{P_y} \\) **Put another way, at an interior optimum, the extra utility per dollar spent on good x is equal to the extra utility per dollar spent on good y.**
- **Interior Optimum**: An optimal basket at which a consumer will be purchasing positive amounts of all commodities.消费者不会不买任何产品
	- an interior optimal basket, the consumer chooses commodi- ties so that the ratio of the marginal utilities (i.e., the marginal rate of substitution) equals the ratio of the prices of the goods.
- 如果MUx和MUy都是正数，那么optimal choice会在budget line上面
- 如果存在diminishing marginal rate of substitution，那么interior optimal consumption会出现在indifferent curve和budget line相切的地方
- 在看待这个优化问题的时候，当然存在别的角度：What basket should the consumer choose to minimize his expenditure (Px x  Py y) and also achieve a given level of utility U2?

$$
\begin{aligned}
& \mathop{min}_{(x, y)} expenditure = P_{x}x + P_{y}y \\
& subject\ to:\ U(x, y) = U_{2}
\end{aligned}
$$

- 这样的问题被称为：**expenditure minimization problem**

<img src="assets/post_pics/Snipaste_2020-05-25_21-22-46.png">

- The consumer can increase utility if he continues to spend $800 monthly, or he can spend less money to stay at the same level of utility he is currently realizing at B.

- **Corner Points**: A solution to the consumer’s optimal choice problem at which some good is not being consumed at all, in which case the optimal basket lies on an axis.

<img src="assets/post_pics/Snipaste_2020-05-25_21-31-52.png">

- 上图就阐明了一种这样子的关系，当没有一条indifferent curve和bl相切。并且这三条indifferent curve的都比BL要更加的斜，经过证明，这代表了：\\( \frac{MU_x}{P_x} \lt \frac{MU_y}{P_y} \\)，也就是说明tells us the marginal utility per dollar spent is higher for food than for clothing, so the consumer would like to purchase more food and less clothing. 所以消费者必定会选择R（把food选到最大）

- 如果要找有拐点的optimal value：先通过计算斜率等大致说出indifference curve和bl的一些性质（凸起还是凹下啊），陈述拐点的可能存在，然后根据MUx/MUy = Px/Py试图找切点，找到悖论证明切点不存在，说明最优解在拐点，直接算拐点的时候的utility值

- Kink：这个知识记在了Module笔记上

### Chapter 4: Appendix 1: The Mathematics of Consumer Choice

- 是拉格朗日乘数是一种寻找多元函数在其变量受到一个或多个条件的约束时的极值的方法
- 这种方法将一个有n 个变量与k 个约束条件的最优化问题转换为一个有n + k个变量的方程组的极值问题，其变量不受任何约束。这种方法引入了一种新的标量未知数，即拉格朗日乘数：约束方程的梯度（gradient）的线性组合里每个向量的系数。
- 先看看这个拉格朗日乘数一般是如何定义的：

$$
\begin{aligned}
	& \text{Assume current funtcion is z = f(x, y) and } \phi(x, y)=0 \\
	& \text{goal is to maximize z while preserving } \phi(x, y) = 0 \\
	& \text{Lagranian Function will be defined as } F(x, y, \lambda) = f(x, y) + \lambda \phi(x, y)\\
\end{aligned}
$$

- 定义好了之后，如何根据拉格朗日函数的方法求值呢？必须要通过三元方程解出\\( x, y, \lambda \\)的值（同时满足下列三个等式）

$$
\begin{aligned}
	& F'_{x} = f'_{x}(x, y) + \lambda {\phi}'_{x}(x, y) = 0 \\
	& F'_{y} = f'_{y}(x, y) + \lambda {\phi}'_{y}(x, y) = 0 \\
	& F'_{\lambda} = {\phi}(x, y) = 0 \\
	& \text{也就是对这三个值分别求导等于0，必须找到这样一个combination就可以了}
\end{aligned}
$$

- 现在回到我们的optimal choice的题目

$$
\begin{aligned}
& \mathop{max}_{(x, y)} U(x, y) \\
& subject\ to:\ P_{x}x + P_{y}y \leq I
\end{aligned}
$$

- 显然拉格朗日函数就被定义为\\( F(x, y, \lambda) = U(x, y) + \lambda (I - P_{x}x - P_{y}y) \\), 且和刚刚一样，都要满足刚刚那几个条件就好了，

<img src="assets/post_pics/Snipaste_2020-05-29_22-51-38.png">

- The partial derivative dU(x, y)/dx is the mathematical expression for the marginal utility of x (MUx). It measures how much utility increases as x increases, holding y constant. Similarly, the partial derivative dU(x, y) /y is the mathematical expression for the marginal utility of y (MUy). It measures how much utility increases as y increases, holding x constant. 这里解释了上面那张图片的几个项是什么意思

- 然后。。。你妈的推回来了以下的等式证明了在cobb效用函数中确实应该使用切线定理：

$$
\begin{aligned}
& \frac{MU_x}{MU_y} = \frac{P_x}{P_y} \\
& P_{x}x + P_{y}y = I \\
\end{aligned}
$$

-  So the mathematical solution to the consumer choice problem tells us that an optimal interior basket will satisfy the tangency condition and be on the budget line. This verifies the conditions for an op- timum we developed in the text, using a graphical approach.神你妈的verify

## Chapter 5: The theory of Demand

- 理解demand的具体信息非常重要：其中包括一条是：如果政府对需求价格弹性不高的（对价格不敏感）的产品征税的话，政府可以得到更高的税收，同时，研究表明，香烟对于消费者工资的变化也相当的不敏感，在recession期间，对香烟征税，且因为香烟对工资的降低不敏感，政府可以得到非常客观的税收
- 这一章的主旨是：Studying the impact of chages in prices and income levels on an individual's consumption decision, we can: **gain insight into why some goods, such as cigarettes, have demands that are relatively insensitive to changes in prices and income, while other goods, such as automobiles, might have demands that are relatively more sensitive to changes in prices, or income, or both.**

- Explain how a consumer's demand for a good depends on the prices of all goods and on income
- Examine how a change in the price of a good affects a consumer through a substitution effect and an income effect
- Explain how a change in the price of a good affects three measures of con- sumers’ well-being: consumer surplus, compensating variation, and equivalent variation.
- Derive market demand curves from individual demand curves.
- Discuss the effects of network externalities on demand curves.
- Explain how consumers choose to allocate their time between labor and leisure and how this relates to the supply of labor in the market.
- Explain the biases in the Consumer Price Index.

### 5.1 Optimal Choice and demand

<img src="assets/post_pics/Snipaste_2020-05-30_22-31-42.png">

- 如上图，这里主要讲了如何通过indifferent curve + budget line的组合作出以下的demand curve。观察就会得到，确实当食物的价格下降的时候，对事物的需求确实变大了
- **Price consumption curve**: The set of utility-maximizing baskets as the price of one good varies (holding constant income and the prices of other goods).(这个curve就是把在indifferent curve那边的当某一商品价格不停变化而带来的optimal choice的变化给连在一起的)
- 需求曲线有时候也可以理解成“消费者愿意消费曲线”：具体怎么看呢？可以看上图，在价格为4的时候，MRSx,y是1，也就是说消费者愿意付出多一个unit的clothing来换得一个unit的food，而一个unit的clothing正好是$4，这就带来了当我们已经有2unit食物的时候，消费者愿意花费4块钱去买多一个，其实就是把图上面的东西解释来解释去
- **The Effect of a change in income**: 

<img src="assets/post_pics/Snipaste_2020-05-30_22-48-25.png">
- **Income consumption curve**: The set of curve utility-maximizing baskets as income varies (and prices are held constant).
- **Engel Curve**: a graph relating the amount of the good consumed to the level of income.
	- 一个正斜率的engel curve代表了normal good：赚得越多，买得越多
	- **shows that a good with a positive income elasticity of demand will have a positively sloped Engel curve.**
	- 一个负斜率的engel curve说明是个inferior good：赚得越多，买的越少

<img src="assets/post_pics/Snipaste_2020-05-30_23-06-20.png">

- 阐述了一句废话： If a good is normal, its income elasticity of demand is positive.
- **如何通过Utility function和budget line去找到demand curve（没有corner points的）**
	- 注意此时的utility function是\\( U(x, y) = xy \\)然后此时的budget line是\\( P_{x}x + P_{y}y = I \\)
	- 并且求出此时的\\( MU_{x} = y, MU_{y} = x \\)
	- 因为根据之前的经验，消费者对这两个商品都想要，mu都大于0。所以他们的optimal choice都是interior，也就是x，y都是正数数量，所以**optimal choice**必然在budget line和indifferent curve的切点上
	- 也就是符合\\( \frac{MU_x}{MU_y} = \frac{P_x}{P_y} \\)

	$$
	\begin{aligned}
		& \text{代入MU_x和MU_y轻松得到} \\
		& \frac{y}{x} = \frac{P_x}{P_y} \\
		& y = (\frac{P_x}{P_y})x \\
		& \text{代入原有的budget line得到} \\
		& P_{x}x + P_{y}(\frac{P_x}{P_y} x) = I
		& x = \frac{I}{2P_{x}}
	\end{aligned}
	$$

	- 上面求出来最后的x=什么什么就是demand curve for x了
	- 然后题目有时候会问你当I等于多少的时候demand curve是多少，就直接把I带进去就好了

- **如何通过Utility function和budget line去找到demand curve（有corner points的）**
	- 注意此时的utility function是\\( U(x, y) = xy+10x \\)，观察易得y可以是0
	- \\( MU_{x} = y + 10, MU_{y} = x \\)
	- price of x is 1, price of y is Py
	- 然后注意这里是有corner point的存在的，这种情况下的话要分情况讨论
		- 最佳点不在拐点：
			- 如果是这种情况的话，那么计算的方式和普通的无拐点的情况下是一样的，根据切点相等的条件用y来表示x，然后代入到budget line里面得到demand curve
			- 具体的就不计算了不过结果是：\\( y = \frac{100 - 10P}{ 2P_{y}} \\)
		- 最佳点在拐点：
			- 这种情况的话就要观察一下，可以看到上面最佳点不在拐点的情况得出来的式子说明当P_y大于10的时候，y就变成负的了，说明这个关键点就是y价格为10的时候
			- 直接讨论说明当y的价格高于10的时候对y的demand为0就好了

### 5.1 Change in the price of good: <u>Substitution Effect and Income Effect</u>

- **Substitution Effect**: The change in the amount of a good that would be consumed as the price of that good changes, holding constant all other prices and the level of utility.保持效用值和别的一切商品价格不变的情况下，当某件商品的价格改变时，消费者购买的数量会如何改变 
	- For example, if the price of food falls, the con- sumer can achieve the same level of utility by substituting food for other goods (i.e., by buying more food and less of other goods)
- **Income Effect**：The change in the amount of a good that a consumer would buy as purchasing power changes, holding all prices constant.当一件商品的价格改变时，等同于说明消费者的购买力也改变了。The income effect accounts for the part of the total difference in the quantity of the good purchased that isn’t accounted for by the substitution effect.
- 下面这个解释挺不错的：
	- 一种商品的名义价格（nominal price）发生变化后，将同时对商品的需求量发生两种影响
		- 替代效应：因该种商品名义价格变化，而导致的消费者所购买的商品组合中，该商品与其他商品之间的替代
		- 收入效应：另一种是在名义收入不变的条件下，因一种商品名义价格变化，导致消费者实际收入变化，而导致的消费者所购商品总量的变化，称为收入效应（income effect）。
- 先留个坑：现在已经知道了替代效应的效用维持不变，那收入效应呢？

#### THE SUBSTITUTION EFFECT

- 替代效应在乎的是： The **change in the amount of a good** that would be consumed as the price of that good changes, holding constant all other prices and the level of utility，根据这一个定义可以看到虽然现在价格下降之后，BL向外推，实际可以达到的效用值是U2，但是我们不在乎这个，目前在乎的是，为了维持现有的效用值，需要多购买x多少个。
- 作平行的原因是因为在价格下跌了之后，y和x之间的比例要保持一致，斜率得一致
- Thus, the substitution effect accounts for the consumer’s movement from basket A to basket B—that is, the portion of the overall effect on the quantity of food purchased that can be attributed to the substitution effect is xB - xA.

<img src="assets/post_pics/Snipaste_2020-06-01_11-22-09.png">

#### THE INCOME EFFECT
- 同样的还是可以根据上面的图来解释
- the change in the amount of a good consumed as the consumer’s utility changes.
- 可以看到在替代效用之后，消费者会在A和B中摇摆不定，因为A和B都在同一条indifferent curve上面，所以对消费者来说似乎没有区别，但同时又看到，如果消费者此时因为替代效用在B点的这个BLd那里，在这一点上消费者的income其实是降低了的，也就是说当他买完B这个basket之后，还有钱没有花掉，所以消费者此时会选择购买更多的东西: **restoring the lost income**从而达到一个更高的效用值U2
- 那么，拢共说明了：当价格从P_x1降到了P_x2的时候，消费者对于x消费的总变化为x_c - x_a，这其中可以分为
	- 因为替代效应而产生的x_c - x_a
	- 因为收入效应而产生的x_c - x_b

- **也就是说收入效应和替代效应都工作于同一个方向**

#### When goods are not normal

- **当商品既不normal也不inferior**：income effect影响为0

	<img src="assets/post_pics/Snipaste_2020-06-01_11-49-37.png">

- **当商品是inferior的时候**：income effect有负影响
	
	<img src="assets/post_pics/Snipaste_2020-06-01_11-52-19.png">

- **当商品是giffen good的时候**：
	- A good so strongly inferior that the income effect outweighs the substitution effect, resulting in an upward-sloping demand curve over some region of prices.
	- 商品实在太垃圾了，导致income effect对数量的负影响甚至超过了替代效应对商品的正影响

	<img src="assets/post_pics/Snipaste_2020-06-01_11-55-59.png">

	- A Giffen good has a demand curve with a positive slope over part of the curve.
	
	- For an inferior good to have an income effect large enough to offset the substitution effect, the income elasticity of demand would have to be negative and the expenditures on the good would need to represent a large part of the consumer’s budget. 

- 对于如何计算income effect和substitution effect具体的数值书上170-171有详细的解释，也是根据上面那个step来的

- 下面就是讨论了当价格上升的时候（normal good）会如何变化，其实都是大同小异的

	<img src="assets/post_pics/Snipaste_2020-06-01_12-39-55.png">

- 在计算的时候，先根据相切的条件算出此时的x和y的数量是多少，然后按照utility function算出价格变化之前的效用值
- 然后把新的价格放入相切条件算出x和y的替换
- 然后代入进之前的效用值中
- 就可以得到为了维持在原有的效用值上，x和y的数量然后计算出他们的income，然后算cv就好了
- **Income and Substitution Effects with a Quasilinear Utility Function**
	- 给定一个quslinear的utility公式，其算demand curve的步骤和cobb的步骤基本是一样的，都是先根据切点的等式来求得
	- 然后有了demand curve之后就很舒服了，他给你什么价格就可以算出什么数量
	- 然后求decomposition的时候要充分记住，utility和原来保持不变，然后斜率和final的保持不变

### 5.3 Change in the price of a good: The concept of consumer surplus消费者盈余

- **Consumer Surplus**: the **difference** between the maximum amount a consumer is willing to pay for a good and the amount he must actually pay to purchase the good in the marketplace.
- The consumer surplus is the area below the demand curve and above the price that the consumer must pay for the good
- 虽然不知道为什么，但是**the area under a demand curve exactly measures net benefits for a consumer only if the consumer experiences no income effect over the range of price change**
- 如果是很简单的线性的demand function的话，算consumer surplus直接计算面积就好了

#### Understanding consumer surplus from the optimal choice diagram: compensating variation and equivalent variation
- 效用没有单位，伟大的经济学家使用金钱的单位来衡量
- **Compensating variation**: A measure of how much money a consumer would be willing to give up after a reduction in the price of a good to be just as well off as before the price decrease. 重点是要maintain utility
	- 当价格下降时，cv为正；当价格上升时，cv为负
- **Equivalent variation**：A measure of how much additional money a consumer would need before a price reduction to be as well off as after the price decrease. 
- 可以的，这个东西其实稍微理解一下可以出来：
	- 补偿变化：指的是在价格之后，消费者的income需要变化多少才可以回到之前的效用值。注意是价格变化之后，可以想象一下，当一个东西的价格变化了，消费者此时应该处于变化了的效用值，我们想让消费者回到之前的效用值，那么他的income需要变化多少。所以补偿变化指的是原来需要购买（价格变化之前的）的optimal组合的income和价格变化之后的价格和变化之前的同等的效用的optimal组合的difference
	- 同等变化：指的是在价格变化之前，消费者愿意主动变化多少自己的income去达到价格改变之后的效用值。这个计算的是价格变化之前的optimal组合和原价格需要的income和新的效用值加上现在的价格（价格没有实际变化）的difference

<img src="assets/post_pics/Snipaste_2020-06-01_19-48-00.png">

- 一般来说，cv和ev并不见得一样，因为income effect常常不是0
- 当income effect是0的时候且效用函数是quasilinear函数的时候，cv和ev相等

<img src="assets/post_pics/Snipaste_2020-06-01_19-52-24.png">

-  if there is no income effect, not only are the compensating variation and the equivalent variation equal to each other, they are also equal to the change in the consumer surplus (the change in the area under the demand curve as a result of the price change)

<img src="assets/post_pics/Snipaste_2020-06-01_20-02-49.png">

- 顺便讲一下为什么quasilinear的utility function就是income effetc就是0呢？因为income effect等于（新的budget line平行的budget line和旧的utility function的切点）和（新的budget line和新的utility function的切点）的差，因为现在两两互相平行，所以结果必定是一样的

### Market Demand

- **The market demand curve is the horizontal sum of the demands of the individual consumers**

<img src="assets/post_pics/Snipaste_2020-06-01_20-53-24.png">

- 计算的时候其实是要分情况讨论的，这一点书上面讲的非常清楚

<img src="assets/post_pics/Snipaste_2020-06-01_20-59-38.png">

- **Network Externalities**: A demand characteristic present when the amount of a good demanded by one consumer depends on the number of other consumers who purchase the good.消费者对于某种产品的需求基于其他想要这个产品的消费者的个数
	- 当externality是正的时候，说明越多人想要，我就越想要
	- 当externality是负的时候，说明越多人想要，我就越不想要

<img src="assets/post_pics/Snipaste_2020-06-01_21-08-02.png">

- 上图展现了一个带有bandwagon effect的正network externality的图，你看，当价格从20->10的时候，一般普通的商品的需求都是沿着需求曲线走的，但是这个不一样，因为价格便宜了，用的人多了，甚至会把需求曲线推向更远的地方，导致了搬瓦工效应

- **Bandwagon effect**: A positive network externality that refers to the increase in each consumer’s demand for a good as more consumers buy the good.

- **Snob effetc**: A negative network externality that refers to the decrease in each consumer’s demand as more consumers buy the good.

### 4.3 Consumer Choice With Composite Goods

- 一般只想探讨的顾客对于单一商品的selection，所以会把别的所有商品拢成*composite good*，这个composite good会被放在竖轴，然后根据传统，这个composite good的价格为1。

#### Application: Coupons and cash sbusidies

- **How a government program might increase the amount of housing chosen by a consumer**

<img src="assets/post_pics/Snipaste_2020-06-07_18-06-15.png">

- 以上这张图就把coupon和subsidy之间的关系阐述的很明了

- **subsidy**：可以看作是政府为了刺激消费者购买更多的housing而**直接给消费者发工资上的补贴**，就是直接给钱，这个钱可以用来买任何商品。那么他的budget line就会向右移动，从而会导致一个新的optimal choice相切于U2，但是也可以看出在这个新的optimal choice下面，房子的数量正好是政府希望人们去拥有的

- **Coupan**：**Coupan指的是只能花费在某种商品下的政府的补贴**，在这种情况下，人们能获得普通商品的量不会改变，却可以买更多的房子。在这张图上面，如果获得了房子的coupon，那么KFG就是消费者的BL，F是消费者把工资全用在普通商品，且只用coupon/voucher去买房子的情况；然后他马上急转直下来到了与x轴的交点，他也正好与U2相切与optimal点，切数量也是政府希望的数量

- 如果是上面的图的话，两种政策带来的后果是一样的，但是有的图，当政府介绍不同的政策的时候会带来不一样的结果，一般分为consumer会不会worse off或者政府的目的到底是想提高某种商品的消费，还是想提高人们的效用值

#### Applicatio: Joining a club

- **Consumer can join clubs that let them purchase goods and services at a discount**

<img src="assets/post_pics/Snipaste_2020-06-07_19-46-11.png">

#### Application: Borrowing and Lending

- 注意了，在接下来的讨论中：**saving = lending钱给银行(with the interest rate offered by the bank)**

<img src="assets/post_pics/Snipaste_2020-06-07_20-01-39.png">

- 这里接的是最下面appendix的内容

- 在这种情况下，消费者的效用函数是：
	
	$$
		\begin{aligned}
			& U(C_{1}) + \frac{U(C_2)}{1+P}
		\end{aligned}
	$$

- 注意在这张图里面，横轴和竖轴代表的是今年和明年而不是两种商品

- U(C)指的是消费者在某一年买了C dollar的composite good的时候所获得的效用值，其实就是给下一年的效用值加了个discount rate。这个discount rate就很特殊，它被称为**consumer's rate of time perference**: is a measure of the consumer's impatience. (这个值越大，说明消费者就越不“耐心”，说明消费者在未来得到的效用就越小)

- **MArginal rate of substitution is** \\( MRS_{c1, c2} = (1+p)\frac{U'(C1)}{U'(c2)} \\)

<img src="assets/post_pics/Snipaste_2020-06-08_16-13-04.png">


- This theory of optimal choice suggests, then, that for a given expectation of in- come growth, a more impatient individual will have a greater propensity to borrow than a more patient individual. And for a given rate of time preference, an individual with a higher expectation of income growth will have a greater propensity to borrow than an individual with a lower expectation of income growth.

#### Application: Quantity Discounts

- 这里讲的东西和第二个module讲的那个**kink**是一样的，其实指的就是**当买了多少多少个之后，价格会进行什么样的变化。**具体去看module 2的kinked budget就好了


### Chapter 4: Appendix 2: The time value of the money

- **Money has time value: 生动的例子就是给你100块钱和明天再给你100块钱之间选择，你大概率会选择前者**。同时这个也是为什么利率会存在的原因

- The techniques that can be used to compare amounts of money received at different points in time

#### Future value and present value

- **Future value of an amount of money \$C**: The amount you would have at a given date in the future if you put \$C into an account that earned a given rate of interest
	
	$$
		\begin{aligned}
		& \text{假设投入的本金为C，利率为r（per t），t是总共要存的period} \\
		& \text{那么future value 就是}C(1+r)^{t}
		\end{aligned}
	$$

- 这个公式当然也可以拿来反推present value：The amount you need to invest today at a given rate of interest so that you would have \$C at a given date in the future. 注意现在这里C变成了未来的钱

	$$
		\begin{aligned}
		& \text{假设未来的目标资金为C，利率为r（per t），t是总共要存的period} \\
		& \text{那么现在的present value 就是}\frac{C}{(1+r)^{t}}
		\end{aligned}
	$$

- **当计算present rate的时候，往往会把interest rate称为<u>discount rate</u>**

- 通过这个可以计算**present value of a stream of payments**

	<img src="assets/post_pics/mike.png">

- **Annuity**: An annuity is a stream of **constant**, equally spaced, payments over a certain period of time. 就是说上面那个C不管经过多少年都是不变的


	$$
		\begin{aligned}
		& \text{计算这个annuity的方法很简单，就是做了下化简} \\
		& \frac{C}{r}(1-\frac{1}{(1+r)^{T}}) \\
		& \text{其中T指的是这种payment会持续到最久的年份（基数词的最后一个）}
		\end{aligned}
	$$

- **Perpetuity**:指的是一种永远也不会停止的annuity，也就是说T趋于无穷，那么括号里面的term就会趋于1，那么最后的presnet value就是简单的\\( \frac{C}{r} \\)

#### Net Present Value

- **An important use of present value is to compare benefits to costs.**

- **Net present value(NPV) is the difference between the present value of the stream of benefits and the upfront cost that musht be incurred.**

	$$
		\begin{aligned}
			& NPV  = -C_{0} + \frac{C_1}{(1+r)} + \frac{C_2}{(1+r)^{2}} + .... + \frac{C_{T}}{(1+r)^{T}}
			& \text{其中c0指的就是一开始的成本，而后面的c1啥的都是之后可以赚到的钱}
		\end{aligned}
	$$

#### Presnet value, future value and the optimal consumption choice problem

- 其实这里的东西很多都跟上面的borrowing and lending有关，所以直接跳到上面去

### 5.5 The Choice of labor and leisure

- We use that model to examine a consumer's choice of how much to work

#### As wages rise, leisure first decreases, then increases

- 假设一天被分成了：work和leisure，work赚到花在leisure上的income

- Assumption:
	- L代表了花在了leisure上的时间(hours)
	- w代表了每小时赚来的钱
	- 所以日收入是w(24-L)
	- 收入可以用来买composite good
- 消费者的效用值基于花在leisure上的时间和能买多少good

<img src="assets/post_pics/Snipaste_2020-06-08_16-38-14.png">

- 斜率都是-w，可以观察到的趋势是当工资上升（从5-15），number of hours of leisure fall；但是观察得到，当工资持续上涨，那么花在leisure上的时间会变多

#### The Backward-bending supply of labor

<img src="assets/post_pics/Snipaste_2020-06-08_16-50-48.png">

- **An increase in the wage rate reduces the amount of work required to buy a unit of the composite good, and this leads to both a substitution effect and an income ef- fect. **

- 可以这么理解：leisure和labor完全是对立的关系，而labor和composite good却不是对立的关系，所以可以看出leisure和composite good是对立的关系。那么为什么替代效应和收入效用会带来影响呢？在这个场景里面，出了wage rate其他的东西都不会变化，那么当wage上升，就会有一些东西在变化
	- 在这里的替代效应：当wage上升的时候，bl必定向y正方向移动，也就是说此时能够购买的composite商品就变多了（这个的效果和我们把composite good的价格降低是一样的效果），那么这个时候对于composite good来说，其替代效应是正的，因为为了维持原有的效用，他可以买更多的composite good，而这个正替代效应，将会：induce the consumer to substitute more of the composite good for leisure，这和前面的是一样的
	- 但是同时，income effect收入效应会导致另外一种情况，那么就是因为leisure是normal good，工资上升自然意味着收入上升，所以人们会想要扩大自己的leisure的时间
	- 两个方向完全不一样的效用导致了这种恶心的曲线

<img src="assets/post_pics/Snipaste_2020-06-08_17-09-22.png">

- In sum, the labor supply curve slopes upward over the region where the substitu- tion effect associated with a wage increase outweighs the income effect, but bends backward over the region where the income effect outweighs the substitution effect.

<img src="assets/post_pics/Snipaste_2020-06-08_17-14-15.png">
