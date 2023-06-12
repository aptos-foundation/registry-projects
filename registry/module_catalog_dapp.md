**Project Information**

- Title: Module Catalog DApp
- Vertical: Move
- Labs POC: Developer Platform team (greg@aptoslabs.com)

**Motivation** 

In the Aptos Network, code is deployed on package level, together with metadata. Both the metadata and the code can be queried over the Web API. The Aptos CLI supports building Move code with dependencies pointing into the network.

While all the data is available on chain, there is no catalog of the available packages, as e.g. Rust has with `crates.io`. This project aims to build a DApp which closes this gap.

**Design Notes**

In contrast to other systems, the data is already there on chain, and the catalog would just reflect it. Probably the available metadata stored on chain and in `Move.toml` needs to be extended for this project, to describe aspects like package type, author, overview, etc.

**What we are looking for**

A team which can independently plan and execute this project. There are likely extensions to be made to existing package metadata, and AIPs will need to be proposed and changes made to [aptos-core](https://github.com/aptos/aptos-core). Experience working with existing package catalogues, like [crates.io](http://crates.io) is a good starting point. Background in building web applications is highly desired.

**Deliverables** 

A DApp providing a web view of the catalog of available packages on a network:

- Type, author, other relevant metadata
- Documentation of the code
- Verification that source code matches bytecode
- Usage of the package (usage in dependencies)
- etc.

**Grant amount** 

Initially 3 person months, with the option to extend the project.
