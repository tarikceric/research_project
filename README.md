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

## Charts

### TVL comparison across top 5 protocols in NEAR and Aurora - (source: DefiLlama)

- Total value locked is a useful guage for determining which protocols are experiencing the highest level of engagement and volume. There is not much insight available on the web that compares the different protocols within Near/Aurora, so this section focuses on understanding which protocols actually make up the majority of TVL in the ecosystems, as well as analyzing what trends are currently taking shape.

Chart:
- Displays the TVL of the top 5 protocols on Aurora and NEAR. 
- In the month of May, Aurora's TVL was almost double that of NEARs, but that rise was shortlived as it quickly decreased to be even lower than NEARs (NEAR: 300m vs Aurora: 250m) 
- Ref Finance, the main DEX on NEAR, has seen fairly consistent TVL even with the recent bear market

![alt text](https://github.com/tarikceric/research_project/blob/main/images/Metric%201%20-%20protocol%20tvl.png)

### Bridging activity to NEAR in relation to other chains (source: Dune Dashboards)

- Dune is a powerful tool for querying on-chain data, but it does not currently have a API which would allow for easier access outside of the Dune platform. Although, if data is available online there is most certainly exists some way to extract it, and in this case a 3rd party library is used to grab data from a Dune dashboard.

- The data being explored is the total value locked by bridges from the Ethereum network. Cross-chain bridges operate by 'locking' assets on the chain where they originate from, and then new tokens are provided on the recieving blockchain. The bridges TVL is then a reflection of the amount of volume being bridged over to another chain.

Chart:
- This graph displays the TVL of chains that interact with Ethereum. Ethereum is by far the largest smart-contract platform, and a majority of bridging activity is performed through Ethereum.
- Polygon has held its TVL fairly consistently, and this can be interpreted as meaning that users tend to stay within the Polygon ecosystem, or that there is an equal amount being bridged in and out. Other EVM chains such as Avalanche and Fantom have experienced a significant drop off, which would mean a decrease of capital 'rotating' into these chains, as users may not see value in participating in those ecosystems.

![alt text](https://github.com/tarikceric/research_project/blob/main/images/metric%202%20-%20bridges.png)

### Metapool staking trend (source: DappLooker)

- Metapool is the inhouse dApp for liquid staking in Near. In return for staking NEAR tokens, Metapool provides stNEAR which can be utilized across a number of dApps in the Near ecosystem. Liquid staking is a very popular approach to managing assets, as a user is able to recieve attractive yields from staking while still maintaining access to their capital, allowing them to participate in the market via stNEAR.

- The datasource utilized is DappLooker, which is one of the only platforms that supports data for the Near chain. In this scenerio I have built a dataset in DappLooker, and use an HTTP get request to extract the response data.

Chart: 
- Showcases the daily amount of new NEAR stakes compared to the amount that was unstaked. The total staked NEAR is displayed in the background as an area figure.
- A significant amount of NEAR is being unstaked every day, with a very miniscule amount of new staking taking its place. This downtrend can also be seen in the gradually decline in the total NEAR staked. 
![alt text](https://github.com/tarikceric/research_project/blob/main/images/metric%203%20-%20metapool%20staking.png)


### Extra exploration: Utilize subgraphs to get the number of daily new accounts

NEAR is a Non-EVM chain, so most major data providers do not cover it. Specific metrics are more difficult to access, but there are other tools that can be utilized to retrieve harder-to-retrieve datasets.

- The Graph is currently developing subgraphs to index the Near chain and allow for more widely-available data retrival. Currently, they are still in the process of developing these subgraphs, but there are community-created subgraphs that can be queried.
- Ths subgraph being explored here only contains data on the creation of new accounts. This is an exercise in showcasing how data can be retrieved via a graphQL query and python.
- subgraph used: https://thegraph.com/hosted-service/subgraph/chainscore/near-subgraph?query=Example%20query

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


