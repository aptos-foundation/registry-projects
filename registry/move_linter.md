**Project Information**

- Title: Move Linter
- Vertical: Move 
- Labs POC: Move Language Team (wg@aptoslabs.com)

**Motivation**

A linter analyzes code for idiomatic usage and potential issues which go beyond the basic language rules. Linting is often integral part of the development process, and successfully passing the linter a requirement for merging code. The Move ecosystem would benefit having a powerful linter with potential emphasis on security. 

**Design Notes**

The linter should be extensible, so it can easily be extended with new rules of language usage, as those evolve. Moreover, the linter should be capable to not only mark incorrect usage, but also provide suggestions how to change the code. The goal is that the linter also becomes an educational tool for Move usage.


**What we are looking for**

An individual or team which is acquainted with compiler context checking technology, and can plan and execute this project independently.

**Deliverables**

- An [AIP](http://github.com/aptos-foundation/aips) describing the tool
- A tool which can lint a Move package
- Integration of the tool into `aptos-core` repo and Move CLI, documentation

**Grant amount**

Initial grant of 3 person months, with potential for extension
