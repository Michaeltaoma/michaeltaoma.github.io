---
layout: post
updated: 2020-05-13 16:29
description: My Economics note
---
## Chapter 1
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
	- Set of constrains
- 所以其实Objective function就一个简单的目标值足矣
- 然后textbook举了个例子来阐述constrained optimization是怎样把人们从不明显的错误中给纠正过来，个人认为是废话。不过课本根据这个问题提出了经济学上的一个重要观点：***The solution to any constrained optimization problem depends on the marginal impact of the decision variables on the value of the objective function.***这句话的意思就是变量对于价值的边际影响决定了cop的答案，边际影响值得是每提高一个unit的变量，价值的改变是多少。
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
- Positive analysis attempts to explain how an economic system works and to predict how the endogenous variables will change as exogenous vari- ables change. Normative analysis considers prescriptive questions such as “What should be done?” Normative studies introduce value judgments into the analysis.
