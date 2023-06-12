**Project Information**

- Title: Move Formatter 
- Vertical: Move 
- Labs POC: Move Language Team (wg@aptoslabs.com)

**Motivation**

In modern development workflows, autoformatting of source code is a standard part of the process. For example, coding standards for languages like Rust or C++ require the code to be in a canonical format, as checked by a formatter, before it can be merged into the git repo. Tools are therefore offered to establish this format, e.g. `cargo fmt`. 

We like to have a similar tool for Move, which generates a canonical format for Move code, which can be used in similar ways as e.g. `cargo fmt`. 

**Design Notes**

A challenge with autoformatting is how to properly deal with comments. Since comments are not part of the grammar (but are dropped in lexical processing already), the Move parser is not the right thing to involve here. A proper solution should include analysis of how other languages have dealt with this problem.

**What we are looking for**

An individual or team which is acquainted with compiler and/or autoformatting of source code, and can plan and execute this project independently.

**Deliverables**

- An [AIP](http://github.com/aptos-foundation/aips) describing the tool
- A tool which can autoformat a Move source file
- Integration of the tool into `aptos-core` repo and Move CLI, documentation

**Grant amount**

3 person months
