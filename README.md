# 设计模式
	**创建型模式**
> 速记：ABFPS

1. 抽象工厂 Abstract Factory 对象创建型模式
**意图**
> 速记：提供一个
提供一个创建一系列相关或相互依赖对象的接口，而无需指定它们具体的类。
**结构**
[image:3C62471B-0D7B-4BC1-8593-E93426C9175B-7015-000011C6606AEFD4/B92229ED-D217-4E7A-978A-6E1B4A43E993.png]
**参与者**
AbstractFactory
	* 声明一个创建抽象产品对象的操作接口
ConcreteFactory
	* 实现创建具体产品对象的操作
AbstractProduct
	* 为一类产品对象声明一个接口
ConcreteProduct
	* 定义一个将被相应的具体工厂创建的产品对象。
	* 实现 AbstractProduct 接口。
Client
	* 仅使用由 AbstractFactory 和 AbstractProduct 类声明的接口。

2. 生成器 Builder 对象创建型模式
**意图**
> 速记： 将一个
将一个复杂对象的构建与它的表示分离，使得同样的构建过程可以创建不同的表示。
**结构**
[image:4ECD5662-E5C7-446A-AFF6-29585C64A094-7015-0000120AB96C6D00/CB94669F-6991-48BB-ADD4-5CF22000FF2E.png]
**参与者**
Builder
	* 为创建一个 Product 对象的各个部件指定抽象接口
ConcreteBuilder
	* 实现 Builder 的接口以构造和装配该产品的各个部件。
	* 定义并明确它所创建的表示。
	* 提供一个检索产品的接口。
Director
	* 构造一个使用 Builder 接口的对象。
Product
	* 表示被构造的复杂对象。ConcreteBuilder 创建该产品的内部表示并定义它的装配过程。
	* 包含定义组成部件的类，包括将这些部件装配成最终产品的接口。

3. 工厂方法 Factory Method 对象创建型模式
**意图**
> 速记：定义一个
定义一个用于创建对象的接口，让子类决定将哪一个类实例化。Factory Method 使一个类的实例化延迟到其子类。
**结构**
[image:FAD19BA4-28D3-4194-BFE1-3380F1C0410B-843-00000C54BD340AB0/2E45871B-09B2-404C-A153-6A5CFD06E751.png]
**参与者**
Product
	* 定义工厂所创建的对象的接口。
ConcreteProduct
	* 实现 Product 接口
Creator
	* 声明工厂方法，该方法返回一个 Product 类型的对象。Creator 也可以定义一个工厂方法的缺省（默认）实现，它返回一个缺省的 ConcreteProduct 对象。
	* 可以调用工厂方法以创建一个 Product 对象。
ConcreteCreator
	* 重定义工厂方法以返回一个 ConcreteProduct 实例。

4. 原型 Prototype 对象创建型模式
**意图**
> 速记：用原型
用原型实例指定创建对象的种类，并且通过拷贝这个原型来创建新的对象。
**结构**
[image:21201D1B-9920-412A-8A8F-6FE373D37AFF-843-00000CA4122F9F33/6290A4C9-B99E-4564-BE8F-6C7C4FD089A5.png]
**参与者**
Prototype
	* 声明一个克隆自身的接口。
ConcretePrototype
	* 实现一个克隆自身的操作。
Client
	* 让一个原型克隆自身从而创建一个新的对象。

5. 单例 Singleton 对象创建型模式
**意图**
> 速记：保证一个类
保证一个类仅有一个实例，并提供一个访问它的全局访问点。
**结构**
[image:C9D9A167-A652-42CA-A598-C28F60C91A6C-843-00000CBFC2296D6F/4E0E7E37-AADF-4C68-BB34-43E8C4609CCE.png]
**参与者**
Singleton
	* 定义一个 Instance 操作，允许客户访问它的唯一实例。Instance 是一个类操作（类方法或静态成员函数）。
	* 可能负责创建它自己的唯一实例。

**结构型模式**
> 速记： ABCDFFP

