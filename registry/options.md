### Overview

Digital asset derivatives typically take the form of futures contracts, particularly perpetual futures contracts that don't expire as traditional commodity or index futures contracts do and there are hundreds of cryptocurrencies with off or on-chain futures contracts available

On-chain options volume accounts for less than 1% of total on-chain derivative volume. This disparity highlights the untapped potential of on-chain options trading but also highlights a problem: why is there a disparity? There’s no quick answer to that although there hasn’t been a protocol to build feature parity (advanced order types in a liquid market, accessible UI, multi-leg strategies) with industry incumbents while extending functionality via blockchain primitives (collateralization fast performance, permissionless vaults)

As there is no standard protocol implementation, we’re looking to fund two teams with different protocol implementations for this registry item

Please note that derivatives trading is regulated in certain jurisdictions. Applicants must ensure that their applications are compliant with all relevant laws. To the extent these activities are prohibited in certain jurisdictions, applicants are required to limit access in such jurisdictions

### Implementations

1. On-chain implementations
    
    Using ThreeSigma’s [analysis](https://threesigma.xyz/blog/defi-options-landscape) as a guide, you can can consider 4 categories that most on-chain options fall into.
    
    1. [**Orderbooks](https://www.investopedia.com/terms/o/order-book.asp)** 
        1. [Econia](https://www.econialabs.com/) is the Aptos’ first fully on-chain order book and can serve as a liquidity layer for you to build options with 
        2. Protocols for reference: [Aevo](https://www.aevo.xyz/), [PsyFi](https://www.psyfi.io/), and [Zeta](https://www.zeta.markets/)
    2. **AMMs** - Automated Market Makers
        
        A common model which can be broken down into two categories:
        
        1. 1st Wave - users only buy (go long) options
        2. 2nd Wave - more advanced use cases. [Lyra](https://lyra.finance/), [Deri](https://deri.io/), and [Hegic](https://www.hegic.co/) can be used as references
    3. **Structured Products**
        
        Custom, automated strategies that often involve the selling of options
        
        1. Examples include [Cega](https://app.cega.fi/), [JonesDAO](https://www.jonesdao.io/), [KnoxVaults](https://www.knoxvaults.com/), [Opium](https://opium.finance/), and [Polynomial](https://www.polynomial.fi/)
    4. **AMM Powered**
        
        Option protocols built on top of pre-existing liquidity layers supplied by DEXes like Uniswap
        
        1. LiquidSwap/Pontem’s DEX includes formally verified concentrated liquidity pools that can be used as a basis for derivative platforms
        2. Examples include [Panoptic](https://www.panoptic.xyz/), [GammaSwap](https://gammaswap.com/), and [Smilee](https://smilee.finance/)
2. Options categories
    
    Options themselves fall into one of three categories
    
    - [**European**](https://www.investopedia.com/terms/e/europeanoption.asp) options can only be exercised or settled at the expiration date
    - [**American**](https://www.google.com/search?q=investopedia+american+options&sourceid=chrome&ie=UTF-8) options can be exercised anytime before expiration
    - [**Bermudian**](https://www.investopedia.com/terms/b/bermuda.asp) options can be exercised at specific pre-expiration dates
    
    American options are the most widely adopted options as they provide investors maximum control over their investment by being able to exercise them at any time


## Specifications

A decentralized on-chain options platform that enables traders to buy, sell, and manage options contracts in a secure, efficient, and scalable manner 

Built using one of the implementations listed under [Implementations](https://www.notion.so/Registry-Options-edcf6446583147deadc341f90a97c555?pvs=21)

1. Using Econia’s fully on chain order book
2. Building a custom AMM (wave 2)
3. Building a structured product
4. AMM powered - Using Pontem’s concentrated liquidity AMM or Mirage’s liquidity layer

### **Key Features**

1. Decentralized and transparent settlement
2. Interoperability with other Aptos DeFi protocols
3. Flexible strike prices for assets
4. Yield Bearing Collateral: 
    1. The platform permits traders to employ yield-bearing assets as collateral, such as [MOD](https://docs.thala.fi/thala-protocol-design/move-dollar-mod/stablecoin), [MKLP](https://docs.merkle.trade/merkle-lp), RWAs, etc., rather than solely relying on stablecoins or other assets
5. Liquidation Engine: 
    1. The platform features a straightforward and transparent liquidation engine that avoids reliance on loosely defined parameters
    2. The engine is designed to:
        - Monitor trader positions and margin levels in real-time
        - Trigger liquidation when a trader's margin falls below a specified threshold
        - Execute liquidation orders in a fair and transparent manner

### Example Smart Contracts

1. **Options Contract Factory:** Responsible for the creation of individual options contracts, setting terms like strike price, expiration date, and underlying asset
2. **Trading Contract:** Manages the buying, selling, and exercising of options. This includes trade matching, order management, and ensuring trade execution according to the specified terms
3. **Collateral Management Contract:** Handles the deposit, withdrawal, and monitoring of collateral used in trades, supporting both standard and yield-bearing assets
4. **Margin System Contract:** Implements cross-margining features, calculating required margin levels, margin calls, and handling opt-in/opt-out mechanisms for traders
5. **Liquidation Contract:** Activates and executes liquidations when necessary, based on predefined rules regarding margin requirements and position monitoring
6. **Settlement Contract:** Manages the settlement process post-expiration of options contracts, ensuring that payoffs are executed correctly
7. **Governance Contract:** Facilitates platform governance, allowing for updates and modifications to parameters or features as dictated by protocol stakeholders
8. **Oracle Contract:** Integrates external data feeds to provide real-time pricing information of underlying assets

