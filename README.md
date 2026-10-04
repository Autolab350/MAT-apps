# MAT-apps — QS desk stack

Personal trading **desk OS**: market data → strategy (Intent) → pre-trade gates → paper execution → audit log. Not a broker, not live trading in this repo — paper only through `qs go`.

| Repo | Role |
|------|------|
| [QSConnect](https://github.com/Autolab350/QSConnect) | Market data (`marketdata` package) |
| [QSResearch](https://github.com/Autolab350/QSResearch) | Signal → `Intent` (`strategy` package) |
| [Omega](https://github.com/Autolab350/Omega) | `Order`, GateChain, paper `ExecutionClient` |
| [QSWorkflow](https://github.com/Autolab350/QSWorkflow) | Operator door: `python -m qs` |

Clone all four into one folder, then install from [QSWorkflow/README.md](https://github.com/Autolab350/QSWorkflow/blob/main/README.md).

Agent and path law: [MAP.md](./MAP.md).
