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
- 在一个竞争市场里面，平衡点出现在当市场clears的时候，即是需求曲线=供给曲线的时候
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
