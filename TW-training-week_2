#TW-Training
##*The second week in ThoughtWorks.*

###杨楠晨 2016 年 3 月 5 日

##TASKING
**Tasking** 是保证能够高质量完成一个 Story 的有效行为，其为思维逻辑的实体表现方式。

* 如何来进行 Tasking？<br/>
当我们需要完成一个 Story 时，首先需要对其进行具体的分析：接收到的信息和输出的信息之间的关系、这个 Story 的主体目标是什么、数据之间的依赖关系等等。通过**正向推导**或者**逆向推导**来设计整个 Story 的执行流程。<br/><br/>
**管道思维** 是一种很好的思维方式用来 Tasking，其具体的表现形式为：由一串具有 Input(输入)、Output(输出)、Process(过程) 的模块连接而成，每一个组件的 Input 是上一个组件的 Output，每个组件之间相互独立，不能产生跳跃。Input 和 Output 有具体的 name 和 structure，Process 有具体的 name。Input、Output、Process 都是穷尽的 —— 明确、清晰。<br/>
	* 习惯大 Task 的分割
	* 理解缩放的概念
	* 高内聚 低耦合
* 如何保证 Tasking 产生的质量？<br/>
	* Tasking 过程中遵循一定的思维框架，如：6W2H（What, Where, When, Why, Who, Which, How, How much）
	* Tasking 结束后进行检查：交叉检查、逆向验证等

##UNIT TEST（单元测试）
###*代码即描述，测试即文档*
* 何时、何故需要写单元测试？
	* 完成一个特性（Feature）的编码并且想确保它能够按照预期工作
	* 文档记录
	* 修改代码 => 不会破坏已经存在的行为
	* 了解当前系统中的行为
	* 第三方代码的行为期望

	单元测试 => 集成测试 + ETE(End-to-End) 测试 = 保证端对端的行为
* 如何正确地书写测试？
	* AAA 原则
		* Awange：整理测试所需要的条件
		* Act：执行
		* Assert：断言（判断是否符合预期）
			* **Tip**：写断言时慎用不靠谱的预期目标
	* Give-When-Then 结构（描述 TestCase 的语言结构）
		* `givenSomeContextWhenDoingSomeBehaviorThenSomeResultOccurs`
		* `given_some_context_when_doing_some_behavior_then_some_result_occurs` -- Snack 命名法（下划线命名）
		* `whenDoingSomeBehaviorThenSomeResultOccurs`
		* `someResultOccursWhenDoingSomeBehavior`
		* `some_Result_Occurs_When_Doing_Some_Behavior`
	* Class 命名：`ClassName_ClassFunction_ClassFunctionParameter`

	测试在组织和书写方面追求的终极目标是：**无限接近言简意赅的自然语言化文档**。
	
	测试行为而不是方法：测试一个类的全部行为的集合，而不是它的每一个独立的方法。
* 什么是好的测试？
	* FIRST 原则
		* First => 足够快
		* Isolated => 相互隔离（SRP）
		* Repeatable => 可复验
		* Self-Validating => 自确认
		* Timely => 足够及时
	* Right-BICEP 原则
		* Right => 结果是正确的吗？—— 明确行为 Happy-Path
		* Boundary Conditions => 边界条件是否都正确？
		* Inverse Relationships => 能否检查反向关系（等价关系）？
		* Cross-Check => 能否用其它手段对结果进行再确认？
		* Error Conditions => 能否强制触发错误条件？—— Sad-Path
		* Performance => 性能特性是否在允许范围内？—— 一般由基于集成的测试方法来检测
* 如何确定测试边界？<br/>
CORRECT 原则
	* Conformance => 一致性
	* Ordering => 有序性（值的顺序是否符合预期？）
	* Range => 区间性
	* Reference => 引用性/耦合性
	* Existence => 存在性
	* Cardinality => 基数性（计数性）—— 是否恰好有足够的值？
	* Time（Absolutely and Relatively） => 时间性

##TEST DOUBLE（测试替身）
*有时候对 SUT（被测系统）进行测试是很困难的，因为它依赖于其他无法在测试环境中使用的组件。这有可能是因为这些组件不可用，它们不会返回测试所需要的结果，或者执行它们会有不良副作用。在其他情况下，我们的测试策略要求对 SUT 的内部行为有更多控制或更多可见性。*

*如果在编写测试时无法使用（或选择不使用）实际的 DOC（依赖组件），可以用测试替身来代替。测试替身不需要和真正的 DOC 有完全一样的行为方式：他只需要提供和真正的组件同样的 API 即可，这样 SUT 就会以为它是真正的组件！*

*-- Gerard Meszaros*

* Dummy => 伪对象(代替空值或者新的对象)  SUT -> DOC
* Test Stub => 伪对象 DOC -> SUT
* Test Spy => 验证 DOC 行为是否符合预期
* Mock Object => 有意义的伪对象（符合要求）
* Fock Object => 打酱油 -> 为了让代码顺利通过

##干货
* CODELF => 起名神器
* thefuck => terminal 插件
* spectrum
* gitignore.io
* hamcrest => 断言语义化工具