# CKB

CKB, an **L1 blockchain** (also referred to as Nervos), is a blockchain that prioritizes [security and decentralization](https://docs.nervos.org/docs/ckb-fundamentals/nervos-blockchain#multi-layer-architecture). [Multiple instances of CKB-VM can execute different smart contracts concurrently](https://docs.nervos.org/docs/ckb-fundamentals/nervos-blockchain#programming-on-nervos), which enables substantial scaling improvements. [Nervos uses NC-MAX (a PoW-based consensus algorithm)](https://docs.nervos.org/docs/ckb-fundamentals/nervos-blockchain#consensus), it splits transactions confirmation process into 2 steps: **propose** & **commit** ([thereby allowing transactions to be fully propagated before being committed](https://docs.nervos.org/docs/ckb-fundamentals/consensus#improved-block-propagation)). The hashing function used by Nervos is [Eaglesong](https://docs.nervos.org/docs/ckb-fundamentals/consensus#eaglesong-hash-function) (it's [32-byte BLAKE2b](https://docs.nervos.org/docs/ckb-fundamentals/ckbhash)).

## Cell Model

The CKB blockchain adopts the **Cell Model**. If you're familiar with Bitcoin, it's essentially the UTxO Model but with extended features to store data and some scripts. An Unspent Output is called a **Live Cell**, and a Spent Output is called a **Dead Cell**. A [Cell](https://docs.nervos.org/docs/tech-explanation/cell) is the smallest and fundamental unit in Nervos CKB, used for storing states. Its structure is as follows:

```
Cell: {
  capacity: HexString; // shannon
  lock: Script; // who can spend the UTxO
  type: Script; // how to spend the UTxO (optional)
  data: HexString; // bytes
}
```

CKB does not run scripts one by one. It first groups the inputs or outputs by script and runs the same script only once (source: [Role of the type script](https://academy.ckb.dev/courses/basic-theory)).

## CKByte

The term "CKB" may also refer to **CKByte**, it is the native token of Nervos.

- 1 CKB = 1 byte data storage on Nervos
- 100-million shannons = 1 CKB

CKByte is used as the fee currency for:

- **Cycles** (computation)
- **Tx Fees** (security)
- **State Rent** (storage - min CKB per UTxO)

**Cycles** compensate miners based on the computational resources used to verify a transaction as measured by CKB-VM.

There is no limit on the cycles for an individual transaction or script, BUT [it is limited by `max_block_cycles`](https://docs.nervos.org/docs/getting-started/how-ckb-works#cycles) (on CKB Mainnet `MIRANA`, it's `3,500,000,000`).

**Tx Fees** are paid to miners for providing the computing power.

**State Rent** compensates miners for providing storage space.

There must be at least 61 CKB per Cell, recommended: at least 62 CKB (sources: https://docs.nervos.org/docs/getting-started/how-ckb-works#how-transaction-works, https://docs.nervos.org/docs/tech-explanation/capacity#capacity-mini).

## CKB Address

An example of a [CKB address](https://docs.nervos.org/docs/ckb-fundamentals/ckb-address):

```
ckb1qzda0cr08m85hc8jlnfp3zer7xulejywt49kt2rr0vthywaa50xwsqdnnw7qkdnnclfkg59uzn8umtfd2kwxceqxwquc4
```

Components:

- Human-readable part: `ckb` for mainnet, `ckt` for testnet
- Separator: always `1`
- Data part: base32 encoded
- Checksum: the last 6 characters

## Consensus

As mentioned earlier, Nervos uses NC-MAX (a PoW-based consensus algorithm). Every node can participate in the consensus process either [by mining to produce new blocks, or by verifying new blocks are valid](https://github.com/nervosnetwork/rfcs/blob/master/rfcs/0002-ckb/0002-ckb.md#3-consensus).

Differences between NC-MAX and Bitcoin's Nakamoto Consensus:

- NC-MAX decouples transactions confirmation into 2 steps (**propose** & **commit**) to eliminate bottleneck in block propagation
- NC-MAX dynamically adjusts the block interval, increasing throughput when network latency improves
- NC-MAX makes selfish mining unprofitable regardless of how the attacker divides its mining power among honest mining, selfish mining and idle, and how many epochs the attack involves

(source: https://github.com/nirenzang/rfcs/blob/master/rfcs/0020-ckb-consensus-protocol/0020-ckb-consensus-protocol.md#technical-overview)

## Nervos DAO

CKB holders may stake their tokens in [Nervos DAO](https://docs.nervos.org/docs/assets-token-standards/economics#nervos-dao). CKB locked in Cells (state rent) [cannot be placed in Nervos DAO](https://docs.nervos.org/docs/assets-token-standards/economics#state-rent).
