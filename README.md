# iBank EOS余额宝理财产品

### 简介
iBank是一款依托于EOS CPU租赁的资金理财DApp，它允许EOS的持有者，将他们的EOS资产存储在iBank智能合约里，并采用集中化的资源租赁循环，将受益分配跟这些资产储存者。

### 储蓄需求分析
随着EOS生态的发展，EOS主网资源将会变得越来越昂贵，很多开发者的资源需求并不持续，往往在短时间内爆发出大量计算需求。与此同时，很多持币者也想要通过出租自己持有的计算资源来获利。iBank对接储蓄和租赁的双方，采用智能合约来记账，降低了市场对接的成本。

### 安全性设计
iBank募集到的所有资金都实时存放在iBank的仓库合约中，仓库有多方签名来共同提供安全审核。iBank为了资金安全，选择不开放源代码。仓库合约的调用被严格限制在储户表内部，不能绕开储户表提款。具体安全架构设计可以参考币乎上的分享文章：https://bihu.com/article/1718844844

### 资金的使用
每当我们的渠道方收到任意一笔租单后，将会自动提取iBank的资金来完成租赁，与此同时，收到的利息也将会立刻被记账在每一位储户的余额宝里。如果你注意观察你的iBank账户，你会发现每隔几分钟，你的存款利息将会慢慢增加。每一笔利息都是真实租单提供的利息收入，我们根据你的存款占据总存款的份额来平均分配每一次利息收入。

### 存款提款说明：
1.使用Chrome带插件Scatter，登录 https://ibankeos.io ，即刻开始存款获取收益。
2.iBank已经对接各大主流钱包，打开钱包搜索iBank DApp，同样可以很方便的存款并查询收益。

### 专业资方服务
如果您是拥有大量EOS的资方人士，欢迎与我们洽淡合作，我们将为你提供稳定的租赁利息收益，24小时在线的智能合约使您提高租赁效率，大量节省了你的时间成本，请即刻联系我们，将为你设计最佳的自动租赁模型。

### 项目方服务
我们全力提供业内最低的租赁价格与最稳定的抵押服务，在人工服务不在线的时候，24小时提供服务的租赁合约，你可以发送EOS到我们的租赁合约，0.5秒即刻抵押到账，解决项目合约卡死的问题。

### 常见问题：
- 募集到的资金是用来做什么的？
回答：募集到的资金，100%的比例全部用来抵押CPU/NET，仅仅执行delegatebw抵押，没有transfer和sent资产，不存在挪用的可能。

- 提款三天到账和立刻提款有什么分别？
回答：由于EOS的设定，赎回资源需要3天时间，如果你现在发送提款命令，选择三天到账，那么你将不产生利息损失。然而当你选择立即提款模式的时候，实际上你存入的资产被抵押出去了，这需要我们提供资金垫付完成你的立即提款操作，所以他收取0.1%的手续费。我们如此设计是为了解决以下情况：如果一个人先存款1万币，然后立刻从CPU租赁市场租赁1万币，然后再次选择立即提取iBank的存款，那么他将会自己收到自己的租赁利息，这对于其他租赁客户来说，是一种不公平的行为。

- 为什么余额宝理财的利率是浮动的？
回答：就像传统的银行一样，假设银行的名义利率固定在6%，银行有100万币，那么当银行租赁出去50万币的时候，对于100万币来说，实际收到的利率仅仅是3%，也就是余额宝理财的收益率是挂钩CPU租赁市场的整体出租率。同时，随着EOS租赁市场的成熟，价格战在所难免。我们时刻关注租赁市场的变化，采取灵活的市场定价策略保持收益的均衡性。

- 你们应该努力让收益率上涨。
回答：这确实是我们努力的目标，iBank的收益率挂钩CPU租赁市场的出租率，但我们也会尝试使用“余额宝理财额度限制”来拉升理财的收益率。但是，出租率和储蓄额度是一个跷跷板的关系，所以，我们一直在优化我们的金融模型，以期在保持资金池稳定的情况下最大化提高理财的收益率。

- 我们会亏本吗？
回答：在极端的情况下，租赁也不会亏本，因为iBank这种理财模型是“租单分红”，也即每当CPU租赁市场收到租单，iBank立刻分红记账，它只有上涨和缓慢上涨，永远不会出现负收益。除非一种情况，你存款不足三天而又选择立刻提款，这将会收取0.1%的立即提款手续费。

- 与其他理财产品相比，iBank的优势是什么？
回答：当EOS币价下跌的时候，在iBank的存款你可以选择立刻提款以降低风险，而不会出现抵押给别人7天无法赎回的问题。相遇于24小时EOS币价下跌10%来说，0.1%的立即提款手续费不值一提，同时你的存款还拿到了利息早已覆盖这个成本。

- iBank的余额宝会发生挤兑吗？我的资产能不能保证提取顺利？
回答：iBank拥有50万EOS币的底仓，我们深耕EOS生态，并不卖出自己拥有的EOS币，iBank资金池仅仅用于抵押操作，所有储户100%提取存款，也不会发生挤兑。

- REX如果上线了，将会有什么影响？
回答：REX是面向开发者的资源租赁系统，他并不支持我们目前的超级短租业务，REX不支持常见的24小时租赁。72小时租赁，租赁市场拥有很多个性化的需求，并非REX可以全部占据。

- iBank的开发者团队是谁？
回答：iBank由国内顶级的DApp开发团队 DAppPub推出，EOSAsia、TokenPocket、麦子钱包、PocketEOS、BitPortal、51Token等提供技术服务，由EOSBank、EOSCloud、CPU一元租赁等渠道方提供租赁业务支持，采取多方合作的方式推出。

### 客户支持
wechat：thbourlove
email: hongbo@dap.pub
