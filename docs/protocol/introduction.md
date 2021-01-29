> All I want for defi is for someone to fork Maker, rip out the governance and replace it with automated interest rate targeting, rip out the DSR and have the token itself just target `index * (1 + interest_rate)**time`, and generalize it to a whole bunch of price indices....

<p align="right">By <a href="https://twitter.com/VitalikButerin/status/1300611609715339265">Vitalik Buterin</a></p>

RealDAO Protocol(以下简称 RealDAO)，实现了 vitalik 在 twitter 上提到的理想中的稳定币协议，但并没有 fork MakerDao 的源码，而是基于 Compound 源码进行了重构，利用其借贷模型实现了一个功能更丰富、特性更吸引人的去中心化稳定币协议。

RealDAO 继承了 MakerDao 的如下特性：

- 多担保品、超额抵押
- 1:1 锚定美元
- 基于以太坊智能合约实现
- 去中心化治理

与 MakerDao 的不同特性：

- 双向借贷模型取代单向铸造模型
- 无 DSR
- 以 Chainlink 取代喂价系统
- 流动性挖矿激励机制
- 一次性清算取代拍卖机制

通过以上一系列的技术和功能改进，我们可以看出 RealDAO 是一个更加完善的去中心化稳定币协议：

- 资产使用率更高
- 利率定价更合理，符合市场供需规律
- 更加轻量级
- 完美符合通证经济的激励机制
- 避免拍卖过程中过多手续费消耗，更经济
- 避免因黑天鹅事件导致的拍卖漏洞，鲁棒性更高
