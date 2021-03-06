# Quantstamp: 智能合约安全协议

**Quantstamp是第一个智能合约安全审计协议。** 我们用可以确保智能合约安全性的技术来拓展Ethereum。我们的团队是由一群软件测试专家组成，总共超过500个谷歌学者引用。

## 问题
区块链网络是安全的，但是智能合约并不安全。2016年6月，黑客从DAO项目中盗取了价值5500万美元的币，原因是智能合约中的一个bug。2017年7月，有黑客从加密公司盗取了价值超过3000万美元的令牌，只因为Parity钱包的智能合约代码中的一个单词错误。这些安全问题损坏了对智能合约的信任，进一步也阻碍了Ethereum网络被更广泛地使用。

当前人们对审计智能合作做的很不充分。从事安全咨询的公司需要人工专家去审核智能合约。这种处理方式昂贵且容易出错。并且依赖于一个公司，需要相信公司中没有任何坏角色。一个依赖于多种不同角色共识的分布式系统显著地更为安全。

人工审计的处理方式，无法应对智能合约的爆炸式增长。2017年6月到10月，智能合约的数量，从50万增长到了200万。我们可以预期1年内会增长为1000万。这对审计工作会有指数级的增长。如今我们没有足够的安全专家来审计所有的智能合约，并且这个短缺未来会更为严峻。

智能合约失败的潜在代价也会增长。仅仅2017年10月，约有32亿美元(1100万ETH)在智能合约中锁定这。而锁定在智能合约中的美元会随着Ethereum和智能合约使用的增长而指数级增长。智能合约中漏洞的潜在带带也会相应增长。

## Quantstamp协议

Quantstamp协议通过创建可伸缩低成本的系统审计所有Ethereum网络的网络的智能合约，来解决智能合约的安全问题。随着时间的推移，我们希望每一个Ethereum智能合约都使用Quantstamp协议来执行安全审计，安全是最基本的。  

协议包含两部分：
- 一个自动且可升级的软件验证系统，用于检查Solidity程序。分布式SAT求解器会需要大量的算力，但随着时间推移，会捕获到更为复杂的攻击。
- 一个自动的赏金支付系统，用于奖励查找合约bug的人工参与者。这个系统的目的，是桥接起通往全自动化目标的隔阂。

Quantstamp协议依赖于参与者们的分布式网络，来减轻坏角色的作用，提供所需的算力，还有提供治理。每一个参与者都使用Quantstamp协议（QSP）令牌来支付，接收，或者提高验证服务。下面是不同类型的参与者。

- **贡献者** 为Solidity验证程序贡献软件，然后获得QSP令牌。所有贡献的带慕都会开源，这样社区可以对效率有所信任。绝大部分的贡献者将会是安全专家。贡献是通过治理机制来投票的。
- **验证器** 运行Quantstamp验证节点并获得QSP令牌。验证着只是贡献计算资源，不需要是安全专家。
- **bug寻找者** 提交智能合约bug，获得QSP令牌作为赏金。
- **合约创建者** 支付QSP令牌验证以验证智能合约。由于智能合约的数量在爆炸式增长，我们预计合约穿件这的需求也会相应增长。
- **合约使用者** 可以查看智能合约的安全审计结果。
- **投票者** 官职系统是协议的一个核心特性。验证被设计为模块化的并且可以基于令牌持有者的投票来升级。治理机制减少了升级分叉的可能性，也会随着时间推移，去中心化创建团队的影响。

## 技术路线

