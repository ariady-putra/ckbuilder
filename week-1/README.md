# Builder Track Weekly Report - Week 1

- **Name:** Ariady Putra
- **Submitted On:** 30-Nov-2026

## Milestones

1. Read ["How CKB Works"](https://docs.nervos.org/docs/getting-started/how-ckb-works)
   - key learnings: [here](./NOTES.md)

2. Setup [Local DevNet](https://docs.nervos.org/docs/getting-started/quick-start)
   - installed [offCKB CLI](https://www.npmjs.com/package/@offckb/cli)
     <img src="https://github.com/user-attachments/assets/a2baf69d-b300-40e6-94f4-ce533c687814" />

   - created and deployed the [`hello-world`](https://docs.nervos.org/docs/sdk-and-devtool/offckb#create-a-contract-project) contract to the local devnet
     <img src="https://github.com/user-attachments/assets/c4f1157f-66c5-42f4-b7cf-76f9612b68e1" />

   - ran the test script
     <img src="https://github.com/user-attachments/assets/1bed99f5-9e4d-4463-82cd-911e651c208a" />

3. TODO: Finish both [CKB Academy lessons 1 and 2](https://academy.ckb.dev/courses)
   - read ["A Common Knowledge Base for Crypto-Economy"](https://github.com/nervosnetwork/rfcs/blob/master/rfcs/0002-ckb/0002-ckb.md)
   - read ["Consensus RFC"](https://github.com/nirenzang/rfcs/blob/master/rfcs/0020-ckb-consensus-protocol/0020-ckb-consensus-protocol.md)

## Blockers

1. I faced an error when building the `hello-world` contract project initially.
   - the error: [here](./blockers/1.md)

## Solutions

1. Make sure local devnet is running. And since I'm using `pnpm`, set `allowBuilds.esbuild` to `true` in [`pnpm-workspace.yaml`](./hello-world/pnpm-workspace.yaml), delete the `node_modules` directory, re-run `pnpm` install and build. And then finally, the contract should be able to be deployed and tested.

## Tangential Topics

### RISC-V

I've heard of the term "RISC-V" in the past but I've never looked for what's the deal with it, so I decided to learn more about RISC-V.

- watched a [non-technical RISC-V explainer video](https://www.youtube.com/watch?v=Ps0JFsyX2fU)

  The video shows some practical real-world applications of RISC-V in general.

- watched ["why RISC-V matters" video](https://www.youtube.com/watch?v=4TmHSsIU1ns)

  The video briefly touches on the difference between ARM's RISC and RISC-V, and highlights the importance of RISC-V's open standard as well as its global implications due to the geopolitical climate in the world.
