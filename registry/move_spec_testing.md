**Project Information**

- Title: Move Specification Testing
- Vertical: Move 
- Labs POC: Move Language Team (wg@aptoslabs.com)

**Motivation** 

Formal specifications in Move can be incomplete, since predicates over inputs and outputs of functions, as well invariants over the global state, are only constraints. For example, a predicate `x > 0` does not specify a particular value for `x`, but just constraints it. Having a tool _to test the completeness_ of Move specifications is therefore an important part of practical use of formal verification in Move

**Design Notes**

There is no standard solution for specification testing. However, [mutation testing](https://en.wikipedia.org/wiki/Mutation_testing) has been investigated at Meta for Move specifications before. In this usage, the code is mutated and the specification is expected to catch the mutation. From a set of systematically generated mutations and the rate how they are caught by the spec, a coverage metric can be derived. This work was not finished at Meta. In the meantime, the Certora verifier for Solidity specs took up a similar idea in their [Gambit tool](https://docs.certora.com/en/latest/docs/gambit/index.html). Notice that Gambit, though originally intended for specification testing, can also be applied for testing completeness of regular test suites.

**What we are looking for**

An individual or team which is acquainted with testing technology, as well as formal verification and compilers,  and can plan and execute this project independently. 

**Deliverables** 

- An [AIP](http://github.com/aptos-foundation/aips) describing the tool
- A mutation testing tool for Move, applied to testing completeness of Move specifications.
- Integration of the tool into `aptos-core` repo and Move CLI, documentation

**Grant amount** 

Initial grant of 3 person months, with potential for extension
