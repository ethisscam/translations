---
title: BADGERS DIGG SUSHI
date: 2021年1月26日
tags:
  - sushi
excerpt: 有些东西还是不要碰。筹集420万美元，从Curve那里复制代码，然后被玩坏。任何支持@saddlefinance的投资者都认为利益高于过程。为什么要资助零创新的分叉项目？
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/01/header-3.jpg
---
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/01/header-3.jpg)

**我们知道蜜獾在夜间外出觅食时会走同样的路线。这会在田野和树林之间形成一条破旧的道路。**

**当蜜獾的通常路径受到某种方式的干扰或阻碍时，这会使动物迷惑，并导致它们重新基于错误的配对。**

一笔交易告警向我们展示一位[经验丰富的DeFi用户](https://etherscan.io/address/0x51841d9afe10fe55571bdb8f4af1060415003528)使用[Badger DAO](https://app.badger.finance/)的代币[DIGG](https://www.coingecko.com/en/coins/digg)把0.001个ETH变成81.68个。

经过进一步研究，我们发现尽管存在漏洞利用，但损害已经得到遏制，被视为对整个SushiSwap协议构成威胁的仅仅是一个聪明的拾荒者，捡拾剩下的食物。

**由于SushiSwap团队一时的健忘，一个已知的钱包正在利用一个旧漏洞，该漏洞已重新打开。**

**尽管起初引起我们注意的交易似乎令人震惊，但是一旦我们与Sushi团队进行了交谈，就可以清楚地发现，没有太大的担忧可言。**

该[交易](https://etherscan.io/tx/0x0af5a6d2d8b49f68dcfd4599a0e767450e76e08a5aeba9b3d534a604d308e60b)显示SushiMaker试图通过一个几乎没有流动性和高滑点的Digg/ETH池转走DIGG/WBTC0.05％的兑换费（〜24小时），导致Digg/ETH池的流动性提供者获得丰厚的费用。

这些是本应支付给XSUSHI持有者的费用，但转给了攻击者。

**这是怎么发生的？**

尽管已经在几周前创建了解决方案，但必须将其与每个新池一起手动应用。由于尚未应用此功能，因此拾荒者得以潜入并收取xSushi持有人应支付的费用。

当在Sushiswaps的中添加新的对时，添加了 Onsen一些非ETH对，但在SushiMaker中未为DIGG / WBTC设置“桥接”。

SushiMaker是收取0.05％交易费用并将其转嫁给以xSUSHI抵押SUSHI的用户以赚取额外SUSHI奖励而不会造成永久损失的合同。

默认情况下，SushiMaker会将累积的费用（及其对）出售给ETH，然后出售给SUSHI。

桥梁意味着，当SushiMaker出售没有ETH对的资产的费用时，它可以对具有适当流动性的ETH以外的资产进行出售。

如果没有桥梁，可以添加流动性以创建ETH对，SushiMaker将尝试通过该货币对转换该资产的费用，并由于流动性小而遭受较高的价格影响。

这导致累积费用直至SushiMaker“服务”奖励那个ETH对的流动性提供者，而不是xSUSHI参与者。

幸运的是，没有任何基础的LP或xSUSHI头寸受到影响，仅损失了前一天的资产收益（DIGG / WBTC掉期的0.05％手续费-81 ETH）。

已通过制造商合同为DIGG建立了桥梁，以解决xSUSHI参与者的此问题。 SushiMaker也包含此桥。

在Sushiswap Discord中的一次对话使我们对漏洞利用的机制有了更深入的了解：



我们分析了清除程序的地址，发现他是机器人和快速贷款的知名用户。

![](https://lh4.googleusercontent.com/mbHCt8MYOKLIbVMR8ZEUaz0LHxerb8pKXbTDahY_U_KS_IocDL9ymBER2j0VVVHSIAQQLKb7mc3XorPJV382OJK0KUFe1rvEQcr4-3zJqOg_t435UtQzUtwjB_UGGgODeEsgWbCg)

来自[Nansen](https://nansen.ai/)的数据 

我们发现了几笔交易，表明该用户一直在试图利用此漏洞并窃取LP费用。

[0x90fb0c9976361f537330a5617a404045ffb3fef5972cf67b531386014eeae7a9](https://etherscan.io/tx/0x90fb0c9976361f537330a5617a404045ffb3fef5972cf67b531386014eeae7a9)

[0x0af5a6d2d8b49f68dcfd4599a0e767450e76e08a5aeba9b3d534a604d308e60b](https://etherscan.io/tx/0x0af5a6d2d8b49f68dcfd4599a0e767450e76e08a5aeba9b3d534a604d308e60b)

[0xcec93808a657d00cbb0245711e9419d0ea278b3a60a9a6d0a8c3353523c0e982](https://etherscan.io/tx/0xcec93808a657d00cbb0245711e9419d0ea278b3a60a9a6d0a8c3353523c0e982)

[0xe0527f7befaea54257113a09c8b3f4cd416e11a0e196cd2ba2e5e07c47767ddf](https://etherscan.io/tx/0xe0527f7befaea54257113a09c8b3f4cd416e11a0e196cd2ba2e5e07c47767ddf)

本来可能是一场灾难结果证明只是对Sushi团队的一次小小耻辱。

尽管攻击者已成功利用了我们的漏洞，但我们可以认为这是对SushiSwap的紧迫呼吁，SushiSwap目前拥有 $ 1.9B TVL 进行保护。

Discord中的对话表明他们将不会自动执行此修复程序，并且将继续依赖于每次都记住要应用此修复程序，这有点令人担忧。

为什么在不需要的情况下允许人为错误？

尽管代码可能是分散的，但是当开发人员使用如此庞大的TVL进行协议时，开发人员将承担巨大的责任。压力的影响通常被低估了，我们看到许多开发人员成为“精疲力尽”的受害者。编码时可能会出错，因此Sushiswap可能会从此处的一些自动化中受益。

这个故事提醒人们，黑客和套利者一直在监视协议，他们会跟随他们的一举一动并试图掏腰包或将其彻底淘汰。

但是，这种检查是双向的-甚至Twitter用户“ simp2win”之类的业余爱好者也可以从远处监视黑客。他们的努力值得称赞，但也许他们应该将分析留给专家。

我们爱一个有话要说的黑客，因此我们很高兴看到他们通过发送以下消息 以太坊呼叫数据。

Twitte上叫simp2win的这个人是谁，说我赚了1000万？我希望真能这样