1. 适配器 Adapter 类对象结构型模式
**意图**
> 速记：将一个类
将一个类的接口转换成客户希望的另外一个接口。Adapter 模式使得原本由于接口不兼容而不能一起工作的那些类可以一起工作。
**结构**
类适配器使用多重继承对一个接口与另一个接口进行匹配。
[image:09744365-6839-4851-BFEF-016A5D837E35-843-00000CF3C8909A31/2131A650-C5F3-43B1-9987-4C1461B78AD4.png]
对象适配器依赖于对象组合。
[image:24EFBF66-D1B7-4A8E-BBB8-BA81A44691A7-843-00000D033EDA343D/37260135-1788-4602-89AC-3792F825F448.png]
**参与者**
Target
	* 定义 Client 使用的与特定领域相关的接口。
Client
	* 与符合 Target 接口的对象协同。
Adaptee
	* 定义一个已经存在的接口，这个接口需要适配。
Adapter
	* 对 Adaptee 的接口与 Target 接口进行适配。
		
2. 桥接 Bridge 对象结构型模式
**意图**
> 速记：将抽象部分
将抽象部分与它的实现部分分离，使他们都可以独立地变化。
**结构**
**参与者**
		
3. 组合 Composite 对象结构型模式
**意图**
> 速记：将对象组合
将对象组合成树形结构以表示“部分-整体”的层次结构。Composite 使得客户对单个对象和复合对象的使用具有一致性。
**结构**
**参与者**
		
4. 装饰 Decorator 对象结构型模式
**意图**
> 速记：动态地给
动态地给一个对象添加一些额外的职责。就扩展功能而言，Decorator 模式比生成子类方式更为灵活。
**结构**
**参与者**
	
5. 外观 Facade 对象结构型模式
**意图**
> 速记：为子系统
为子系统中的一组接口提供一个一致的界面，Facade 模式定义了一个高层接口，这个接口使得这一子系统更加容易使用。
**结构**
**参与者**
	
6. 享元 Flyweight 对象结构型模式
**意图**
> 速记：运用共享
运用共享技术有效地支持大量细粒度的对象。
**结构**
**参与者**
	
7. 代理 Proxy 对象结构型模式
**意图**
> 速记：为其他
为其他对象提供一个代理以控制对这个对象的访问。
**结构**
**参与者**
	
**行为型模式**
> 速记：职命解迭中、备观状策模访
	
1. 职责链 Chain of Responsibility 对象行为型模式
**意图**
> 速记：为解除
为解除请求的发送者和接收者之间的耦合，而使多个对象都有机会处理这个请求。将这些对象连成一条链，并沿着这条链传递该请求，直到有一个对象处理它。
**结构**
**参与者**

2. 命令 Command 对象行为型模式
**意图**
> 速记：将一个请求
将一个请求封装成一个对象，从而使你可用不同的请求对客户进行参数化；对请求排队或记录请求日志，以及支持可取消的操作。
**结构**
**参与者**

3. 解释器 Interpreter 类行为型模式
**意图**
> 速记：给定一个语言
给定一个语言，定义它的文法的一种表示，并定义一个解释器，该解释器使用该表示来解释语言中的句子。
**结构**
**参与者**
		
4. 迭代器 Iterator 对象行为型模式
**意图**
> 速记：提供一种方法
提供一种方法顺序访问一个聚合对象中各个元素，而又不暴露该对象的内部表示。
**结构**
**参与者**
		
5. 中介者 Mediator 对象行为型模式
**意图**
> 速记：用一个中介
用一个中介对象来封装一系列的对象交互。中介者使各对象不需要显式地相互引用，从而使其耦合松散，而且可以独立地改变它们之间的交互。
**结构**
[image:12147135-FC18-4D5A-BB31-DAC44ECA4383-843-00002C866E395F77/4A4F763D-6FD0-4975-AAA2-E126EAEE8604.png]
**参与者**
Mediator（中介者）
	* 中介者定义一个接口用于与各同事（Colleague）对象通信。
ConcreteMediator（具体中介者）
	* 具体中介者通过协调各同事对象实现协作行为。
	* 了解并维护它的各个同事。
Colleague class（同事类）
	* 每一个同事类都知道它的中介者对象。
	* 每一个同事对象在需与其他的同事通信的时候，与它的中介者通信。
		
