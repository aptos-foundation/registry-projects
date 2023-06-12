**Project Information**

- Title: Move Decompiler 
- Vertical: Move 
- Labs POC: Move Language Team (wg@aptoslabs.com)

**Motivation** 

Move bytecode is strongly typed and contains all information needed to generate Move source code from it. Being able to decompile Move bytecode as stored on chain into readable source code will highly contribute to security as it makes transparent what code is executed. 

There is the concern that a Move decompiler disallows to keep intellectual property in Move code concealed. However, it is an illusion that Move code can be private. If the community doesn't provide a tool like a decompiler, actual thefts will easily build substitutes. It is better to have a common solution for this, levelling the field.

**Design Notes**

The biggest technical challenge of the decompiler is to reconstruct control flow constructs like loops and conditionals from the branching bytecode. However, this is a problem solved e.g. for LLVM backends (e.g. WASM and JS backends), and the solutions can be adapted for Move.

**What we are looking for**

An individual or team which is acquainted with compiler technology, and can plan and execute this project independently. 

**Deliverables** 

- An [AIP](http://github.com/aptos-foundation/aips) describing the tool
- A tool which can decompile a Move bytecode module into a valid Move source code module
- Integration of the tool into `aptos-core` repo and Move CLI, documentation

**Grant amount**

3 person months
