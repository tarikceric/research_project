# Analyst Research Project
Cryptocurrency analytics project with Jupyter notebook and Dune Dashboard information

- Project 1: Data Visualization - [NEAR Ecosystem Exploration](https://github.com/tarikceric/research_project/blob/main/NEAR_analysis.ipynb)
- Project 2: Dune Dashboard - [BNB Chain game-theory analysis](https://dune.com/tarcer/game-theory-in-bnb-chain)

### Setup

Install dependencies:
- ```virtualenv venv```
- ```source venv/bin/activate```
- ```pip3 install -r requirements.txt```

Start Jupyter Notebook
- ```jupyter notebook```


# Project 1: NEAR Ecosystem Exploration

NEAR is a proof-of-stake layer-1 blockchain that utilizes a unique sharding approach to address scalability and throughput challenges that plaque other chains. Due to it being a non-EVM chain, data tends to be more sparse and challenging to collect, in contrast to EVM-compatible chains. Additionally, a separate smart-contract platform with EVM capabilitiy called Aurora was built on top of the NEAR blockchain, which provides a connection between NEAR and the Ethereum ecosystem. Aurora has played a significant role in the growth of the NEAR ecosystem, where it almost rivals its predecessor in size.

In this notebook I showcase different methods for extracting NEAR/Aurora data from various types of sources, and create visuals that are not widely used. This includes:

- TVL comparison across top 5 protocols in NEAR and Aurora - (source: DefiLlama)
- Bridging activity to NEAR in relation to other chains (source: Dune Dashboards)
- Metapool staking trend (source: DappLooker)
- Extra explorattion: Utilize subgraphs to get the number of daily new accounts

### Charts

![alt text](https://github.com/tarikceric/research_project/blob/main/images/Metric%201%20-%20protocol%20tvl.png)

![alt text](https://github.com/tarikceric/research_project/blob/main/images/metric%202%20-%20bridges.png)

![alt text](https://github.com/tarikceric/research_project/blob/main/images/metric%203%20-%20metapool%20staking.png)

![alt text](https://github.com/tarikceric/research_project/blob/main/images/exploratory%20-%20users.png)


# Project 2: BNB Chain game-theory analysis

Dune Dashboard - [BNB Chain game-theory analysis](https://dune.com/tarcer/game-theory-in-bnb-chain)

This Dune dashboard focuses on displaying analytics that are more game-theory based, in an effort to showcase a more unique approach to understanding activity across the BNB Chain. It features a collection of graphs that I believe are different from what most competitors use, by utilizing some creativity in displaying information that may be useful to users. I also avoided including metrics that can be easily found anywhere, as this was an attempt at thinking out-of-the-box and not simply recreating metrics that are readily available.

## Metric categories:

### Stablecoin activity on BNBChain
- metrics that display the amount of activity related to stablecoins, which can convey that market participants are more risk-averse, as opposed to transacting with BNB or other BEP20 tokens which are much more volatile. The theory is that if less activity is based on stablecoins, then the market is expecting positive growth as they rotate into other tokens.

### Comparison to Competitor Chains
- putting BNB Chain head-to-head with its competitors, as well as understanding the chains that BNB users commonly move over to. With a number of chains existing in the crypto ecosystem, its key to understand their performance and what market participants are still willing to use, especially in a serious down market.


### dApps and Tokens 
- exploring the largest DEX on BNBChain (Pancake Swap), dApps that are seeing growth in users, as well as other BNBChain user trends


