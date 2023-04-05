# huff-puzzles by [RareSkills](https://www.rareskills.io)

A series of puzzles that go from very easy to more difficult so that you can have a hands-on introduction to the [huff language](https://huff.sh) and learn EVM bytecode while doing it.

## Solved exercises

1) [x] [CallValue](/src/CallValue.huff)
2) [x] [CalldataLength](/src/CalldataLength.huff)
3) [x] [MyEtherBalance](/src/MyEtherBalance.huff)
4) [x] [Add1](/src/Add1.huff)
5) [x] [Multiply](/src/Multiply.huff)
6) [x] [NonPayable](/src/NonPayable.huff)
7) [x] [FooBar](/src/FooBar.huff)
8) [x] [SimpleStore](/src/SimpleStore.huff)
9) [x] [RevertCustom](/src/RevertCustom.huff)
10) [x] [RevertString](/src/RevertString.huff)
11) [x] [SumArray](/src/SumArray.huff)
12) [x] [Keccak](/src/Keccak.huff)
13) [x] [MaxOfArray](/src/MaxOfArray.huff)
14) [x] [Donations](/src/Donations.huff)
15) [x] [BasicBank](/src/BasicBank.huff)
16) [x] [SimulateArray](/src/SimulateArray.huff)
17) [x] [Emitter](/src/Emitter.huff)
18) [x] [Create](/src/Create.huff)
19) [x] [SendEther](/src/SendEther.huff)
20) [x] [Distribute](/src/Distributor.huff)


## Pre-requisites

Make sure you've installed the Huff Compiler as outlined in the [Huff Docs](https://docs.huff.sh/get-started/installing/#installing-huff).

TLDR:

    curl -L get.huff.sh | bash

then:

     huffup

To verify your installation, run `huffc --help`. This should print a list of available commands for the huff compiler cli.

## Installation

To install dependencies, run:

    forge install

## How to play

Go to [Return1.huff](https://github.com/rareskills/huff-puzzles/blob/main/src/Return1.huff) in the src folder and edit it as follows

```c
#define macro MAIN() = takes(0) returns(0) {
    // store 1 in memory at offset 0
    0x01            // [1]
    0x00            // [0, 1]
    mstore          // []

    // return 1
    // return 32 bytes of memory starting at offset 0
    0x20            // [32]
    0x00            // [0, 32]
    return          // []
}
```

Then run the test with

    forge test -vvv --mc Return1Test

You should see something like this

    Running 1 test for test/Return1.t.sol:Return1Test
    [PASS] testReturn1() (gas: 5358)
    Test result: ok. 1 passed; 0 failed; finished in 4.56s

## Suggested order for other exercises

- [CallValue](https://github.com/rareskills/huff-puzzles/blob/main/src/CallValue.huff)
- [CalldataLength](https://github.com/rareskills/huff-puzzles/blob/main/src/CalldataLength.huff)
- [MyEtherBalance](https://github.com/rareskills/huff-puzzles/blob/main/src/MyEtherBalance.huff)
- [Add1](https://github.com/rareskills/huff-puzzles/blob/main/src/Add1.huff)
- [Multiply](https://github.com/rareskills/huff-puzzles/blob/main/src/Multiply.huff)
- [NonPayable](https://github.com/rareskills/huff-puzzles/blob/main/src/NonPayable.huff)
- [FooBar](https://github.com/rareskills/huff-puzzles/blob/main/src/FooBar.huff)
- [SimpleStore](https://github.com/rareskills/huff-puzzles/blob/main/src/SimpleStore.huff)
- [RevertCustom](https://github.com/rareskills/huff-puzzles/blob/main/src/RevertCustom.huff)
- [RevertString](https://github.com/rareskills/huff-puzzles/blob/main/src/RevertString.huff)
- [SumArray](https://github.com/rareskills/huff-puzzles/blob/main/src/SumArray.huff)
- [Keccak](https://github.com/rareskills/huff-puzzles/blob/main/src/Keccak.huff)
- [MaxOfArray](https://github.com/rareskills/huff-puzzles/blob/main/src/MaxOfArray.huff)
- [Donations](https://github.com/rareskills/huff-puzzles/blob/main/src/Donations.huff)
- [BasicBank](https://github.com/rareskills/huff-puzzles/blob/main/src/BasicBank.huff)
- [SimulateArray](https://github.com/rareskills/huff-puzzles/blob/main/src/SimulateArray.huff)
- [Emitter](https://github.com/rareskills/huff-puzzles/blob/main/src/Emitter.huff)
- [Create](https://github.com/rareskills/huff-puzzles/blob/main/src/Create.huff)
- [SendEther](https://github.com/rareskills/huff-puzzles/blob/main/src/SendEther.huff)
- [Distribute](https://github.com/rareskills/huff-puzzles/blob/main/src/Distribute.huff)

## More resources

- [Huff Documentation 🐴](https://docs.huff.sh/)
- [Evm codes](https://evm.codes)
- [Huffmate](https://github.com/pentagon-xyz/huffmate)
- [Huff Console.log](https://github.com/AmadiMichael/Huff-Console)

## Contributors

- [Michael Amadi](https://github.com/AmadiMichael)
- [Jesse Raymond](https://github.com/jesserc)