2017 | &nbsp;
---|---
6月 | Richard和Steven创立Quantstamp
7月 | Parity钱包被黑几天后建立Solidity静态分析原型
8月 | 发布第一版白皮书
9月 | 聘到Ed，Krishna，Vajih，Leo
10月 | 完成[Request Network](https://request.network/)的半自动审计 <br/> 创建自动松露测试发生器  <br/> 与另一个公司完成第2个半自动审计
11月 | 与另一个公司完成第3个半自动审计 <br/> QSP令牌启动 <br/> 与滑铁卢大学开始大学合作
12月 | 在Ethereum上构建Quantstamp验证/付款智能合约 <br/>完成第4次半自动审核
**2018** | &nbsp；
1月 | 构建Quantstamp验证节点（增强的Ethereum节点）
2月 | 将v1版本的分析软件添加到验证节点，返回审计证明散列值和原始输出 <br/> 用v1版本的分析软件完成第5次半自动审核
3月 | 开始测试阶段和改进加密经济激励措施 <br/> 为可升级协议实现令牌持有人治理系统
4月 | 在系统测试验证后部署到测试网络 <br/> 实现可升级协议的令牌持有人治理系统
5月 | 举报第1次Quantstamp黑客马拉松
6月 | 与合作伙伴开展智能合约保险工作
7月 | 经过几个月的测试和修正之后，为主网举办令牌持有人投票
8月 | 发布主网v1
9月 | 开始用拜占庭容错为主网v2开发分布式的SAT共识
10月 | 在主网智能合约上添加智能合约保险alpha产品

## 动机

我们的团队致力于帮助开发人员编写更可靠的代码，我们代表了在软件验证领域多年的学术研究和实战经验。有机会将这些专业知识应用于下一代数字技术革命，对每个人来说都是非常激动人心的。对于更安全的代码，也有着明确而迫切的需求。

智能合约的漏洞已经威胁到区块链技术和数字货币的应用。目前正在进行大量的工作是用来以扩大Ethereum的规模，然而我们认为安全同样重要。没有安全性的智能合约没有安全性，很难获得人们的信任，除非是风险投资。我们对未来的展望是智能合约会成为人们使用的主流应用程序，并且会使人们的日常生活更便捷。我们将采用可确保智能合约安全性的技术来扩展Ethereum，从而实现智能合约的愿景。

我们相信自动化的安全审计将帮助开发人员部署公众可以信任的代码，而无需编写包含比程序本身更多代码的正式规范。我们的目标是尽可能地将检查和属性验证自动化。这些目标中的每一个都应该有助于实现一个更健康的区块链生态系统，这个解决方案是解决决基础设施层面的问题。 
 
我们的策略是创建一个基础协议，最终可以直接并入Ethereum平台，为第一个Ethereum杀手级应用创造一个安全的环境。 
 
本文档的其余部分详细说明了为什么安全协议是必要的技术先进性，并提供平台的高层次架构。 

## 智能合约改进

### 我们如何改进智能合约架构

该协议允许对智能合约代码进行自动安全检查，并以一个不依赖第三方的方式执行。我们的方法有以下两个优势。

1. 协议允许终端用户直接提交用于验证的程序，并且审计结果不会被坏人操纵。

想象一下，安全审计公司的坏人放过了一个几百万美元的bug，然后可以等合约上线之后获取利益。Quantstamp协议所需的共识减轻了这些基于经济利益驱动的坏人的影响——要操纵结果的成本是相当大的。完成验证的智能合约会携带一个审计证明的散列值，里面包含了验证库的版本，还有基于共识的文本报告。未来，我们计划与第三方合作提供智能合约保险，以进一步降低使用智能合约的风险。

2. 我们将智能合约的验证和证明做为Ethereum验证节点软件的一部分，以此激励旷工

在一个区块链架构中，“矿工”是向链内添加交易的参与实体。在Quantstamp协议中，矿工被称为验证者。验证者需要运行验证节点软件，该软件在Quantstamp校验合约上监视更新。执行服务的费用使验证者诚实可信。验证者执行合约验证，生成散列值，然后获得令牌费用作为回报。如果验证者发现合约违反了安全目标，他会作为违规行为的证人会提出一个反例，同时托管的智能合约会向验证者支付奖金。开发人员负责在漏洞被找到后解决漏洞，他们可以在涉及真正的经济利益之前解决这个漏洞。

### 我们如何改进开发人员流程

善意的软件开发人员需要别人的帮助来生产更好的代码。Luu etal指出，存在一种语义上的差异，这种差异植根于对代码如何在区块链中执行的误解。因此，迫切需要更好的工具，可以帮助开发人员在部署之前捕获漏洞。目前开发人员测试代码的方式——手动地通过开放的代码评审和单元测试(如果他们是勤奋的)——是不足以满足区块链技术的需求的，这技术只会在理想情况下提供了完美的安全性。以上所有方法都是非常手工的方法，会有人为的错误。我们需要一个简单流程来验证智能合约，同时尽可能减少被破解之后产生严重漏洞的可能性。Quantstamp协议提供了简单的接口，可以在区块链上证明开发人员执行安全审计，进而保护了开发人员的声誉。  

![image](https://github.com/yajiya/quantstamp-summary/blob/master/pics/process.jpg)

### Quantstamp示例

假设开发人员计划在Ethereum上部署一份Solidity编写的智能合约。在编写代码访问货币系统时存在很大的风险，开发人员必须小心确保没有因漏洞而丢失资金。为了最小化风险，开发人员通过Quantstamp的Ethereum智能合约直接从钱包提交他的代码，发送QSP令牌以执行安全审计，源代码含在data字段中。根据程序的安全需求，开发人员可以决定发送多少赏金。然后，智能合约接收到请求，并在下一个Ethereum区块验证节点上，执行一组安全检查来验证智能合约。取得共识后，审计证明和报告数据与相应的令牌支付一起添加到再下一个Ethereum区块。报告按照严重程度从1-10将问题分类；1是轻微警告，10是重大漏洞。从这一时刻起，如果没有立即检测到严重的漏洞，那么赏金就会一直被合约锁定，直到经过指定的时间。时间结束时，赏金将返回给请求审计的开发人员。在申请审计时，开发人员可以选择公开或隐秘安全报告。隐秘的报告使用智能合约的公钥加密，可以由合约所有者/开发人员解密。开发人员和公众可以访问一个名为qsscan.io的站点查看任何安全报告。站点通过Quantstamp智能合约对交易data字段中的信息进行解析并显示。通过使用审计证明散列值，公众看到的安全报告与经过审计的源代码完全匹配，以防止对报告结果的操纵。

在发布公开审计之前，开发人员可以在本地机器上执行安全审计，但是可能发现计算开销过高。与普通的开发人员机器相比，在内存和处理核心方面，Quantstamp验证节点的计算能力可能更强。同时，通过丰厚赏金来聚集人类黑客力量，这样这个项目能够远远超过标准代码审查的覆盖范围。代码准备部署时，开发人员会很乐意生成一个公共安全报告，以便让用户放心，合约已经执行过离散的安全审计。

当安全报告识别出智能合约中发现的问题时，开发人员可以在qsscan.io公开地注释和反馈。这样，开发人员就能够在报告中标记误报，社区可以验证注释。

Quantstamp并不能保证完美的源代码，但是通过使用自动化和众包方法，提供了更高级别的安全保障。Quantstamp团队承诺会不断地进行研究和开发，定期对安全库进行改进。当有新版本发布时，开发人员可以重新审计他们的智能合约，展示他们对保护代码和增强公众信心的承诺。  

非开发人员将对项目有更多的信心，因为他们可以看到智能合约开发人员是否已经审计过代码，以及审计了哪个版本。

## 技术

实施安全审计的技术建立于对验证算法和区块链技术的前沿研究。其基础是由Quantstamp开发的验证节点，被深度修改过的Ethereum节点，其中包括采用常规方法技术的分析工具包。

### 验证协议

本安全审计的验证协议会奖励提供计算资源来执行智能合约检查的参与者。这些检查由验证器节点运行。该验证协议确保对智能合约的认证是“审计证明”的一部分。

通过引入一个基于Ethereum的中介托管/治理智能合约，系统可以确保计算费用的交易安全。如果接正在接收的智能合约未通过验证器的验证，托管器将持有交易直到验证完成。如果验证失败，令牌被自动返回发送者或持有直至安全违例被修正。
Quantstamp节点是Ethereum网络的合作伙伴。Ethereum处理网络和交易协议，而Quantstamp节点处理验证协议，以确保安全审核并将其添加到数据字段或交易。

#### 设计

本验证协议处理算力分发和共识。这个协议指明网络节点如何执行自动化软件验证，以及漏洞赏金的奖励机制。

我们协议的核心价值主张在于其去信任并阻止坏人操纵审计结果。它也可以通过QSP令牌的去中心化治理进行升级。这就是我们如何设计协议以实现这些目标。

##### 协议自治

我们计划将Quantstamp协议设计为具有自治系统的可升级协议，并且由QSP令牌持有者控制。自治系统控制校验合约和验证节点的升级。校验合约被设计为模块化和可升级的。如发展路线图所详述，在实现核心功能后，自治系统本身将被添加到合约中。

一个时间锁定的多重签名被用于自治升级。在提出的途径中，任何成员都可以发起升级交易，交易被越多成员批准，就能越早执行。成员可以投票反对升级，这意味着他会退出一项其他人通过的签名。已经全部成员通过的升级可以在1小时后执行。每5％成员不投票，所需时间翻倍；如果投票反对则增加四倍。

自治是一个关键的功能，因为验证者和贡献者需要升级协议。自治机制降低升级分叉的可能性，允许协议兼顾贡献者升级和确保用户间的一致性。随着时间的推移和新贡献者的加入，去中心化的治理特征允许社区参与并稀释创始团队的影响力。

例如：验证者想通过投票改变工作量贡献方式，为了增加收入的潜力。用户想要通过投票引入高并发的算法，让协议更快执行。

##### 加密经济激励

为了防止坏人操纵系统，我们构建了一个激励机制，其策略在于让发起攻击代价昂贵，以防止流氓验证节点改变审计结果。验证者通过QSP令牌中的交易费激励，处理一部分计算。所提议的协议要求拜占庭容错2/3。如果没有达到2/3的共识，则不支付令牌。我们保留在测试和验证阶段改进此设计的权利。以下部分将更详细地说明容错设计。

##### 对抗攻击与分布式计算

单一的坏人不能操纵网络，因为其他人会被经济激励，阻止攻击。 为了分配我们的算力，每个成员只收到一个整体验证问题的组成部分。对于算力分配，我们目前在考虑使用t-masking quorum系统，其中两个quorum在至少2t +1服务器中交互。该quorum系统可以处理至少有t个节点的故障系统。由于没有单一的人能够访问整个验证过程，所以通过运算处理的分配进一步阻止了坏人。

##### 囚徒困境

在游戏理论中，囚徒的困境是一个悖论，其中两个人以自己的利益为由选择了一种不会导致理想结果的行为。两者都选择牺牲另一方以使自己受益，但两者最终都比通过合作更糟。 

假设发现错误的验证者可以选择不获取赏金，并利用它来获取未来的收益。然而，我们的经济激励措施驱使验证者追求赏金，而不是试图利用错误。验证者若想试图利用错误而不是报告错误，必须假设没有其他验证者会发现同一个错误和报告它，并修复错误。由于难以协调的验证者数量很大，很可能是其他验证者会发现这个错误，然后去获得赏金。因此，该机制设计下，验证者在个人利益驱使下将追求赏金。

### 安全审计引擎

安全审计引擎采用一个未验证的智能合约作为输入，执行自动的安全漏洞检查并生成报告。验证结果会和一个proof-of-audit（审计证明）散列值结合起来，这个散列值会有一个版本代码，可以用于从这个版本的安全库追踪检查的范围。

在安全库中运行完整测试所需的时间与智能合约代码的复杂性相关，因此，验证奖励与计算时间成正比。验证者需要奖励来激励其参与这一过程，因此发行令牌让使用者可以使用这些功能。

当知道智能合约被通过共识的方式透明验证时，公众越来越有信心，从而激励开发人员使用这些特性。整体信心则会由于尝试找到重大bug的赏金猎人的努力得到进一步提升。

此外，随着新的漏洞被发现，安全库将会不断改进和发布新版本。用户将有机会用最新版本的安全库重新验证其使用的智能合约，确保他们的代码不会受到新发现的漏洞的攻击。这类似于软件用户下载补丁修复安全漏洞或用户更新其防病毒软件。

### 架构图

Quantstamp协议（QSP）是用于审计所有的基于Ethereum的智能合约项目的可扩展的系统。我们对Quantstamp安全协议的愿景是它将成为Ethereum协议其中的一部分。

QSP分为三个概念类别：

1.	基于Ethereum的Quantstamp校验合约
2.	由被高度修正的Ethereum节点组成的Quantstamp网络（QN）
3.	Quantstamp报告（数据承载于智能合约交易中）

QN是由验证者节点组成的网络，以共识的方式生成安全报告。作为一种效用，QSP与平台无关——安全库可以有许多变体，其中之一包括Solidity（用于Ethereum），以及可能涵盖其他不同平台的智能合约语言的变体。

![image](https://github.com/yajiya/quantstamp-summary/blob/master/pics/architectural-view.jpg)

#### Quantstamp校验智能合约

最终用户可以访问以下功能列表。

**register()**
用户可以注册一个Ethereum地址，该地址提醒Quantstamp网络，监控该注册地址的API调用。

**audit()**
用户可以为一个安全审计提交源代码以及令牌赏金费用。成功后，智能合约被数字签署以证明其通过严格的安全检查。同时也会生成一份加密的安全报告。bug赏金仍然在合约上，从而激励查找bug的人，直到到达指定的时间限制。

**upgrade()**
升级现有的智能合约。新版本的智能合约必须通过安全审计。现有的赏金向前滚动。


#### 基于以太坊的Quantstamp网络

Quantstamp网络（QN）是一种专用协议，能够监视一个注册过的智能合约上相关的交易，这个合约会的涉及Quantstamp校验合约调用。

#### Quantstamp报告

 “Quantstamp报告”提供了QN执行的安全审计的公开视图。这些报告将通过qsscan.io上的基于Web的用户界面展示。

报告可以是公共的或私人的。每个人都可以看到并阅读到公共报告。注册用户则可以用公共密钥对私人报告进行加密，只有注册用户可以阅读报告的内容。一旦智能合约被部署，智能合约的最终安全报告是公开的。这样可以让投资者和其他用户在提交资金前查阅这些报告。

智能合约的所有者被鼓励在安全报告中加入注释。智能合约所有者被鼓励对所有已发布的安全警告和被标记的问题进行回复。答复可能是简单的“这是误报”或“我们不关心这个问题”，也可能是非常详细的。所有者的责任是向那些想要阅读安全报告来提高信任度的人提供尽可能多的信息。 基于对在安全报告中的发现、赏金的额度、赏金已经生效时间的长度以及社区的反馈，每个智能合约都将被计算得到一个“信任评分”。

### 谍报

在现实世界中，同行评审和单元测试是在用的主要的软件验证技术。尽管同行评审是一种有效的方法，但它仍然容易出现人为错误，手工测试在覆盖范围和边界上总是有限的。采用自动推理工具进行软件验证有助于缩小差距。尽管自动推理工具的研究几十年前就已经开始，但在过去几年里，它们的实际重要性才迅速发展。

安全审计引擎建立在基于离散数学，逻辑和计算机科学研究的工具和技术的*谍报*之上。它与安全库进行交互，安全库提供对安全检查（待执行）和属性（待验证）的访问。

我们下面总结支持安全审计引擎的谍报。

#### 计算机辅助推理工具

计算机辅助推理工具，如SAT/ SMT求解器（见下文），近年来对软件工程和安全性产生了巨大的影响。 在软件工程中采用求解器的关键原因是其性能和表现力在不断提升。

##### SAT求解器

SAT（可满足性）求解器支持软件验证工具。 计算机程序被建模为布尔公式，然后传递给求解器。 在为特定条件建模程序行为和测试时，可以构造一个布尔公式，满足赋值的条件存在，则意味着存在bug。 如果SAT求解器可以找到解决方案，则报告“可满足”，否则，报告“不可满足”。

SAT求解器是软件工程好几个领域的重要工具，包括软件验证，程序分析，程序合成和自动化测试。其他应用程序涉及各种问题领域，包括电子设计自动化，计算机辅助设计及其他。 SAT求解器效率惊人，结合了决策启发，演绎推理和各种各样的实验性的验证技术。

##### SMT求解器

SMT求解器是一种可以将各种一阶理论结合一起的可满足性公式工具。 它是SAT求解器的泛化，可以处理比命题逻辑更丰富的理论。 通用的一阶理论，可以对计算机代码片段的漏洞分析建模，包括等式，位向量，数组，理性，整数和差分逻辑。 这是一个非常活跃的研究领域，有很多应用：软件验证，编程语言，测试用例生成，规划和调度等。 众所周知的SMT求解器包括Yices（SRI），Z3（Microsoft），CVC3（NYU，Iowa），STP（Stanford），MathSAT
（U.Trento，Italy），Barcelogic（Catalonia，Spain）。
 
#### 模型检验

模型检验是基于代码行为以特定方式进行抽象，这通常会导致发现不一致。 这种技术以强力的方式探索所有可能的系统状态。

与模型检验相反，有界模型检验（BMC）是用于验证给定属性（通常表示为用户的断言）在给定边界数字k，程序在约束的执行路径执行路径边界内循环迭代和递归调用，来寻找bug。 使用SAT求解器布尔可满足性问题，可以减少这类问题。

有界模型检验的实用性部分地得到*小范围假设*的支持。 这个假设指出，大多数错误具有很小的反例，并且已被证明是在软件模型中查找错误的有效思想。 这个假设是名为的*轻量*的正式方法的基础。

#### 静态程序分析

静态分析确定程序的属性，不需要实际执行程序。自动化工具可以帮助程序员和开发人员进行静态分析。静态分析被用于查找潜在的空指针错误，并验证设备驱动程序是否全部满足API的使用要求。

#### 符号执行及Concolic testing

卷积测试是一种运行符号执行的混合软件验证技术，是将程序变量视为具体执行路径的符号变量的经典技术。 符号执行与自动定理证明器一起使用以生成新的测试用例，其主要重点是查找错误而不是证明正确性。


### 增量发布和订阅模型

安全库的软件发布版本，会有严重、主要和次要的版本标签。 当开发人员部署代码时，根据订阅支付模式，他们可以在合约上做标注，在严重/主要/次要的版本上，执行合约的重新验证。

对于非常财务敏感的合约，开发人员可以在所有版本上选择重新验证。 对于较不敏感的合约，只能在关键版本上选择重新验证。 当开发人员签署合约进行验证时，随后的验证失败，网络将通知他们，并可立即采取行动。

令牌交易费用的市场价格是平衡计算资源供应和经常性需求平衡的重要组成部分。因为令牌的市场价格是自由浮动的，所以去中心化的验证者节点会被市场力量驱动，动态地添置新资源来满足需求。

开发人员可以选择不订阅，因为他们对自己的程序有信心，不想支付订阅费用，但如果代码中存在重要漏洞，那么只能在软件更新一天后，才会发现漏洞。这样就存在一种可能，用旧的安全库验证过的合约已经部署到网络，后来却发现了漏洞。

### bug查找人

在开源软件中，通常开发人员寻找bug不会获得报酬。最近，Emin Gün Sirer在度假时发现BitGo的两个关键漏洞，并写了一封友好的电子邮件来提醒他们。在安全开发人员的通常经验中，他收到了一个没有感谢的答复，并且后来还被BitGo CTO责难。 QSP令牌的自动奖励奖励允许熟练的开发人员向验证者合约提交错误，并获得即时奖励和公众认可，而无需与公司交涉。

QSP令牌中的优惠，随同源代码发送到Quantstamp验证器智能合约，然后托管在合约中。 bug查找者可以使用任何手段来破解代码，如果合约中有重大漏洞被发现，合约中托管的错误奖励会授予验证者。验证器节点运行验证软件，可以验证提交的错误。

我们相信，通过在我们的平台上手动搜索公开的智能合约中的安全漏洞，熟练的开发人员可以纯粹通过错误发现赚取收入。 财务敏感的合约价值数百万美元在真正部署上线之前，理论上应该价值至少几万美元的赏金合约。这将增加我们平台的安全性，并激励更多的安全专家花时间在生态系统中开发自己的技能。

### 安全披露策略

攻击者可能会选择利用安全库作为查找现有智能合约漏洞的工具。 任何检测到的漏洞可以作为计划攻击的入手点。我们的本意不是要为攻击者提供便利，无论他们能否成功，都不太可能。

理论上讲，如果所有部署的智能合约都被QSP预审，而不必为攻击者提供访问完整的安全库，就可以一开始避免这种不幸的情况。因此，我们将采取以下行动：

1.  我们将在安全库的发布流程中实施一个Staging阶段，在此期间，我们将生成加密的安全报告，只有智能合约拥有者可以访问。

2.  我们将发布公开统计数据，指出在智能合约中出现的重大问题和频率，希望激励智能合约拥有者阅读安全报告并采取适当的行动。

3.  为避免给可能成为攻击者的人提供线索，我们将确保存在报告不会暗示为存在漏洞，加密报告的特性也不会提供任何可靠的线索，比方大小。

当新版本的安全库发布时，以前审计过的智能合约会有一个时间窗口发现新漏洞。即使这个机会的窗口相对较小，也可能会成为攻击者有机会使用安全库作为计划攻击的入口点。 这是独立验证者系统的次要目的 ——通过利用人的智慧与赏金，我们可以弥补不充分的自动检查和相对复杂的自动化攻击之间的差距。

### 分布并行SAT

软件验证带来了许多好处：更好的代码，更好的测试，更少的黑客，并且是提高软件安全性的有效方法。 SAT求解器是这项工作的重要工具。 在本节中，我们对SAT和Parallel SAT进行了粗略的讨论。

Quantstamp网络给SAT领域带来了精彩迷人的机会。 Quantstamp正在建立一种新的分布式SAT解决方案，其中内置了共识和冗余，并激励参与者解决所有SAT问题的各种问题，以求索赔和认证合约。 将这项技术应用于智能合约尤其令人兴奋，因为有这么多的关键。

#### 可满足性问题(SAT)

SAT的一个问题实例由n个变量中的布尔公式f组成。SAT求解器确认是否存在满足变量的赋值；换言之，对每个变量的赋值为真或假，使公式本身为真。大多数求解器要求f用合取范式 (CNF)，公式由子句连接组成，每个子句由一些分词组成。

典型的SAT求解器通过实际的求解过程，从问题的高级编码中参与以下三步工作流。
1. 编码器  
    a. 将问题编码为合取范式(CNF)，这样满足解就可以指示属性冲突  
    b. 通常多项式时间复杂  
    c. 需要少于1% 的总时间

2. 预处理程序  
    a. 经常执行简化和重编码  
    b. 多项式时间复杂度  
    c. 需要总时间的20% 左右  

3. 解决程序
    a. 冲突驱动的语句学习 (CDCL)
    b. 变量排序和其他试探法
    c. 输入的大小的**指数时间复杂度**
    d. 需要总时间的80%左右

解决程序是最具挑战性的，最坏的情况下，需要80%的计算工作和其指数级的时间复杂度。

许多策略已经被开发用来解决 SAT 公式，但最广泛的采用和成功的解决方法是基于 Davis-Putnam-Logemann-Loveland (DPLL)算法。当结合语句学习和巧妙的实现技巧时，DPLL-SAT便SAT求解器实际使用到了广泛应用中，反映了SAT在计算机科学中作为中心问题的重要性。

下面描述了 DPLL-SAT12 的概述。

![DPLL-SAT](https://github.com/yajiya/quantstamp-summary/blob/master/pics/dpll-sat.png)

Decide模块由 VSIDS (一种可变排序探索) 引导来执行决策。BCP 模块执行单元传播，直到没有新单位可派生，或识别出冲突 (unSAT)子句。该语句被移交至Analyze Conflict模块，跟踪语句冲突原因，并生成一个 "learnt"子句添加到子句数据库中。"learnt"子句防止赋值出错，Backtrack模块将回退状态，撤销赋值冲突。公式中识别出高级别冲突语句就认为是UNSAT，如果所以判断分支都完成，或当前赋值集合的所有字句都满足，就被认为是SAT。


#### 平行 SAT 求解器

通常依赖SAT求解器的模型检查和自动定理证明技术，在寻常电脑上可能需要从毫秒到小时的计算量。对于一些最难解决的问题，解决时间可以延长到几天，几周，或更长时间。算法、启发式和并行求解方面的进来发展很有帮助。能够共享工作负荷的求解器比不能共享的更好。平行的 SAT Solver使用更多的内核来克服连续的减速。

一个典型的并行 SAT求解器使用主从 (或任务农场)方法，分割搜索空间并在单独的过程中并行分析子空间。这是个很好的例子方法是 Parallel MiniSAT (PMSAT)。PMSAT 是一个分布式并行 SAT求解器，使用消息传递接口 (MPI) 在 C++ 中实现节点.PMSAT在以下方面是新颖的: (1) 它如何划分搜索空间可变选择和假设生成；(2) 假设是如何被修剪的；(3) 如何学会子句共享；和 (4) 自动设置。主控制客户的调度并在它们之间分配各种任务。可以使用多个分区启发式允许用户使用和共享学习条款。冲突学习用于修剪出色的任务，并可能停止其搜索空间不相关的进程。两个可选变量选择: (1) 频繁变量，或 (2) 变量出现在更大的条款中。

"任务农场" 方法使用一主多从的工作节点。从节点从主节点接受假设语句，返回搜索其子树的结果。主节点根据配置的操作模式对工作区进行分区。当工作节点发现UNSAT，它可以发送一个"learnt"子句和/或一个冲突向量，主节点用他来删除所有未测试的假设，然后直接导致UNSAT。收到UNSAT之后，主节点终止执行。冲突向量直接在结果消息，使用大小为20的数组发送给主节点，(如果需要，可以发送多个消息)。通常，假设语句比可用的工作节点多，这样工作节点完成工作之后，马上有事可做。

另一种并行SAT-sovler采用组合方法；也就是说，它依赖于运行在同一 SAT 实例中，多个解决方案并行。这项技术是最先进的并行 SAT求解器，目前由 ManySAT14 控制.很多ManySAT已发现使用不同的搜索启发式，甚至是不同的 SAT求解器，在性能上带来了巨大的收益。通过共享学习的条款，在不同的实例中可以观察到性能的提高。

Aigner et al 讨论了一个在终止时同步的纯并行组合 (PPP) 规划求解，但否则不共享任何信息。他们的多核实现使用共享内存，并提出这样的问题: 作为共享资源的内存是否成为瓶颈？如果是这样，经济放缓的程度有多大？内存系统拥塞导致性能下降被视为投资组合系统预期放缓的上限。投资组合解决方案，如ManySAT 和 Plingeling 有一个架构，其中原始公式和共享子句由每个规划求解器复制，简化设计并最小化同步开销。试图在一个更 细粒度水平上并行化的解决方案也不能扩展。缺点是，无论是公式，还是学习子句都不是物理共享的，从而 n 倍需要更多的内存，可能会有更多的内存系统造成经济放缓；但是，实验表明，大多数内存访问是本地 (由核心本地缓存满足)，即使在很大数量的情况下，也会保持低增长，解决并行运行。
13 Luis Miguel Silveira，Paulo Flores和Paulo Flores。PMSAT:一个平行版本的微型版本。杂志上可满足性，布尔建模和计算，6:71-98，2008。
14 Lakhdar Sais，Said Jabbour和Said Jabbour。许多SAT考试:一个平行的SAT解算器。杂志上可满足性，布尔建模和计算，6:245-262，2008。
15 Mathias Preiner、Aina Niemetz、Aina Niemetz、Christoph Kirsch和Armin Biere。投资组合分析在当前的多核架构上，风格并行的SAT解决方案。在第四届国际上SAT的语用学(后三)，Citeseer，2013。

#### 平行 SAT 和共识
如前所述,  Quantstamp 验证协议是将整体验证问题通过去中心化计算分成多个小的验证问题来同时进行处理。这个协议是制止破坏者的重要的规则。每个小区域处理完成的结果最后会被收集整理到SAT协议下，通过SAT协议进行规划得到最终结果。在Quantstamp 网络中我们称不相交子空间映射到节点的分区为quanstamp区域。在每个区域中节点的任务是在一个离散空间中找到一个完美的分配的方案。由于分区是不相交的，所以将每一个区域内识别出的完美方案带回原公式都可以算出一个恰当的数值。编码过程的第一步保证了加密计算可以进行，然后在原始系统中将会产生一个bug，这个BUG的需要由剩下2 /3 区域的最终输出达成一致意见后才能解决。

### 以太坊和Solidity的常见的漏洞
区块链技术所采用的Nick Szabo的智能合约是一个计算机程序，它会按严格程序运转不受任何权威机构的操控。
Ethereum协议支持有状态合约，这意味着状态变量的值在多个调用之间持续存在。合约在其地址上接到用来自用户的交易，就会被调用。
如果这样的交易被区块链接受，那么网络的所有参与者将执行这个合约代码。网络根据共识协议，对合约的输出和下一个阶段的状态达成一致。由于以太坊智能合约是不可改变的，交易结果是不可逆转的，所以在发布之前有效地解释代码的含义十分的重要。
Atzei等人在中描述了用Solidity为Ethereum编写智能合约的缺陷分类和会产生的异常行为。尽管现在只有以太坊有这种缺陷，但是未来使用智能合约的其他平台也很快会面临如何解决这种缺陷。我们根据用户的发现对这些缺陷做了如下归纳。


&nbsp;| &nbsp;
---|---
对于未知函数的调用 | 一些Solidity原语对接受者回退函数有不太明显的副作用。这可能导致意外行为，可能被攻击者利用。(我们在关于奇偶校验/多重集漏洞的部分中讨论此问题。
异常处理| 对于如何处理异常, 有两种不同的方法，采取哪一种主要取决于合约与项目的关联性。有的异常处理可以恢复所有的异常；而有的异常处理仅仅只能恢复智能合约被调用后的结果。因为如果进行更多修正将会影响到原有合约的安全性。
无Gas数据传输 | 当用户向合约发送以太坊时, 可能会出现不能进行gas传输的异常。
类型转换 | 编译器仅可以进行某一类型检查, 但如果代码超出了编译器检查范围, 就可导致异常。
重放 | 回退机制允许非递归函数在终止前进行重新输入， 修改非递归函数可以使其自动循环将ETH做为gas转出。 (当初Dao项目被盗就是利用了此漏洞)。
保守秘密 | 将字段声明为私有并不保证其保密性，因为 区块链是公开的，交易的内容是可察的。可能需要使用加密技术来保护秘密。
不可变修改性带来的问题 | 包括当在合约有漏洞，且并没有直接的方法来修补它时，无法更改部署的合约。（比如以太坊被盗后只有通过硬分叉来否认了以太坊失窃的后果）
交易可能丢失以太坊 |  以太发送到不使用地址后将会永远丢失，而且没有办法检测这个地址是否为不被使用的地址。
堆栈大小限制 |  调用堆栈会由1024帧和另一个调用绑定引发异常。（以太坊在2016年10月的硬分叉后已经解决了这个漏洞）
不可预知性 | 在向网络发送一笔交易时，并不能确保合约的状态是实际执行时的合约状态。此外，矿工将合约分组成块时不需要遵守的原有交易秩序。这导致黑客可以攻击“排队交易”这个漏洞。
随机性生成 | 一个矿工可以用他的程序块来伪造随机数的结果，冒充原有结果发送给用户。例如，彩票、游戏等这严重欺骗了使用者。
时间约束 | 时间约束可以用来确定当前状态应用程序允许进行什么操作。所以如果一个矿工在合约上持有股份，那么他可以通过选择一个合适的时间戳来获得额外收入。

下面是我们对数据库的安全性检测。

&nbsp; | &nbsp;
---|---
常数函数 | 编译器强制执行一个常数运算方法，该方法的结果不可被修改。
合约可以直接接收以太坊 | 直接接收以太的合约需要实现一个回退函数的功能用来接收以太坊，否则函数将会产生异常并退回以太坊。如果退回功能没有实现程序具备警报功能，这样程序员就可以发现并人工的去做退回操作。
回退功能 | 合约具备这样一个保障功能，它能在花费不超过2300 gas的条件下退回接收的以太坊。我们的自动测试程序员已经在花费不到2300 gas的条件下完成这个回退测试。
嵌入和开发 | 当调用另一个合约时，被调用的契约可以通过它的函数改变调用契约的状态变量。QUANTSTAMP可以检查调用外部函数后目前合约状态变量的变化，可嵌入开发能做到这点实属不易。 
隐含声明 | 函数中明确的所有变量是指在整个函数的范围内的所有变量。这些现在变量处于整个函数初始化的默认值。编写恶意码会篡改函数中这些具有默认值的变量。当这种情况发生时，我们将会向用户发送警报。 
交易所属人 | 当检查tx.origin时可以立马停止该地址上进行的交易并得到该地址信息。如果智能合约必须要求tx.origin 的所有者操作，则黑客不能通过攻击钱包盗取所有的资金。因为在这这种情况下tx.origin仅仅具备钱包的地址的功能并不能进行转出。 
Gas传输 | 这是一个非常危险的功能称为地址索取费用功能。该功能给出gas接收合约，可以通过支付高额gas实现更多功能。这是一个有待进一步深入探讨的问题。

## 财务计划

最小目标| | | |最大目标
---|---|---|---|---
300万美元| 600万美元| 1200万美元| 2000万美元| 3000万美元
工程师团队|||||
3年5名全职工程师| 3年8名全职工程师|5年12名全职工程师|5年20名全职工程师|5年27名全职工程师     
产品||||
最小的工作计划<br/>1名全职全领域安全工程师|提高工作计划<br/>1名全职软件测试工程师| 2名全职全领域安全工程师<br/>针对工作计划进行核实并修正| 打造更多的基于QSP网络的生态，改善QSP网络查询| 3名全职全领域安全工程师<br/>提高工作计划并保证最好的质量
社区与教育||||
编写QSP使用教程<br/>开展见面会来说明加强安全意识 | 编写QSP的MOOC教程<br/>每年举办一次QSP的安全创新活动|为使用QSP的区块链企业开发更容易的材料和举办会议说明|对QSP系统开发成果有领导贡献的开源补助|我们将提高行业的平台协作、合作研究、开源补助、安全事件、编程马拉松
商业||||
CEO管理所有非技术类成果|1名全职业务拓展专家，发展1名UX设计师|3名全职业务拓展或技术专家<br/>用来发展并帮助企业接入QSP系统|招租多名国际业务拓展专家，用来拓展亚洲市场。|在社区、服务支持、企业发展以及国际业务拓展等领域招租更多的人。


## 我们团队的研究成果

下表包括与我们联合研究工作相联系的部分软件验证项目的一些选择。必要时，我们将这些成熟的技术，实现我们在区块链安全智能合约中的目标。

名称| 成果研究者| 描述
---|---|---
Aolly及Aolly分析工具|Vajih Montaghami、Derek Rayside 、Steven Stewart| Aolly是一种使开发人员能够创建抽象的软件模型与成因的关系逻辑系统，Aolly分析工具有生成用户模型的示例的机械性能。最初是作为软件的一部分在麻省理工学院的丹尼尔杰克逊博士指导下的设计小组开发的。http://alloy.mit.edu/alloy/
Bordeaux|Derek Rayside|波尔多是一种制作边界示例的基于Aolly技术和外延的技术，并改进了软件模型中的部分过约束错误的识别调试能力。https://github.com/drayside/bordeaux
Clafer| Ed Zulkoski| Clafer是GSD实验室、滑铁卢大学的建模组与哥本哈根大学共同开发的一个通用的轻量级建模技术，轻量级建模技术旨在提高对软件开发早期阶段的领域问题的理解，且用较少的方法确定需求。Clafer的目标是使建模方式可访问范围更广的用户和域。http://www.clafer.org/
Margaux| Derek Rayside 、Vajih Montaghami| Margaux是一个基于调试模式的可以引导用户查找bug的工具。Github页面里包含一个架构图，说明如何使用判别示例的调试器用来指导开发人员纠正逻辑推理上的bug。https://github.com/vmontagh/margaux
MapleSAT、MapleCOMSPS 、MapleGlucose	Vijay Ganesh| Ed Zulkoski| 获奖的枫叶系列工具是由在滑铁卢大学开发并由Vijay Ganesh博士监督的，一个由冲突驱动的SAT冲突学习调解器。https://sites.google.com/a/gsd.uwaterloo.ca/mapl
MathCheck| Vijay Ganesh 、Ed Zulkoski| 一个关于计算机代数系统的结合了约束规划系统的SAT求解器。关于已知结果的两个猜想的超立方体。https://sites.google.com/site/uwmathcheck/
Miramichi| Derek Rayside、Steven Stewart| Miramichi是一个利用GPU计算性能的实验性的并行SAT求解器。https://bitbucket.org/sstewart2015/miramichi4j
Moolloy| Derek Rayside 、Steven Stewart| moolloy是一个在科学、软件中的应用工程与金融中扩展的离散多目标优化表达问题的关系逻辑系统。https://github.com/TeamAmalgam/moolloy
Petitcodiac| Derek Rayside、Steven Stewart| Petitcodiac是一个利用OpenMP和GPU的实验性的解决方案，如Yices和微软的Z3，通常使用一个变种单工的过程也采用了Petitcodiac。https://github.com/sstewart2012/peticodiac
STP| Vijay Ganesh| STP是针对求解位向量和数组的约束条件的约束求解器(或SMT solver)。这些约束的类型可以通过程序生成分析工具，定理证明，自动bug查询，加密攻击工具，智能开源工具fuzzers，模型检测以及更多的应用。https://github.com/stp/stp

### Demo:定位Parity多方签名漏洞

我们提供了一个自动定位Parity多重签名钱包漏洞的通用技术演示系统，此漏洞导致了3260万美元被盗窃。

这个简单的分析器构造了多个AST(抽象的语法树)的访问者，并使用它们提取一个稳定的Solidity合约的程序变量和调用结构。分析器可以提醒开发人员并发现任何直接或间接暴露非公共状态变量修改的公开方法。使用调用图，我们可以捕获可能存在的一类漏洞且定位其解决方案。在这个演示系统中，我们有两个solidity合约示例如何被分析者识别其直接和间接的漏洞。

演示系统在Github上的代码：https://github.com/quantstamp/solidity-analyzer



## 常见问题与解答
## 详细履历

**联合创始人** | &nbsp；
---|---
![image](https://quantstamp.com/wp-content/uploads/2017/09/Steven-Stewart-SQ.png)<br/> | **Steven Stewart** <br/> 滑铁卢大学ECE，软件审计 <br/><br/>史蒂文是滑铁卢大学（ECE）的博士生，师从于著名的导师Derek Rayside和Krzysztof Czarnecki，他专注于使用高性能分布式计算和GPU改进软件审计工具和求解器。<br/><br/>此前，Steven在旧金山联合创立了一家名叫“Many Trees Inc”的创业公司，主要是使用GPUs进行机器学习和大数据分析。在他的业余时间，他喜欢使用GPU来修改内存数据库。他在加拿大国防部的密码机构工作了接近5年。 博士毕业后，就创立了Quantstamp。
![image](https://quantstamp.com/wp-content/uploads/2017/08/Richard-Ma-SQ.png) | **Richard Ma** <br/>康奈尔大学ECE，算法投资组合经理<br/><br/>比特币HFT基金的算法投资组合经理。前Tower Research资本量子策略师。在竞争激烈的美国，欧洲和亚洲地区衍生品交易所有用C++/Python/R生成过程序化交易算法。编写了数万个单元测试并构建生产级集成和验证测试软件。在Richard卓越的测试和风险管理下，他的HFT交易系统近十年来一直稳定管理着数百万美元的资产而零大事故。
**创始成员**  | &nbsp；
![image](https://quantstamp.com/wp-content/uploads/2017/09/vajih.jpg) | **Dr Vajih Montaghami**，博士 <br/> Vajih Montaghami从滑铁卢大学获得博士学位，他的研究方向是校验和调试轻量级形式化模型。<br/> <br/> 在博士学习期间，他曾在Google工作过，具有丰富的大数据分析系统实战经验。他从事过有实际应用，基于海量数据源和机器学习算法的end-to-end测试自动化工作。最近，Vajih在亚马逊作为后端软件工程师协助开发高扩展性能的系统。
![image](https://quantstamp.com/wp-content/uploads/2017/09/ed_blue-sq2.png) | **Ed Zulkoski**，<br/> 数学与计算机科学系学士<br/> <br/> Ed Zulkoski是一名博士生，是Vijay Ganesh，Krzysztof Czarnecki管理下滑铁卢大学计算机与科学系下的候选人。他在Dr.Christopher Wintersteiger指导下完成了微软公司的研究实习。他的博士研究重点是学习并利用SAT和SMT的结构特性。他早期的工作调研了SAT结合计算机代数系统和优化技术实现多目标产品线路优化。Ed在IBM加拿大前沿学科研究中心获得了博士奖学金。
**顾问** | &nbsp；
![image](https://quantstamp.com/wp-content/uploads/2017/08/Vijay-Ganesh-SQ.png)|**Dr. Vijay Ganesh** <br/> 滑铁卢大学助理教授 <br/><br/>Vijay Ganesh博士是滑铁卢大学的一名助理教授。在此之前，他是麻省理工学院的研究科学家，并且于2007年完成了斯坦福大学计算机科学博士学位，Vijay的主要研究领域针对软件工程的自动推理，形式化方法，安全和数学的理论和实践。<br/><br/> Vijay赢得了无数奖项，最近获得了ACM CCS 2016年度奖，2016年度早期研究员奖，ACSAC 2016年杰出论文奖，2015年IBM研究学院奖，2013年和2011年两个Google研究人员奖，以及在2008年获得了十年最具影响力的论文奖。他总共赢了9最佳论文奖/荣誉。
![image](https://quantstamp.com/wp-content/uploads/2017/08/Derek-SQ.png) | Dr. Derek Rayside <br/>滑铁卢大学副教授<br/><br/>Derek Rayside是滑铁卢大学工程学院下电气与计算机系的一名副教授。他的主要研究领域是轻量级的形式化方法和程序分析。他已经获得了麻省理工学院计算机科学博士学位。<br/><br/>Derek是最近一家被微软收购的滑铁卢创业公司的顾问。

## 附录A

### 为什么我们会对智能合约表示担忧？

越来越多的证据表明，有超过40%的比例认为以太坊的智能合约是很脆弱的，并对此表示担忧。很难断定当前的智能合约是安全的，因为它们可能包含尚未发现的漏洞。这不是打击以太坊，假设任何平台能执行任意的代码并访问货币体系，这是有很大风险的。责任明显是在开发者身上。

#### DAO以及其他事件

代码即法律，他们如是说。

2016年6月17日，现在被称为“DAO”的从此也许跟现代最大的抢劫成为同义词。一个ETH小偷，在智能合约中发现了一个允许重复提款的漏洞，盗取了价值5500万美元的币。智能合约是没有按钮让人确认的，一旦部署了一个智能合约，就无法恢复到原来的状态了。这让攻击者很兴奋，因为智能合约是不可改变的和公开的，他们可以不择手段的学习和利用。


时间 | 损失 | 描述
---|---|---
2016年6月17日 | 5500万美金 | DAO事件应该是最出名的。非递归函数可以重新输入终止，导致循环调用消耗燃气。未处理的异常意味着，在函数调用中重复提现是可能的。
2017年6月20日 | 3260万美金 | Parity钱包多重签名中的一个漏洞被黑客利用，在这种情况下，一些Solidity函数，没有指定回调函数的调用者。这可能会导致意想不到的行为和可能被攻击者利用。
2017年7月31日 | 1000万美金 | REX令牌销售时智能合约中出现了错误，具体来说，当生成合约字节时部署时，定义构造函数参数时出错。错误的使用Javascript十六进制字符串而不是一个引用的字符串作为地址。这不是由攻击者引起的盗窃，这是一个可预防的损失。

当然，随之而来的是众所周知的并且有争议的以太坊硬分叉，意图通过这样纠正攻击者的犯下的错误。或许，对局外人来说，硬分叉有争议是令人惊讶的。毕竟，谁能宽恕世界最大的小偷呢？但是，问题在于：如果代码就是法律，那不就应该尊重它是这么写的吗？虽然智能合约的开发者确信没有提供AMT服务，但是正如代码本身所写的，却是允许这样做的。如果代码是法律，而这法律却允许盗窃，那将没有违法犯罪了。

无论你对代码有什么想法，那意味着都是法律问题。在我们看来，有一件事是肯定的：决不假设一个智能合约是安全的。只要代码能够访问货币系统，只要人类想赚钱，就没有真正安全的代码。我们所能做的是将风险降到最低，更可贵的是我们可以采证并排除一些众所周知的可利用的缺陷和漏洞。可以毫无遗漏地捕获所有在计算机程序中可能出现的错误的解决方案是不存在的，我们可以肯定的是把风险降到最低。事实上，有人会争辩说任何值得发现的bug都会被发现，而那些没被发现的都是无关紧要的。

不过，如果只发生过一次的事情---不管它的破坏力有多大，我们也许只是把它当成低概率的偶然事件。偶尔的盗窃只认为是个让人讨厌的麻烦事，从不认为这个是必然的灾难（喔，又是一起盗窃而已）。不幸的是，也没有一种错误代码的保险品种(目前还没有)，当漏洞被利用了，后果就是灾难性的。除此之外，还有种简单却不合实际的方法，不管什么时候发生了盗窃，那就进行硬分叉吧。

当然，找到一个bug并不是一件容易的事。即使bug可以自我识别，想设计出能完全理解代码背后真正含义的解决方案是很困难的。有时看起来像个bug实际上却是一个特性，我们应该怎么做呢？

我们的回答是：学习并保持不断的学习，识别漏洞的模式和类型。使用建模技术，并进行必要的优化改良。把这一切都封装起来，就成了能分散协作并一致验证其输出的安全库。我们将激励有贡献的人，并努力获得白帽子和黑帽子的援助。当他们成功发现漏洞时，开发者负责奖励他们。

### 最新研究

智能合约受安全漏洞的威胁的程度还不得而知，然而，最近的研究清楚地表明，这确实是一场灾难。下面我们总结一下论文研究中显示的一些常见严重漏洞，其中的一些是因为开发者很容易在不知不觉就犯的错误。


&nbsp；| &nbsp；
---|---
**让智能合约更智能** <br/> Loi Luu，Duc-Hiep Chu，Hrishi Olickel，Prateek Saxena，and Aquinas Hobor. 2016  <br/> 让智能合约更智能. 在 2016 ACM SIGSAC会议论文集 <br/> 计算机与通信安全（CCS '16）。 ACM，New  <br/>York，NY，USA，254-269。DOI：  <br/>https://doi.org/10.1145/2976749.2978309 | 恶意矿工和用户都可以利用某些类的漏洞，作者认为这是由于“语义鸿沟”造成的。在于开发人员如何思考代码预期执行与实际上的执行出现偏差。在他们研究的19366中，高达8519（44%）的能合约存在义鸿沟”漏洞，涉及总额在6百万的ETH。
智能合约的形式证明: 简略型论文<br/> Karthikeyan Bhargavan，Antoine elignat-Lavaud，Cédric ournet，Anitha Gollamudi，Georges Gonthier，Nadim <br/> Kobeissi，Natalia Kulatova，Aseem Rastogi，Thomas ibut-Pinote，Nikhil Swamy，and Santiago Zanella-Béguelin。 <br/> 智能合约的正式验证：简略型论文。 在2016 ACM讲习班编程论文集语言和安全分析（PLAS '16）。<br/>ACM，New ork，NY，USA，91-96。DOI：https://doi.org/10.1145/2993600.2993611| 作者将Solidity转换为F * 行分析EVM字节码。他们依次检查当send()方法调用失败时，两边的资产是否还原。他们也检测DAO发生过可重入的问题。他们的工具局限性只分析了46个智能合约，但是，那个作者声明只有屈指可数的能通过他们的验证。这意味着如果大量分析已发布的智能合约，将会发现大量的漏洞。
揭秘计算机共识激励<br/>Loi Luu，Jason Teutsch，Raghav Kulkarni和Prateek Saxena。揭秘计算机共识激励。 在第22届ACM SIGSAC会议论文集 计算机和通信安全（CCS '15）。 ACM，New York，NY，USA，706-719。DOI：https://doi.org/10.1145/2810103.2813659 | 作者表明图灵完备脚本将矿工暴露在一种新类型的攻击下，“老实的矿工容易受到伤害，验证每个区块的密码算法的数字货币交易需要显著计算资源”，为解决这个问题，他们提出了一种激励机制，让协商作弊无利可图。
智能合约上的攻击调查<br/>Nicola Atzei，Massimo Bartoletti和Tiziana Cimoli。 2017. 智能合约上的攻击调查 .第六届International Conference on Principles of Security and Trust - 第10204卷，Matteo Maffei and Mark Ryan (Eds.)，Vol。 10204. Springer-Verlag New York，Inc.，New York，NY，USA，164-186。DOI： https://doi.org/10.1007/978-3-662-54455-6_8 | 作者给当前出现的智能合约漏洞做了一个分类。总的来说，这些漏洞的产生是巧妙的利用了开发者未知或者被误解的东西。
逐步创建智能合约 <br/> D. Delmolino等人。逐步创造一个安全的智能合约：cryptocurrency实验室​经验与启示。Cryptology ePrint Archive，报告2015/460 2015。  http://eprint.iacr.org/ | 作者甚至展示了如何使用Rock，Paper，Scissors创建一个包含几处缺陷的合约。他们是无法回退，缺乏密码学而实现公平，激励错位的合约。
通过类型驱动实现更安全的智能合约  <br/> J. Pettersson and R. Edström. 通过类型驱动实现更安全的智能合约.使用依赖和多态类型开发更安全的智能合约。计算机科学论文，Chalmers University of Technology ​ ​of ​ ​Gothenburg，​ ​Sweden，​ ​2016. | 作者特别指出了在智能合约中很常见的三类错误. 意外状态，加密失败，完全调用堆栈。作者建议使用一种支持依赖和多态的叫Idris的函数语言，开发安全的智能合约。

虽然上述提到的都是一些个例，但据报道，还有相当一部分智能合约都存在已知的漏洞。我们认为：通过执行自动检查和形式化验证预期的属性，可以防止其中的许多问题。虽然有些攻击者可能会将精力集中在知名度高的，伺机盗取大额数量。但许多其他的攻击者也满足于多个目标小额盗取而不引起很大的注意。大家都在冒着风险！

## 附录B

#### 离线开发工具

除了去中心的安全平台，我们有兴趣开发一套旨在简化智能合约开发、调试和部署的离线工具。 这包括近期我们团队成员开发更智能的调试工具的应用。

### 智能调试使用区分示例

具有数学或逻辑基础的软件模型已被证明对软件工程实践有价值，使软件工程师能够将重点放在基本抽象上，同时关心更少的软件设计重要细节。 像任何人造工件一样，模型在设计过程的某些阶段可能存在缺陷：它可 能存在内部不一致，或者可能无法正确表达工程师的设计意图。


我们介绍一个智能调试器的想法，帮助非专家开发人员根据经过验证的本地化，理解和修复策略来发现缺陷和漏洞。
Vajih Montaghami和导师Derek Ravside博士（滑铁卢大学）在他的论文里面深入探究了具有辨别不同实例模型的调试方法声明。


需要进行调试是因为所表达的含义与预期的含义不同，但用户不知道在哪里或为什么。在整个软件生命周期中，调试可能是一个繁琐而耗时的任务。
Zeller在他关于调试命令性程序的精品书中，给人一个深刻的印象：那些真正的调试大师，他们看着代码，将手指指向屏幕，并告诉你：“你尝试过X吗？”你尝试X果然成功了。调试大师做了什么？他们已经识别，本地 化和纠正了错误，并且他们已经通过首先形成一个假设来做到这一点。
 
最近已经开发了工具和技术，为文中提到的将软件抽象化概念转化为关系逻辑模型提供自动化支持。

这样的工具有两种，被称为Bordeaux和Margaux（在下面的架构图中描绘）。
这些工具首先帮助用户形成关于模型可能出错的假设，并计算用户接受或拒绝的辨别示例来识别和理解错误。如果用户判断出错误已经被识别，则有助于本地进一步的自动化分析。

模型的哪一部分需要改变，并可能提供高层次的概念描述的纠正（但用户仍然需要手动进行纠正）。
 
举例，如程序的测试用例，如果它们揭示了模型的含义和工程师的设计意图之间的差异，则更有价值。 我们提出了为此目的区分例子的想法。

从工程师逻辑模型所表达的和工程师程序化的真正意图生成假设的组合中合成了一个区分例子。一个区分例子，要么满足模型，要么满足假设，要么满足假设，而是满足模型。它显示了模型与假设替代方案之间的差 异。
 
验证模逻辑型是工程师真正的意图，是一个重要而困难的问题。一个重要的的挑战是：工程师的意图是一个精神对象，通常没有一个书面模型来与之比较。
针对这一挑战的一个成功的方法是自动化示例生成工具，如合成分析仪。
这些工具产生了工程师接受或拒绝的示例（满足模型的逻辑）。工程师对这些例子的判断，都是工程师反馈的真正意图。
 
智能调试可以减轻那些他们认为该代码的功能和代码实际的功能之间差异的开发者
智能调试器使开发人员（可能缺少正式方法的培训）来应用本地化，解析和反馈修复错误。

## 附录C




