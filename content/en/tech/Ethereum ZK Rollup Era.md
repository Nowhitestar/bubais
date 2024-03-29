---
title: "Ethereum's ZK Rollup Era"
date: 2022-04-22T21:51:33+08:00
description: Ethereum is about to enter its Layer 2 era, and ZK Rollup is one of the best solutions among all L2 scaling technologies. What kind of sparks can zero-knowledge proof technology and aggregate expansion technology create? How is ZK Rollup better than other scaling technologies? How can it be adopted quickly? From the perspective of investment, how to capture the value of the ZK Rollup era, and what kind of innovative applications will it produce?
tags:
- Infrastructure
- Web 3.0
indent: false
comments: false
toc: false
slug: Ethereum ZK Rollup Era
---

# Why focus on Zero-Knowledge (ZK) Rollup?

For a brief introduction to ZK and ZK Rollup technology, you can refer to my previous article.

[ZK Rollup: The Future of Ethereum Scaling](https://mirror.xyz/bubai.eth/CfIJX6ASjERg-MdYccN7QYf0T88Ey3fCk-F7MNLtq9I)

Zero-Knowledge cryptography has been called one of the most underrated technologies of our generation. Unlike the overwhelming news coverage of topics like artificial intelligence and big data, there is little media attention to zero-knowledge technology. Nonetheless, the technology is still a great breakthrough, bringing valuable privacy guarantees to this era of big data where personal information has nowhere to hide.

Zero-knowledge cryptography is a broad topic, but in this article, we will only focus on one area most relevant to blockchains: zero-knowledge proofs. A zero-knowledge proof is a non-interactive, zero-knowledge proof of knowledge that assumes two parties: a prover and a verifier. The prover wants to prove to the verifier that they know some information without revealing what it is. At the same time, the validator will look at the proof and accept or reject it. These schemes have three properties:

1. Integrity - any valid result can justify a given program
2. Robustness - no dishonest actor can create valid proofs
3. Zero knowledge - the verifier knows nothing about the *input* of the proof, only the result

In the realm of blockchains, which are publicly visible on all data chains, this proof of a statement without revealing its truth is a powerful primitive. Whether for individuals, enterprises or governments, this technology can solve many real pain points, such as [Protecting user data, designing sensitive systems or contracts, proving fairness in the distribution of public goods, and enabling more efficient and economical government agencies](https://zeroknowledge.fm/zero-knowledge-cryptography-the-next-digital-revolution/)。

In the field of blockchain, in addition to privacy protection, the most eye-catching application is ZK Rollup, the expansion scheme of Ethereum. [Ethereum is currently embracing a rollup-centric scaling solution](https://ethereum-magicians.org/t/a-rollup-centric-ethereum-roadmap/4698), it represents the optimal trade-off between decentralization, security, and scalability. Essentially, the Ethereum upgrade will make the network more scalable, sustainable and secure.

The expansion plan of Ethereum is divided into on-chain expansion and off-chain expansion.

On-chain scaling technology is an upgrade to the base layer of the blockchain to improve scalability. Ethereum's long-term on-chain scaling solution is called sharding, which actually splits the base layer into 64 chains with shared security secured by the beacon chain.

Off-chain scaling refers to scaling solutions that use an external execution layer instead of the base layer. These Layer 2 or "L2" are auxiliary layers that sit on top of the base layer and provide more transactional capabilities to the entire blockchain. The L2s solution embraced by Ethereum is Rollup, which can bring the following features:

1. With roll up, Ethereum can go from about 25 to 3,000 TPS without sacrificing security;
2. With roll up, user funds cannot be stolen or censored (as is the case on some sidechains);
3. Users can always access data on L1, and no one can prevent users’ funds from safely withdrawing from the roll up at any time.

There are two (main) types of rollups in current solutions: ZK Rollup (ZKRU) and Optimistic Rollup (OR).

## Optimistic and Zero Knowledge method comparison

Optimistic Rollup is a more mature solution than ZKRU. Products from Optimstic and Arbiturm are already available to Ethereum developers. However, due to the use of the fraud proof mechanism, its withdrawal time and security are currently debatable, and its cost optimization is slightly inferior to ZK. The weaknesses of ZK Rollup are basically technical problems. With a large number of excellent developers investing in related research, most people including Vitalik agree that ZK Rollup will be a better expansion solution in the future. Comparing the two, [the gas cost and TPS of each solution are as follows](https://w3hitchhiker.mirror.xyz/7dwD76ZZIlR7ep731K6y9vTTuXGHOojxWSnkXKzqPzI)：

![untitled](https://tva1.sinaimg.cn/large/e6c9d24egy1h2bizskocfj216u0n4q78.jpg "The cost of each of the four methods Source: Xiang｜W3.Hitchhiker，The premise of the above calculation is that the current Eth price is 2500u, the block gas limit is 30000000, the gas cost is 30Gwei, and the average block time is 13 seconds. The limit TPS refers to the corresponding operating environment occupying all Ethereum block space (in the proof verification Costs 500,000 gas), ordinary TPS means that the corresponding operating environment occupies 1/3 of the block space of all Ethereum.")

In terms of efficiency and cost, the ZK scheme is more efficient than the OR scheme, with higher TPS and lower costs.

In terms of time cost, and due to the fraud proof mechanism, withdrawals on Optimtisc Rollup require a submission period of 7-14 days for others to falsify potential malicious behavior, although there are already Optimstic Rollup solutions such as Boba Network. Proposed liquidity pool mechanism to reduce withdrawal period.

In terms of compatibility, both Optimistic and ZK face the problem of accommodating complex EVM contract invocation operations, but Optimistic is easier to achieve this. OR solutions including Arbitrum, Optimism have EVM-compatible virtual machines, allowing them to process all transactions on the main chain of Ethereum. 

One of the main issues limiting the development of ZK Rollup is EVM compatibility. At the beginning of the EVM design, the developer did not expect to use ZK technology in the future. Therefore, it is almost impossible to generate usable zero-knowledge proofs through EVM operations, thus giving rise to the need for ZK-EVM. So far there is no publicly available ZK-EVM solution. However, the zkSync 2.0 public testnet was officially launched at the end of February, which is also the first EVM-compatible ZK Rollup on the Ethereum testnet. Perhaps the large-scale practical use of ZK Rollup will come sooner than we expect. 

> Why is EVM compatibility so difficult for ZK?
> Most of the existing ZK Rollup solutions can only support simple payment and swap scenarios. The reason is that zkEVM not only needs to normally execute the bytecode of the smart contract, but also needs to generate a Proof to indicate that the state has been updated correctly after the transaction is reached. It’s difficult for the two to be compatible due to t[he design of EVM and the algorithm principles of ZK Proof](https://hackmd.io/@yezhang/S1_KMMbGt). 

In terms of security, the security of OR comes from economics where a reasonable incentive mechanism must be designed to drive a group of verifiers on the main chain to monitor the submitter at any time and be ready to submit fraud proofs. The submitter, on the other hand, must pay the price for the evil node by staking. Meanwhile, the security of ZK comes from mathematics or cryptography which can be trustless. The guarantees provided by mathematics and cryptography are far more reliable than the optimistic belief that human nature cannot be evil. 

In comparison, the [pros and cons](https://mirror.xyz/0x3D5FE39342e661776bb5273521F52E99B624288c/NFOsWYCb2eVk612VSnrrCsoKcwI_EMObp_q9uNKa4uA) of ZK Rollups are as follows:

PROS

- Less data contained in each transaction increases the throughput and scalability of L2 with the benefits of greater scalability and reduced transaction costs compared with Optimistic Rollups;
- There is no need for anyone to monitor ZKR;
- Do not require a dispute window like Optimistic Rollups, which can reduce the withdrawal time from about two weeks to minutes; 
- Privacy is enabled by default.

CONS

- The difficulty in computing zero-knowledge proofs will require data optimization to get maximum throughput;
- Initially setting up and integrating into the Ethereum network is more difficult than Optimistic Rollups. 

Relatively speaking, the weaknesses of ZK Rollup are basically technical issues. It is believed that these problems will be solved as a large number of outstanding developers are devoting themselves to relevant research. Most people including Vitalik agree that ZK Rollup will be a better scaling solution in the future. 

# What Is the Landscape of the ZK Rollup Scalability Solution?

## ZK Rollups Players Comparison

There are two major players in the ZK Rollup technology area: [zkSync](https://twitter.com/zksync) and  [StarkWare](https://twitter.com/StarkWareLtd)。

Some of the [major differences](https://news.ethereum.cn/Layer2/zksync-vs-starkware) between the two players in terms of team, technology, data availability, financing and supporters, current products and roadmaps are shown directly in the table below. 

|  | StarkWare | zkSync（Matter Lab） |
| --- | --- | --- |
| Team | Established in May 2018. Its core members include a former Chief Scientist of Zcash and professors at Technion Israel Institute of Technology | Established in December 2019. Alex G. is its co-founder |
| Technology | zk-STARKs | zk-SNARKs（like PLONK） |
| Data Availability | Off-chain solution: Volition | Off-chain solution: zkPorter (based on Volition architecture, more decentralized) |
| Financing and Supporters | A seed round funding of 6 million USD in May 2018 (Pantera/Naval/Vitalik) <br> A Series A funding of 30 million USD in October 2018 (Paradigm/Sequoia/Cb Ventures) <br> A Series B funding of 75 million USD in March 2021 (Paradigm/3AC/Alameda) <br> A Series C funding of $50 million in November 2021 (Paradigm/3AC/Alameda) <br> Supporters: Ethereum Foundation members, prominent investment institutions | A Series A funding of 6 million in March 2021 (Binance/Cb Ventures/AAVE/Balancer/Curve) <br> A Series B funding of 50 million in November 2021 (a16z/Placeholdxr/Crypto.com, etc.) <br> Supporters: comparatively not so many famous investors |
| Current Products | StarEx、StarkNet、Volition、Validium | zkSync、zkPorter |
| Roadmap | Planets-> Constellations-> Universe | Scalable Payments -> Smart Contracts -> Privacy -> Censorship Resistance |

Team. StarWare have more academic professionals. Its team is composed of world-class cryptographers and scientists who have been pioneers and innovators in the zero-knowledge field for many years. They have published many academic papers, which are in the process of turning into a real-world product, StarkWare. Meanwhile, there is not much information about zkSync team. From the product launch, it’s indicated that the team is cross-professional and highly efficient. 

Technology. StarkWare is still a better choice. It provides blockchain finality, which means it has the optimal capital efficiency. Besides, the [main advantages](https://www.geekmeta.com/article/3421070.html) of STARK are as follows:

1. 1.StarkWare invented and built its own ZK-STARK system, while zkSync’s technology stack was built by someone else (PLONK, built by Aztec). This also means that StarkWare is more capable of mastering and improving technology. 
2. StarkWare already has several systems running in the production environment, which use a Turing-complete programming language called Cairo, which is readily available; while Matter Labs has only one simple payment system in the production environment, and no Turing-complete language is available. 
3. StarkWare is faster, more secure (in a cryptographic sense), transparent (no trust settings required) and post-quantum secure; while the core technology used by Matter Labs (built by another team) is slower, requires trust settings, and can be breached by quantum computers. 

Data availability (DA). StarkWare invented the Volition system to solve DA problems. Volition allows end-users to choose between the rollup solution (on-chain data availability) and the validium solution (off-chain data availability) for each transaction. ZkSync uses the zkPorter technology based on Volition. The main difference between Volition and zkPorter is: in the Volition solution, users can choose the data storage method based on each transaction, while in zkPorter solution, users can choose the transaction settlement method based on each account (zkPorter accounts can only be accessed through off-chain data-available ways to make transactions). In addition, zkPorter’s off-chain DA system is more decentralized, because its DA is motivated by Guardian, actuated by zkSync native tokens to provide security, rather than a centralized “DAC”.

Financing and supporters. StarkWare is valued at 2 billion USD and is in the process of raising a Series D funding worth approximately 6 billion USD. This is a world-class financing process, attracting many famous investors. Some tycoons and members of Ethereum Foundation have been involved. Vitalik itself has also reviewed most of the articles published by StarkWare. Compared with StarkWare, zkSync has fewer prominent investors, and it looks like large-scale DeFi/CEX encrypted family financing. Each of these projects is well-recognized,  and together they can form a good ecosystem. It’s important to note that the success of ZK Rollup will depend heavily on the addition of the DeFi protocol and the direct integration with CEX. 

Current products and roadmap. In June 2020, StarkWare first launched StarEx, which represents the “Planets” phase of their roadmap and allows the creation of permissioned, application-specific ZK Rollup supported by Cairo and STARKs, such as [dydx](https://twitter.com/dydxprotocol), [Immutable](https://twitter.com/Immutable), [Deversifi](https://twitter.com/deversifi), [Sorare](https://sorare.com/?action=signin). They are the four main applications supported by the production version of StarkEx. As of March 2022, StarkEx has processed 134 million transactions, and its cumulative transaction volume amounts to $490 billion and the Total Value Locked hit $1.1 billion.

![StarkWare 路线图 来源：StarkWare](https://tva1.sinaimg.cn/large/e6c9d24egy1h2bj0upigbj20iw097jry.jpg "StarkWare Roadmap Source: StarkWare")

On November 29, 2021, they released the Alpha version of the mainnet of StarkNet, which is rapidly moving towards the “Constellations” phase of the roadmap. StarkNet is the general ZK Rollup that we expect to be permissionless and multi-application. As of March 2022, the StarkNet testnet Goerli has generated 1.4 million transactions and 45,000 were made on the mainnet. In terms of contract deployment, there are 26,000 contracts on the testnet Goerli and 1,600 contracts on the mainnet.

Initially, StarkNet will be driven by a centralized prover, and applications will need to apply for a whitelist to be deployed sequentially, just like what Optimism did. They plan to develop the ecosystem and gradually decentralize StarkNet to achieve the “Universe” phase of the roadmap.

The roadmap for zkSync can be summarized as the following 4 steps. The first phase corresponds to the zkSync 1.0 launched in June 2020, which is roughly equivalent to a ZK Rollup without smart contract integration. Users can send and receive tokens but this lacks composability. Many promising projects have been already deployed on zkSync 1.0.

![zkSync 路线图 来源：Matter Lab](https://images.mirror-media.xyz/publication-images/wn63t_kZgq73Qtgrzt0JR.png?height=206&width=837 "zkSync Roadmap Source：Matter Lab")

The second phase of the roadmap started with the launch of zkSync 2.0 on the mainnet, which includes everything we expect: a fully EVM-compatible ZK Rollup with smart contract composability. zkSync 2.0 was initially planned to be launched on the mainnet in August but was delayed due to [some technical difficulties](https://blog.matter-labs.io/zksync-2-0-developer-update-d25417f16446). These issues are now being tested on the testnet and are gradually being resolved. In October, zkSync revealed some of its recently completed technical details and deployed an AMM-like testnet (uniswap) to verify its EVM compatibility. To ensure the compatibility of LLVM/Solidity, Matter Labs delays its launch, which may sound depressing at the beginning. However, it will help every Ethereum tool to achieve local integration on zkSync 2.0.

## Advantages of ZK Rollup

The ZK Rollup solution can bring [unique advantages](https://mp.weixin.qq.com/s/r7cNMWYPP-9sqjLcKz64Aw) such as privacy protection, scalability preserving and cross-chain application implementation.

1. Privacy is one of the advantages and features of ZK Rollup.

Permissionless blockchains can achieve computational completeness without trusting third parties, but they come at a cost in terms of scalability and privacy. Since the 1980s, theoretical work on the proof system such as zero-knowledge proofs, interactive proofs, and probabilistically checkable proofs has elucidated ways to address these two issues and embodied them in practical applications.

2. Scalability gives developers almost unlimited computing power theoretically.

This makes it possible to port over all the ecologies on the Internet. For example, matchmaking games were previously difficult to develop on Ethereum, but ZK Rollup can change that. In addition, the supercomputing power coupled with the characteristics of the blockchain can also create many new applications.

3. The cross-chain application is one of the representatives of ZK Rollup. StarkNet has a very diverse range of bridging functions.

Developers can send any load (not transfers) from L1 to L2, that is, deploy the head of the dApp on L2 where governance or game operations can be performed at a lower cost, while sending instructions to the liquidity of L1. It's like using L2 as the brain and L1 as the muscle.

## Limitations of ZK Rollup

Although ZK Rollup is a very good solution for Ethereum scaling, its applications are still accompanied by some risks, such as liquidity fragmentation, reduced composability due to communication difficulties and technology barriers, and centralization risks.

1. The problem of liquidity fragmentation has become increasingly prominent in the current multi-chain world and is not specific to ZK Rollup applications.

Due to the existence of multiple technology solutions, the number of rollup networks will increase in the future, which will lead to more severe liquidity fragmentation. The good news is that there are many cross-chain communication technology solutions that address this issue, such as Layerzero's StarGate (note that StarGate does not support ZK Rollup at the moment) launched in March 2022. Under the premise of ensuring security, LayerZero is bringing us an “omni-chain future”, including state sharing, unified bridge liquidity, cross-chain lending, Swap, and multi-chain revenue aggregators.

2. The composability problem is mainly reflected in the interaction between the main chain dapp and the sub-chain dapp.

Each new protocol built on Ethereum is like a Lego block on which other protocols can easily be built, which is one of [the reasons why DeFi is growing rapidly](https://future.a16z.com/how-composability-unlocks-crypto-and-everything-else/). If the communication and contract standard issues cannot be solved, then dapps on sub-chains need to rebuild their own ecologies, which creates abigger waste of resources. Communication mechanisms and corresponding contract standards are needed not only between sub-chains and main chains, but also between sub-chains and sub-chains.

3. The centralization risk is mainly due to the fact that the sequencer responsible for executing, sorting, compressing and packaging transactions in current Rollup solutions is a more centralized role. Rollup must address the centralization issue if it is to further improve security.

# What Does the Future of Scaling Look Like

[The scaling roadmap of Ethereum](https://ethereum-magicians.org/t/a-rollup-centric-ethereum-roadmap/4698) describes the scaling scenario focusing on Optimistic Rollup in the short term and sharding + ZK Rollup in the medium and long term.

In general, [Rollup is undoubtedly the best option for Ethereum scaling](https://www.panewslab.com/zh/articledetails/D56636383.html) due to its impressive characteristics of security and scalability. Although it takes time to solve technical problems in terms of programmability, Rollup is a very ideal scaling technology in the medium and long term. The combination of Ethereum sharding and ZK Rollup will break the so-called Impossible Triangle. At the same time, the launch of zkEVM can support programmability and help developers move to L2 more easily. 

> In the medium to long term, ZK rollups will win out in all use cases as ZK-SNARK technology improves. — Vitalik Buterin

Nevertheless, there are many issues to be addressed before ZK Rollup can be actually adopted on a large scale, including [technology](https://hackmd.io/@yezhang/S1_KMMbGt), [GTM ](https://future.a16z.com/go-to-market-in-web3)(Go to Market) and [GTC](https://future.a16z.com/community-%E2%89%A0-marketing-why-we-need-go-to-community-not-just-go-to-market/) (Go to Community).

## Technology Issues

The technology issues of the ZK Rollup have been briefly explained above, and some details are added here.

Regarding compatibility, technology problems of ZK Rollup mainly lie in the fact that it is not developer-friendly, resulting in limited functionality. Previously, it was difficult to build generic DApps mainly due to the following two reasons.

- First, if you want to develop DApp on ZK Rollup, you are required to write all your smart contract logic in a special language (i.e. [R1CS](https://tlu.tarilabs.com/cryptography/r1cs-bulletproofs/mainreport.html#rank-1-constraint-systems)). The syntax of the required language is complex. Furthermore, you have to possess comprehensive expertise in zero-knowledge proofs. 
- Second, ZK Rollup does not support composability, which means different ZK Rollup applications cannot interact with each other on L2. This quality greatly undermines the composability of DeFi applications. 

There are two ways to build a generic DApp in ZK Rollup. One is to build application-specific circuits (ASIC) for different DApps, which is the path taken by ZK Rollup in its early stages, corresponding to the “Planets” phase of StarkWare where applications cannot interact with each other. The other way is to build a general “EVM” circuit for smart contract execution, on which StarkWare and zkSync have made great progress. 

The development of StarkWare is in the “Constellations” phase for the time being. In September 2021, StarkWare announced the launch of the general ZK Rollup that is permissionless, multi-application, and supportive to smart contracts through Cairo. Meanwhile, the development of zkSync is also in the second stage. In February 2022, the zkSync 2.0 testnet was launched. Continuous testing ensures LLVM/Solidity compatibility for full EVM compatibility and smart contract composability.

Note: StarkWare and zkSync adopt two completely different technology solutions. 

StarkWare uses [Cairo, a brand new Turing-complete programming language](https://medium.com/starkware/starknet-alpha-2-4aa116f0ecfc), and works with OpenZeppelin to develop standardized contracts, just as they did with Ethereum, which means they adopt a new contract standard for composability. It’s certainly a bold decision, as it will significantly increase the entry cost for developers. For now, Nethermind’s Warp team [is helping](https://medium.com/nethermind-eth/warp-your-way-to-starknet-ddd6856875e0) developers convert ERC-20 contracts from EVM bytecode to StarkNet contracts and deploy them on StarkNet. The project is progressing rapidly, and its next goal is to move arbitrary smart contracts from Yul to Cairo.

On the other hand, [zkSync uses zkEVM solution for EVM compatibility](https://mirror.xyz/kuiqian.eth/FW6gE79ksYDgfrDOhW9zse-bGhLBzaMizIlid3iKZ8Q). For zkEVM, there are two major implementation strategies at the moment. 

- Directly supports the existing set of EVM opcodes, which is fully compatible with the set of Solidity opcodes. This strategy is used by Hermez and the Ethereum Foundation zkEVM.
- Maintaining Solidity compatibility by redesigning a new virtual machine that is ZKP-friendly and adaptive to EVM development tools. This strategy is mainly used by zkSync.

Overall, the first strategy has better compatibility and higher security, but needs more work, which is used by Hermez; the second strategy is more flexible with less work but requires extra effort in adaptation, which is used by zkSync. zkSync has developed two compiler front-ends for zkEVM at the same time: Yul and Zinc. zkSync chose LLVM to build its own compiler. The LLVM/Solidity compatibility issue is the major reason behind the [failure to launch](https://blog.matter-labs.io/zksync-2-0-developer-update-d25417f16446) zkSync 2.0 as scheduled in August 2021, which is also the issue that is currently being focused on during the launch of the zkSync 2.0 testnet.

Using Cairo makes StarkWare seem to be less compatible. Is this the weakness of StarkWare? It is not.

StarkWare uses the Cairo language to port the smart contract logic to Rollup. Although the new language somewhat increases the entry cost for developers, many features of Cairo allow ZK to integrate more elegantly into the blockchain ecosystem.For example, Cario has an accompanying Algebraic Intermediate Representation (AIR) visualization tool to view the details of proofs, securely and credibly generate zk-STARK proofs to ensure computational completeness, and the language is designed to be neater and more logically in line with mathematical proofs, and it has a complete tool chain as well.

In addition, Cairo also [increases security](https://medium.com/starkware/hello-cairo-3cb43b13b209). Cairo’s AIR is relatively simple, which leads to low efficiency and low amortized costs for both the on-chain verifier and the off-chain proving service. Besides, auditing a single simple AIR is safer than auditing multiple complicated application-specific AIRs. As a result, with Cairo, we can rely on a single Verifier smart contract; there is no longer a need to deploy a Verifier for every application used. 

Note the security implication of this property: a single set of audits for this one contract protects any application from the proof system risk since it only audits the business logic. As for the business logic, it’s much easier to understand and audit the correctness of codes than it is to comprehend application-specific AIR. Cairo cannot solve the problem of possible bugs in contracts faced by EVM currently. However, [some people](https://multicoin.capital/2022/03/15/move-move-move/?mc_cid=43fd88cdd6&mc_eid=0b68dd5aad) are trying to fix it. 

# Go-to-Market Issues

ZK Rollup gains the market in much the same way as public chains named “Ethereum killers”. StarkWare is centralized and is promoting decentralization right now, while zkSync is open source and decentralized (not at a high level), but neither of them has a token. Similarly, Optimism and Arbitrum, the other two players in the Rollup technology area, have no tokens.

zkSync will launch a token as confirmed by their source codes. StarkWare and Arbitrum have no public statements, but Optimism has launched the token recently.

Nonetheless, issuing tokens is necessary for L2s to promote decentralization and gain the market. [Tokens, as a good incentive tool, can also help to better govern the community](https://newsletter.banklesshq.com/p/rollup-tokens-are-coming?s=r). The main obstacles to issuing tokens are the immaturity of L2s cross-chain bridges and the unsettled EVM compatibility.

According to the organizational structure and economic incentive model of Web3, A16Z defines the [GTM matrix](https://future.a16z.com/go-to-market-in-web3) as follows:

![Web3 走向市场矩阵 来源：a16z](https://tva1.sinaimg.cn/large/e6c9d24egy1h2bj1p5k5dj21bu0u076h.jpg "Web3 GTM Matrix Source:a16z")

They argued that the Go to Market (GTM) strategy of Web3 is hugely different from that of Web2. The most innovative part is the introduction of tokens and the emergence of the new organizational structure Decentralized Autonomous Organization (DAO). GTM differs in each of the quadrants and can span everything from traditional web2-style strategies to emerging and experimental strategies. 

Metrics that measure whether Layer1/Layer2 gains the market include the number of Github stars, protocol developers, project integrations, protocol forks, and TVL.

![L1 公链走向市场矩阵 来源：a16z](https://tva1.sinaimg.cn/large/e6c9d24egy1h2bj2657llj21kw0fo0u4.jpg "L1 Public Chain GTM Matrix Source: a16z")

Here, there is no way to compare StarkWare as it is not open source. Looking at the data in March 2022, the situation of zkSync, Optimism and Arbitrum are as follows:

- When it comes to Github stars, zkSync comes out on top. ZkSync has 1,300 stars, slightly higher than Optimism’s 900 stars and Arbitrum’s 700 stars.
- When it comes to the number of protocol developers on Github, Optimism comes in first. zkSync has 43 developers, Optimism 66, and Arbitrum 36.
- When it comes to the number of protocol forks on Github, Arbitrum has a slightly higher number of 355, while the forks of zkSync and Optimism are quite close, being 292 and 303 respectively. 
- When it comes to TVL, Arbitrum is far ahead with $3.41 billion at present, while zkSync and Optimism stand at $148 million and $562 million respectively.

In comparison, the more successful Ethereum “alternative chain” Solana has 7,700 Github stars, 1,800 forks, 305 contributors and a TVL of $7.46 billion.

It can be seen that the present Rollups are far from being called a market winner, and there is still a lot of work to be done. The most important is to get more project integrations, since more adoption will attract more developers, thus building better eco-projects, getting more users and attracting more funding. To achieve these goals, the project side is required to Go to Community (GTC).

## Go-to-Community Issues

[It is argued](https://future.a16z.com/community-%E2%89%A0-marketing-why-we-need-go-to-community-not-just-go-to-market/) that the key difference between the incentives in GTM and GTC strategy can be summarized as the difference between value capture and value creation. For a product, it is its users that make up the community, while for a blockchain or a protocol, it is the applications that adopt it that make up the community. Therefore, it may be more accurate to use Ecosystem instead of Community here. Now, with the launch of StarkNet Alpha and zkSync 2.0 testnet, ZK Rollup technology has been adopted rapidly, and their ecosystems are also expanding. The ecosystems of the two technologies have been sorted as shown below.

Currently, with the launch of the StarkNet Alpha and zkSync 2.0 testnets, ZK Rollup technology is rapidly being adopted, and the ecosystems of both are expanding. Some people have organized the ecology of the two major technologies as shown below.

![StarkWare Landscape 来源：ZK_Daily](https://tva1.sinaimg.cn/large/e6c9d24egy1h2bj2eewsbj21gs0u07dh.jpg "StarkWare Landscape Source: ZK_Daily")

![zkSync Landscape 来源：ZK_Daily](https://tva1.sinaimg.cn/large/e6c9d24egy1h2bj2mr8ayj21gf0u0qch.jpg "zkSync Landscape Source: ZK_Daily")

The two ecosystems have comparable levels of prosperity. It can be seen that zkSync is supported by more cross-chain, DeFi and wallet applications, while there is a more prosperous Games & NFTs ecosystem on StarkWare. 

For an L1s/L2s ecosystem, [liquidity is equivalent to bandwidth](https://newsletter.banklesshq.com/p/liquidity-is-bandwidth), connecting different application scenarios to form a larger network, i.e. the Internet of Value. The definition of liquidity over here is the value exchange between different applications. When liquidity is good, there is less value loss; and when it is poor, there is more value loss. In addition, when there is no value exchange between different applications, there is no liquidity. An ecosystem is only functioning when its liquidity can run through the whole process, like the Ethereum ecosystem where every application based on Ethereum can be valued and exchanged through Ethereum.

I divide the liquidity in the ecosystem into horizontal and vertical liquidity. In L2s, the role of the bridge is to bridge between different Rollups horizontally. Recently, there is an innovative way called LayerZero, which innovates the liquidity bridging way of traditional bridges and brings better security and trustlessness. The vertical liquidity mainly lies in different applications. End Users connect to the whole ecosystem through Wallet. Sometimes they top up and buy cryptocurrency through Payment to get value and exchange value in different applications. Sometimes intermediate exchange is required through Marketplace apps.

![L2 生态价值流动图](https://tva1.sinaimg.cn/large/e6c9d24egy1h2bj2v0ef5j20ma0f9q3p.jpg "L2 Eco-value Flow Diagram")

At present, in each liquidity node, StarkWare and zkSync have corresponding applications deployed, most of which are in the testing phase, and their ecosystems are compared in the chart below.

![zkSync 和 StarkWare 生态对比 来源：ZK_Daily](https://tva1.sinaimg.cn/large/e6c9d24egy1h2bj34ji7lj21gx0u0gtw.jpg "zkSync and StarkWare Ecosystem Comparison Source: ZK_Daily")

Go to Community (Ecosystem), first of all, needs to be able to open up vertical liquidity internally, which requires support for composability so that there is a unified standard in the ecosystem that enables permissionless mutual integration between different application protocols just as Lego blocks. This is easy to do on Ethereum, but due to the zero-knowledge proof issue, both StarkWare and zkSync have worked very hard to solve this problem.

The prerequisite for a vibrant community (ecosystem) is to have good horizontal liquidity, which requires the support of useful bridges that can bridge the liquidity of Ethereum at a low cost and, more importantly, can easily communicate with other L2 solutions or even L1 solutions. A fast (high TPS), low cost (low fees) and secure blockchain are naturally attractive for both applications and users. The lower the migration cost, the more attractive the ecosystem is to both applications and users.

The necessary condition for a community (ecosystem) to take off is the emergence of the killer app that draws a large number of users and capital in. This cannot be achieved only through high APY, token airdrops or subsidies and a closed “play to earn” ecosystem.

# How to Invest in Scaling Ecosystem

Blockchain is the Internet of Value, while the traditional Internet is the Internet of Information; Information data is transmitted by bandwidth, while value exchange is undertaken by liquidity. The first thing that the public chain ecosystem needs to achieve is the flow of value, followed by the efficient exchange of value. Then, based on the efficient exchange of value, productivity increased by establishing applications that meet the needs of users, and finally a blockchain world created featured in efficiency, permissionlessness and censorship resistance, endowed with democratic and anti-vice mechanisms that are open inclusive and transparent.

Thanks to smart contracts, the blockchain application is not only limited to being a decentralized ledger but also generates new things such as Non-fungible Token for ownership definition in the digital world and DAO, a new governance organization structure with homogeneous tokens as the cornerstone of governance. These innovations, combined with existing Internet applications, have given rise to more application scenarios, but the current blockchain infrastructure is not well equipped to support the implementation of these application scenarios.

First is the issue of scaling. Both TPS and data availability need scaling. This has been explored by ZK Rollup and Validium and their work has been productive. In addition, there are other Layer 2/Layer 1 solutions such as Optimistic Rollup, Plasma, Solana and Celestia. Scaling technology itself is the best investment target. At this stage, we can put more attention to the on-chain storage technology. After scaling, high TPS and reliable data availability can greatly improve the performance of the blockchain, which allows more complex applications to be built on the blockchain. These applications can be divided into two categories: Internet product blockchainlized and Blockchain original innovation.

- Internet product blockchainlized: The most obvious examples are the applications in the GameFi field, such as GameFi on-chain real-time matchmaking settlements, on-chain real-time communication and large-scale payments.
- Blockchain original innovation: High-performance blockchain infrastructure allows more frequent and intensive value exchange behavior than before, which will greatly promote the cost-efficiency of value flow. Innovative applications should be those that can truly improve the efficiency of capital utilization and thus achieve higher productivity. Moreover, high-performance blockchains make it possible to achieve [data capital market](https://www.amazon.com/%E6%95%B0%E6%8D%AE%E8%B5%84%E6%9C%AC%E6%97%B6%E4%BB%A3-%E6%89%98%E9%A9%AC%E6%96%AF%C2%B7%E6%8B%89%E5%A7%86%E4%BB%80-Thomas-%E7%BB%B4%E5%85%8B%E6%89%98%C2%B7%E8%BF%88%E5%B0%94-%E8%88%8D%E6%81%A9%E4%BC%AF%E6%A0%BC-Mayer-Sch%C3%B6nberger/dp/B07KLFLYH9) liquidity, which is a groundbreaking innovation that allows data, as a factor of production in the information age, to flow and be applied fully, with reasonable and fair benefit distribution.

Next is the issue of liquidity, which is divided into horizontal and vertical liquidity here. 

- Horizontal liquidity refers to the transfer of value among different public chains/L2 ecosystems. When a new public chain/L2 ecosystem is formed, users need a good value exchange tool, sometimes called a bridge, to migrate from the original ecosystem. Currently, traditional bridge tools have some security issues, which may lead to the loss of users' money and sometimes even trigger chain effects. The good news is that there are new bridge technologies, such as Layerzero, and it is believed that there will be more and better technologies, such as zk bridges which are expected to [solve many problems](https://hackmd.io/@kalmanlajko/rkgg9GLG5) about bridges currently exist. Bridges, as a liquidity portal of ecosystem’s value, can generate more DeFi applications thus capturing more value.

[https://twitter.com/pseudotheos/status/1511342937262759939](https://twitter.com/pseudotheos/status/1511342937262759939)

- Vertical liquidity refers to the transfer of value within the same L1/L2 ecosystem. The optimization of vertical liquidity contributes more to the efficient flow of value, thanks to various innovative DeFi applications including AMM, Yield Farm and Lending. Efficient applications result in less value loss in the exchange process and the value captured in this segment is undoubtedly huge. However, the current solutions are not good enough, as most of them provide liquidity by locking it, which is not an efficient way to use funds. Novel solutions in this area include Tokemak and dAMM, and we can look out for more L2 applications in this area.

The third is the issue of data privacy. No company wants to make all its financial data public so that the whole network can audit its every financial flow. The blockchain on-chain data is in the HTTP era of the Internet, where all information is “transmitted” in clear text, while the emergence of ZK technology can make the blockchain embrace the HTTPS era. It can be believed that almost every transaction on the blockchain in the future can be protected by zero-knowledge technology. At that time, blockchain technology will be able to penetrate every corner of society and protect privacy of transactions while ensuring trustlessness, tamper-proof, openness, security and transparency. The best way to guarantee privacy is in the form of a protocol, serving as a plug-in, which can be built together with other protocols like Lego blocks, and it can be configured, owned and censorship-resistant. In the foreseeable future, the privacy protocol will be mandatory for every application.

Lastly, the wallet plays a crucial role as the gateway to the blockchain world. If compared with the Internet, wallet is like the browser in the Internet era. Information interacts with people through the browser, but value interacts with people through the wallet. It is said that we have entered the Netscape era of blockchain, and MetaMask may be the Netscape that flourished back then, although their endings may be different. However, I think the wallet is far from being good at this moment. One of the most important points is that value does not flow efficiently between different wallets. There may be some compatibility issues that affect interoperability here, but undoubtedly, we need a universal set of standards to define this value interface.

The mentioned above is the infrastructure, the area where value is created and begins to be captured. Only after these issues are improved (which may not be exhaustive) will blockchain technology be able to take off and the Internet of Value be able to connect everyone.

Inside the previous public chain ecosystem, the value was mainly captured by protocols, firstly in the public chain itself, and then in the DeFi field, especially in exchanges and exchange platforms. Here we can refer to the famous [Fat Protocol Theory](https://www.usv.com/writing/2016/08/fat-protocols/), which has always been [debatable](https://messari.io/article/analyst-notes-cracks-in-the-fat-protocol-theory). For the moment, however, Fat Protocol Theory is generally correct. In my opinion, this is because the blockchain infrastructure era is still far from over.

Infrastructure construction is long, difficult and labor- and material-intensive, but it is the area with the most notable moat effect. On top of the infrastructure, applications that can bring great benefits are called kinetic applications, and those that create the most value effects must be kinetic applications. To be the infrastructure or the kinetic application is not unchanging, for example, Taobao, once the kinetic application of the Internet, but now serves as a platform that is gradually becoming the infrastructure of Ant Group. The core purpose of infrastructure is to pave the way for kinetic applications and reduce the adoption cost of kinetic applications.

The kinetic age of blockchain has not yet arrived, and as it does, there is no doubt that the Fat Protocol Theory will fail (although some problems have already emerged). At this moment, it would be wise to bet on the infrastructure track that can reduce the cost of application adoption. The adoption cost includes not only economic costs, but also efficiency, technology thresholds, and even belief costs (reflected in blockchain fundamentalism such as decentralization, trustlessness, and censorship resistance).

With the gradual application of ZK Rollup in the L2 era and even [the arrival of the era of L3 and L4](https://medium.com/starkware/fractal-scaling-from-l2-to-l3-7fe238ecfb4f), the kinetic era of blockchain will surely become predictable. So who is the leading role in the kinetic era? It must come from areas that could emerge killer applications. These areas include games, entertainment, social networks and virtual reality. Early betting in these areas is also a desirable investment. However, given the difficulty and return ratio, it is not very cost-effective at this stage. When investing in these areas, you can fully consider whether they make full use of the new infrastructure or retain full scalability for the new infrastructure, which enables fast enough,high-value cost control and efficiency improvements. It will greatly improve their competitiveness in the rapidly evolving blockchain infrastructure era.

# References

[Zero Knowledge Cryptography & the Next Digital Revolution - ZK Podcast](https://zeroknowledge.fm/zero-knowledge-cryptography-the-next-digital-revolution/)

[A rollup-centric ethereum roadmap](https://ethereum-magicians.org/t/a-rollup-centric-ethereum-roadmap/4698)

[一文了解Layer2的四大解决方案交易成本对比](https://w3hitchhiker.mirror.xyz/7dwD76ZZIlR7ep731K6y9vTTuXGHOojxWSnkXKzqPzI)

[zkEVM - HackMD](https://hackmd.io/@yezhang/S1_KMMbGt)

[Ethereum's Ultimate Scaling Explanation and Directory](https://mirror.xyz/0x3D5FE39342e661776bb5273521F52E99B624288c/NFOsWYCb2eVk612VSnrrCsoKcwI_EMObp_q9uNKa4uA)

[zk-rollup 争夺战：zkSync vs. StarkWare](https://news.ethereum.cn/Layer2/zksync-vs-starkware)

[吊打 Optimistic Rollups？StarkWare 的 L2 赛道大揭秘 | Unitimes AMAes AMA](https://www.geekmeta.com/article/3421070.html)

[StarkNet 中文开发者 Meetup（文字版）](https://mp.weixin.qq.com/s/r7cNMWYPP-9sqjLcKz64Aw)

[Composability is Innovation](https://future.a16z.com/how-composability-unlocks-crypto-and-everything-else/)

[探索以太坊扩容之路：哪个方案才是未来？-PANews](https://www.panewslab.com/zh/articledetails/D56636383.html)

[Go-to-Market in Web3: New Mindsets, Tactics, Metrics](https://future.a16z.com/go-to-market-in-web3)

[Go-to-Market in Web3: New Mindsets, Tactics, Metrics](https://future.a16z.com/go-to-market-in-web3)

[Community ≠ Marketing: Why We Need Go-to-Community, Not Just Go-to-Market](https://future.a16z.com/community-%E2%89%A0-marketing-why-we-need-go-to-community-not-just-go-to-market/)

[StarkNet Alpha 2](https://medium.com/starkware/starknet-alpha-2-4aa116f0ecfc)

[以太坊扩容方案的明珠](https://mirror.xyz/kuiqian.eth/FW6gE79ksYDgfrDOhW9zse-bGhLBzaMizIlid3iKZ8Q)

[Hello, Cairo!](https://medium.com/starkware/hello-cairo-3cb43b13b209)

[Multicoin Capital: Move Move Move](https://multicoin.capital/2022/03/15/move-move-move/?mc_cid=43fd88cdd6&mc_eid=0b68dd5aad)

[Layer 2 Tokens Are Coming](https://newsletter.banklesshq.com/p/rollup-tokens-are-coming?s=r)

[Liquidity is bandwidth](https://newsletter.banklesshq.com/p/liquidity-is-bandwidth)

[Fat Protocols | Union Square Ventures](https://www.usv.com/writing/2016/08/fat-protocols/)

[Analyst Notes: Cracks in the Fat Protocol Theory](https://messari.io/article/analyst-notes-cracks-in-the-fat-protocol-theory)

[Fractal Scaling: From L2 to L3](https://medium.com/starkware/fractal-scaling-from-l2-to-l3-7fe238ecfb4f)

[Geometry presents: Slush, a proposal for Fractal scaling - HackMD](https://hackmd.io/@kalmanlajko/rkgg9GLG5)

# Worth Reading

[Uhttps://www.bubais.top/en/tech/nft-a-revolution/nfollow The Money](https://wrongalot.substack.com/p/unfollow-the-money?token=eyJ1c2VyX2lkIjo2NTk5MTM0MCwicG9zdF9pZCI6NTAzNjg3NjYsIl8iOiI3VnR1NSIsImlhdCI6MTY0NzM1Njc5MiwiZXhwIjoxNjQ3MzYwMzkyLCJpc3MiOiJwdWItMjU5MTUiLCJzdWIiOiJwb3N0LXJlYWN0aW9uIn0.lYPfVwsDOu7GtYm4WMA6wlK0XyPGAGXaqlFDkjDGLCg&s=r)

[A Look Under the Hood Into Ethereum Technology and Scaling Solut...](https://mirror.xyz/0x3D5FE39342e661776bb5273521F52E99B624288c/I_zTz72C8lZtteRYBxco9p2iPUE77a6rwtgRWeP9e-s)

[What is ZEXE? (Part I) - ZK Podcast](https://zeroknowledge.fm/what-is-zexe-part-i/)

[What is ZEXE? (Part II) - ZK Podcast](https://zeroknowledge.fm/what-is-zexe-part-ii/)

[What is ZEXE? (PART III) - ZK Podcast](https://zeroknowledge.fm/what-is-zexe-part-iii/)

[WTF is Data Availability?](https://medium.com/blockchain-capital-blog/wtf-is-data-availability-80c2c95ded0f)

[Understanding rollup economics from first principles](https://barnabe.substack.com/p/understanding-rollup-economics-from?utm_source=url#footnote-anchor-1)

[A normie's guide to rollups](https://www.preethikasireddy.com/post/a-normies-guide-to-rollups)

[The ultimate guide to L2s on Ethereum](https://dcbuilder.mirror.xyz/QX_ELJBQBm1Iq45ktPsz8pWLZN1C52DmEtH09boZuo0)

[The best ways to invest in Layer 2](https://newsletter.banklesshq.com/p/the-best-ways-to-invest-in-layer?s=r)

[Blockchain Bridges](https://medium.com/1kxnetwork/blockchain-bridges-5db6afac44f8)

[详解10大Layer1与4大Layer2年度进展与竞争格局 |链捕手](https://mp.weixin.qq.com/s?__biz=MzU4MTQwMzMxOA==&mid=2247488686&idx=1&sn=a02c7db30f3dddb87ce1a1376b612d9c&chksm=fd494377ca3eca6189517e9c3cf739c2b352417928dccf066dc5cf748614dda77081eb97b89a&scene=21#wechat_redirect)