## Pump.fun smart contract clone
This pumpfun smart contract forked pump.fun, but it's developed to give basic understanding about pump fun. 
To get whole part of smart contract and backend & frontend, feel free to reach out of me[Telegram: https://t.me/Oxundying]
You can also get frontend and backend repository from my github.


## Project structure

```text
.
├── .gitignore
├── .prettierignore
├── Anchor.toml                 # Anchor program IDs, cluster, wallet, test script
├── Cargo.toml                  # Rust workspace (members: programs/*)
├── Cargo.lock
├── package.json                # Node scripts / ts-mocha tests
├── tsconfig.json               # TypeScript config for CLI + tests
├── programs/
│   └── pump/                   # On-chain Anchor program (curve / pool logic)
│       ├── Cargo.toml
│       ├── Xargo.toml          # BPF build profile helpers
│       └── src/
│           ├── lib.rs          # Program entry + instruction dispatch
│           ├── consts.rs       # Constants (fees, limits, decimals)
│           ├── errors.rs       # Custom program errors
│           ├── state.rs        # Curve configuration + liquidity accounts
│           ├── instructions/   # initialize, add/remove liquidity, swap
│           └── utils/          # Math helpers (e.g. bonding curve calculations)
├── cli/                        # TypeScript Anchor client stubs (IDL-derived types)
│   ├── programId.ts
│   ├── accounts/               # Account decoders / builders
│   ├── instructions/           # Instruction encoders used by scripts/tests
│   └── errors/
├── migrations/
│   └── deploy.ts               # Deploy helper migration
└── tests/
    └── pump.ts                 # Anchor integration tests (mocha/ts)
```

- **`programs/pump`** — Rust smart contract implementing initialization, liquidity, and swaps around the bonding-curve-style pool.
- **`cli`** — TypeScript wrappers for invoking the program and serializing accounts/instructions during development and automated tests.
- **`migrations`** — Deployment scaffolding for the Anchor program.
- **`tests`** — End-to-end or instruction-level tests hitting a local ledger or configured cluster.


## Core Functionalities
1. Initialization [Admin wallet setting, Buy/Sell/Migration fee setting, Curve limit set]
2. Pool creation [Token creation, new liquidity]
3. Buy/Sell 
4. Migration after bonding curve complete


### Contact Information
- Telegram: https://t.me/Oxundying
