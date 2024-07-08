# Registry: Prediction Markets

### Overview

Prediction markets efficiently gather and synthesize dispersed information and diverse opinions from participants, leading to more accurate forecasts. Reputable examples include [Polymarket](https://polymarket.com/) and [Augur](https://augur.net/). By aligning financial incentives with accurate predictions, prediction markets encourage participants to reveal their true beliefs, leading to more accurate predictions. By building permissionless prediction market platforms on Aptos, developers could further enhance these benefits by leveraging the blockchain's performance, transparency, decentralization, and security features

Operating a prediction market may be regulated or prohibited in certain jurisdictions. To the extent these activities are prohibited in certain jurisdictions, applicants are required to limit access in such jurisdictions. Applicants must ensure that their applications are compliant with all relevant laws
### Key Features

- **Prediction Mechanism**: Participants buy and sell positions representing possible outcomes of events, with payouts based on the realized outcome
- **Market Interpretation**: Prices of traded predictions act as the probability of each outcome
- **Application Areas**: Used for forecasting in politics, sports, finance, and scientific studies
- **Matching Buyers and Sellers**: Platforms use automated market makers or order book trading mechanisms

### Example Markets to Target

1. **Sports**:
    - **Major League Events**: NFL, NBA, MLB, Premier League soccer
    - **International Tournaments**: FIFA World Cup, Olympics, Wimbledon
    - **Player Performances**: Statistics, transfers, retirements
    - **Season Outcomes**: Playoff qualifications, championship winners
2. **Politics**:
    - **Election Outcomes**: Presidential, congressional, local elections
    - **Legislative Actions**: Passage of key legislation, policy decisions
    - **International Relations**: Diplomatic events, treaties, conflicts
    - **Political Milestones**: Cabinet formations, leadership changes
3. **Finance**:
    - **Stock Market**: Price movements of major stocks, IPO outcomes
    - **Economic Indicators**: GDP growth, unemployment rates, inflation rates
    - **Corporate Events**: Mergers, acquisitions, earnings reports
4. **Entertainment**:
    - **Award Shows**: Outcomes of Oscars, Grammys, Emmys
    - **Box Office**: Opening weekend earnings, total box office revenues
    - **TV Shows**: Plot developments, character fates in popular series
    - **Celebrity Events**: Marriages, divorces, public controversies
5. **Science and Technology**:
    - **Research Breakthroughs**: Significant discoveries, Nobel Prize winners
    - **Tech Innovations**: New product releases, technology adoption rates
    - **Space Exploration**: Mission outcomes, satellite launches, planetary discoveries
    - **Medical Advances**: FDA approvals, vaccine developments, major health studies
6. **Weather and Environment**:
    - **Climate Events**: Predictions on hurricanes, heatwaves, and major weather events
    - **Environmental Policies**: Adoption of climate regulations, environmental treaties
    - **Natural Disasters**: Earthquake occurrences, volcanic activities
    - **Conservation Efforts**: Success of wildlife protection initiatives, deforestation rates
7. **Miscellaneous**:
    - **Cultural Trends**: Fashion trends, social media challenges, viral phenomena
    - **Education**: Adoption of new educational policies, university ranking changes
    - **Real Estate**: Housing market trends, property price fluctuations
    - **Travel and Tourism**: Tourist arrival numbers, new travel regulations, popular destinations

### Example Smart Contract Functions

1. **Create Market**: This function allows users to create new prediction markets. It would require parameters such as the event or question being predicted, the conditions or outcomes users can predict, and other relevant market details.
2. **Place Prediction**: Users can use this function to place predictions on the outcomes of existing markets. They would specify the market, the condition they are predicting on, and the amount they are wagering.
3. **Resolve Market**: After the event or condition is determined, this function is used to resolve the market and distribute winnings to the users who made correct predictions. It should take into account oracle data for accurate resolution.
4. **Withdraw Winnings**: Users who have made correct predictions should be able to withdraw their assets from the smart contract to their wallets.
5. **Market Information**: Provide functions to retrieve information about active markets, their conditions, and other relevant details.
6. **Audit Trail**: Implement a function to log all interactions with the smart contract, ensuring transparency and accountability.
7. **Oracle Integration**: Smart contracts should have the ability to integrate with trusted oracles (Pyth, SwitchBoard, SupraOracles) to fetch real-world data for market resolution.
8. **User Balances**: Allow users to check their account balances within the smart contract, including their available funds and pending predictions.
9. **Cancel**: Users might want to cancel their prediction before the market is resolved. Implement a function to allow for cancellation under certain conditions.
10. **Market Expiry**: Define a mechanism to automatically close markets after a specified time to prevent utilization of outdated events.

---

Funding estimate: $100-150k depending on quality of team

Target teams to fund: 1
