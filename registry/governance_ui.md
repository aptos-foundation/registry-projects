**Project Information**

- Title: Aptos Governance Portal
- Vertical: Governance

**Motivation**

The Aptos blockchain supports voting in on-chain governance from any token holder, therefore leading to further decentralization of the network and more flexible architectures for upgrading the code. Token holders can participate in the governance process by direct voting or by delegating their voting power to other entities. Holders can also look into proposed AIPs and corresponding governance proposals to enable the corresponding features. 

**Main goals of Aptos Governance Portal**

- Allows token holders to connect any wallet supported by Aptos Wallet Adapter, vote on governance proposals, and delegate to any voter address
- Build a delegate portal to allow interested entities to create delegate profiles and receive voting power from other entities
- Build a notification system to alert token holders when there are new governance proposals
- Build a page for Aptos Improvement Proposal (AIP) statuses and discussions using Github as the source of truth
- Build an engagement program around governance participation

**Deliverables**

- Governance UI: Token holders can:
    - View governance proposals. UI should highlight the type of the proposals - framework upgrades, feature flags, etc. and the core proposal content - e.g. which exact feature flags are getting turned on/off.
    - View (as embedded views) the corresponding AIPs and any associated discussions (on Github or custom forum)
    - View whether the governance proposal is verified (bytecode matches the proposal script)
    - Vote for governance proposals
    - View who has voted on specific governance proposals with support for ANS v1/v2, details on whether the voter is direct or delegated to, etc.
        - Export feature to export to csv
    - View proposal status, including which steps have been executed
    - Opt in for email notifications on specific proposals - votes reaching certain thresholds, proposal passes/fails or is executed
- Delegate/Profile UI:
    - Users can delegate voting power to known delegates and view their current delegations
    - Delegates can view their voting powers across different pools and who have delegated to them
    - Show all the proposals they have created
    - Delegates can set up their profile (e.g. description, associated ANS domain, etc.) that is viewable by delegatees. Their profile page also shows their past votes.
        - Write down notes for why they voted on specific proposals
    - Users can also look up past votes for a specific account even if they’re not a delegate
    - Delegation leaderboard - This should show “top delegates” based on number of delegators, total voting power, and participation rate
- Notification system
    - Users can opt in for notifications when there are new governance proposals
    - Users can also opt in to get notified for new AIPs (by categories as well)
- AIP page
    - View all Aptos Improvement Proposals
        - With status on whether they have been implemented/launched
    - Participate in discussions with the community. Ideally synced with Github but can be standalone if UI is polished enough
- On going support for at least 6-12 months
    - Any critical requirements as we go through the ~5-10 releases in that time frame
    - Any critical updates such as correcting any description/metadata issues for proposals
 
**Grant Amount**
- Total effort estimation: ~$50k (4 months for 2 engineers - FE + BE and ~1-2 months of work for one designer + 1 month of maintenance/bug fixes)