6. 备忘录 Memento 对象行为型模式
**意图**
> 速记：在不破坏
在不破坏封装性的前提下，捕获一个对象的内部状态，并在该对象之外保存这个状态。这样以后就可将该对象恢复到保存的状态。
**结构**
**参与者**
		
7. 观察者 Observer 对象行为型模式
**意图**
> 速记：定义对象
定义对象间的一种一对多的依赖关系，以便当一个对象的状态发生改变时，所有依赖于它的对象都得到通知并自动刷新。
**别名**
依赖、发布-订阅
**结构**
[image:9C5AEC1F-59E7-4164-85DF-97D33D266AF9-843-00002C128F607CEE/7A31D13F-8AEF-4635-9988-43B7FD4F8D8B.png]
**参与者**
Subject（目标）
	* 目标知道它的观察者。可以有任意多个观察者观察同一个目标。
	* 提供注册和删除观察者对象的接口。
Observer（观察者）
	* 为那些在目标发生改变时需获得通知的对象定义一个更新接口。
ConcreteSubject（具体目标）
	* 将有关状态存入各 ConcreteObserver 对象。
	* 当它的状态发生改变时，向它的各个观察者发出通知。
ConcreteObserver（具体观察者）
	* 维护一个指向 ConcreteSubject 对象的引用。
	* 存储有关状态，这些状态应与目标的状态保持一致。
	* 实现 Observer 的更新接口以使自身状态与目标的状态保持一致。

		
8. 状态 State 对象行为型模式
**意图**
> 速记：允许一个
允许一个对象在其内部状态改变时改变它的行为。对象看起来似乎修改了它所属的类。
**结构**
**参与者**
		
9. 策略 Strategy 对象行为型模式
**意图**
> 速记：定义一系列
定义一系列的算法，把它们一个个封装起来，并且使它们可相互替换。本模式使得算法的变化可独立于使用它的客户。
**结构**
**参与者**
		
10. 模板方法 Template Method 类行为型模式
**意图**
> 速记：定义一个操作
定义一个操作中的算法骨架，而将一些步骤延迟到子类中。Template Method 使得子类可以不改变一个算法的结构即可重定义该算法的某些特定步骤。
**结构**
**参与者**
		
11. 访问者 Visitor 对象行为型模式
**意图**
> 速记：表示一个
表示一个作用于某对象结构中的各元素的操作。它使你可以在不改变各元素的类的前提下定义作用于这些元素的新操作。
**结构**
**参与者**

	- [ ] 1.5 组织编目
模式依据其目的可分为创建型（Creational）、结构型（Structural）、行为型（Behavioral）三种。
**创建型模式**
> 速记：创建型模式“与”
创建型模式与对象的创建有关；
**结构型模式**
> 速记：结构型模式“处理”
结构型模式处理类或对象的组合；
**行为型模式**
> 速记：行为型模式“对”
行为型模式对类或对象怎样交互和怎样分配职责进行描述。

第二是范围准则，指定模式主要是用于类还是用于对象。
**类模式**
> 速记：类模式处理”类”
类模式处理类之间的关系，这些关系通过继承建立，是静态的，在编译时刻便确定下来了。
**对象模式**
> 速记：对象模式处理“对象”
对象模式处理对象间的关系，这些关系在运行时刻是可以变化的，更具动态性。

**创建型类模式**	
> 速记：创建型类模式将…延迟到子类
创建型类模式将对象的部分创建工作延迟到子类。
**创建型对象模式**
> 速记：创建型对象模式将…延迟到另一个对象中
创建型对象模式将对象的部分创建工作延迟到另一个对象中。

**结构型类模式**
> 速记：结构型类模式”使用”
结构型类模式使用继承机制来组合类。
**结构型对象模式**
> 速记：结构型对象模式”描述”
结构型对象模式描述了对象的组装方式。

**类行为型模式**
> 速记：行为型类模式使用
类行为型模式使用继承描述算法和控制流。
**对象行为型模式**
> 速记：行为型对象模式描述
对象行为型模式描述一组对象怎样协作完成单个对象所无法完成的任务。

#设计模式/设计模式整理
