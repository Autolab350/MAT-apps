# MAT-apps — paper equity & options desk

Python libraries for a small **stock / options** desk: pull market data, turn a signal into an intent, run pre-trade risk checks, paper-fill, and keep an audit trail. One operator door: `python -m qs`. **Paper only** in this public tree — no live broker keys, no session journals.

This is Phase A of a broader markets stack. Later work can hang a crypto markets UI (charts, perps, prediction books) on the same desk ideas — risk gates, kill switch, human confirm before send. That UI stays private for now; MAT here is the equity/options library and console.

| Repo | Role |
|------|------|
| [QSConnect](https://github.com/Autolab350/QSConnect) | Market data (`marketdata`) |
| [QSResearch](https://github.com/Autolab350/QSResearch) | Signal → `Intent` (`strategy`) |
| [Omega](https://github.com/Autolab350/Omega) | Orders, GateChain risk, paper execution |
| [QSWorkflow](https://github.com/Autolab350/QSWorkflow) | `python -m qs` console + STORE |

Clone the four repos next to each other, then follow [QSWorkflow/README.md](https://github.com/Autolab350/QSWorkflow/blob/main/README.md).

Layout law for agents: [MAP.md](./MAP.md).
