# ckbuilder

A Builder Track repository documenting Ariady Putra's weekly progress learning and developing on the Nervos CKB blockchain.

## Contents

- [`week-1/`](./week-1/) — Week 1 report, CKB fundamentals, a local DevNet setup, and a `hello-world` smart contract project.
  - [`NOTES.md`](./week-1/NOTES.md) — Notes on CKB, the Cell model, CKByte, addresses, and Nervos DAO.
  - [`hello-world/`](./week-1/hello-world/) — CKB JavaScript smart contract project.
  - [`blockers/`](./week-1/blockers/) — Development issues and troubleshooting notes.

## Technologies

- JavaScript
- TypeScript
- CKB JavaScript VM
- pnpm
- Jest
- esbuild

## Getting Started

The first project is in [`week-1/hello-world`](./week-1/hello-world). It requires Node.js 20 or later, pnpm, and a running CKB local DevNet.

```bash
cd week-1/hello-world
pnpm install
pnpm run build
pnpm test
pnpm run deploy
```

See the [project README](./week-1/hello-world/README.md) for detailed build, test, add-contract, and deployment instructions.

## Reports

- [Week 1 Report](./week-1/README.md)

## License

No license has been specified for this repository.
