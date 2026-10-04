# MAT-apps — holding map (law for agents)

Four homes only. Do not create a fifth app. Do not invent folders off this map.

| Folder | Institutional role | Job | Never |
|--------|-------------------|-----|-------|
| **QSConnect** | Market data / pricing | Provider → clean → SQLite (`pull`, `last`, `quote`, `assess`) | Orders, notes, sizing, a CLI |
| **QSResearch** | Strategy / trade generation | Signal paste → `Intent`; allocation weights | Broker send, a CLI |
| **Omega** | OMS + pre-trade risk + execution | `Order` → GateChain → books → `ExecutionClient` | Market ingest, journals, a CLI |
| **QSWorkflow** | Front-office console + audit | `python -m qs`; MAP, STORE, journal, reference | Strategy math, provider HTTP, venue SDKs |

Python packages: `marketdata`, `strategy`, `omega`, `qs` (inside the QS* folders — not a second `QSResearch/` tree).

One door: `python -m qs <verb>`. Libraries have no `cli.py`.

Layer 0: `qs day|market|signal|check|fill|portfolio`. Layer 1 (owner): `qs go`.  
Kill switch: `QSWorkflow/HALT` or `QS_HALT=1` → `KILL_001`.

**Session journal** (live desk notes only): `QSWorkflow/journal/{day,levels,risk}/`.  
**Reference** (procedures, playbooks, static docs): `QSWorkflow/reference/`. Not session journal.

Install: venv in `QSWorkflow`, `pip install -e ../QSConnect -e ../QSResearch -e ../Omega -e .`  
Build junk (`*.egg-info/`, `__pycache__/`, `.pytest_cache/`) is gitignored — pip recreates `*.egg-info` on editable install; delete anytime.
