# Builder Track Weekly Report - Week 1

- **Name:** Ariady Putra
- **Submitted On:** 30-Nov-2026

## Milestones

1. Read ["How CKB Works"](https://docs.nervos.org/docs/getting-started/how-ckb-works)
   - key learnings: [here](./NOTES.md)
2. Setup [Local DevNet](https://docs.nervos.org/docs/getting-started/quick-start)
   - installed [offCKB CLI](https://www.npmjs.com/package/@offckb/cli)
   - created and deployed the [`hello-world`](https://docs.nervos.org/docs/sdk-and-devtool/offckb#create-a-contract-project) contract to the local devnet
   - ran the test script
3. TODO: Finish both [CKB Academy lessons 1 and 2](https://academy.ckb.dev/courses)

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
