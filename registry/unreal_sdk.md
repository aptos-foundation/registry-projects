**Project Information**
- Title: Aptos Unreal SDK
- Vertical: Gaming

**Motivation** 

As Aptos engages with more game developers to build on our chain, many developers are asking for ways to speed integration to the chain via an SDK. We currently have an [Aptos-verified SDK on the Unity Store](https://assetstore.unity.com/packages/decentralization/aptos-sdk-244713), and [Unreal Engine 5](https://www.unrealengine.com/en-US/unreal-engine-5) is the second-largest game engine.

As part of producing this, we expect this to be structured as a C++ SDK, which is then used within Unreal- this benefits the ecosystem as some backends are written in C++. The goal is to enable game developers to increase the number of SDKs with feature parity to our [Typescript SDK](https://github.com/aptos-labs/aptos-core/tree/main/ecosystem/typescript/sdk) - our primary, and most feature-complete, SDK, by following our [SDK spec](https://github.com/aptos-labs/aptos-core/blob/main/ecosystem/typescript/sdk/SPEC.md).

**Deliverables** 
As mentioned above, there are two pieces to this:

1. C++ Aptos SDK, following the [SDK spec](https://github.com/aptos-labs/aptos-core/blob/main/ecosystem/typescript/sdk/SPEC.md). The recommended development order/milestones are below, but the [SDK spec](https://github.com/aptos-labs/aptos-core/blob/main/ecosystem/typescript/sdk/SPEC.md) is the source of truth for all required features and implementation details.
    1. [BCS Encoding & Decoding](https://github.com/aptos-labs/aptos-core/blob/main/ecosystem/typescript/sdk/SPEC.md#1-BCS-Encoding--Decoding)
        1. Encoding of all primitive and complex types
        2. Idiomatic encoding/decoding of structs, or other representations of complex, nested data
    2. [API Interactions](https://github.com/aptos-labs/aptos-core/blob/main/ecosystem/typescript/sdk/SPEC.md#2-API-servers)
        1. Node REST client
        2. Indexer Graphql client
        3. Custom endpoint URL support
    3. [Account Management](https://github.com/aptos-labs/aptos-core/blob/main/ecosystem/typescript/sdk/SPEC.md#3-Account-Management)
        1. Account creation (Ed25519 key generation)
        2. Loading keys (files, byte arrays, etc)
        3. Account rotation
        4. Reading account balances and resources
        5. Mnemonic support
        6. Multi-agent signer support
    4. [Transactions](https://github.com/aptos-labs/aptos-core/blob/main/ecosystem/typescript/sdk/SPEC.md#4-Transaction)
        1. Entry function support
        2. Script function support
        3. Transaction simulation API support
        4. View function payload support
        5. Gas estimation API support (with local caching)
    5. [Coin Management](https://github.com/aptos-labs/aptos-core/blob/main/ecosystem/typescript/sdk/SPEC.md#5-Coin-Management)
        1. Transfer of APT
        2. Transfer of other coins
    6. [Testing & Logging](https://github.com/aptos-labs/aptos-core/blob/main/ecosystem/typescript/sdk/SPEC.md#9-documentation)
        1. Thorough test coverage
        2. Github CI on PRs
2. Unreal “Demo” scene
    1. A mini “demo wallet” that:
        1. Allows for key generation/import, and stores the key locally
        2. Allows the minting of an NFT, and fetching/displaying it to the user

We expect flexibility for the developer to select devnet, testnet, mainnet, or custom endpoints as the target, and have the SDK work with them.

**What we are looking for** 

The Aptos C++ SDK, and Unreal Engine 5 SDK, should be a clean and idiomatic port of the typescript SDK to C++. It should adhere to any Epic guidelines for approval in their Unreal marketplace.

**Grant amount**

Up to $75k USD
