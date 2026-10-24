<div align="center">
  <img src="assets/banner.svg" width="100%" alt="Salman Chhatwal — systems, agents, settlement rails" />
</div>

<br />

Full-stack and AI/ML engineer. Most of what I build sits under agents rather than inside them: settlement rails, permission layers, adjudication, the machinery that has to hold when nobody is watching.

I work upstream too. 374 pull requests to Nous Research's Hermes Agent and its plugin repos — TUI, gateway, tool layer, desktop runtimes, state stores, adapters.

<br />

<div align="center"><img src="assets/rule.svg" width="100%" alt="" /></div>

<br />

<div align="center"><img src="assets/sec-01.svg" width="100%" alt="01 — Now" /></div>

<br />

| Working on | Role | State |
| --- | --- | --- |
| **PayMate** — non-custodial USDC billing rail for agents | author | live on GOAT mainnet |
| **MediVault** — private AI health vault on 0G | author | live, ERC-7857 contract on mainnet |
| **Hermes Agent** — agent runtime and plugin catalog | upstream contributor | 374 PRs open |
| **GenLayer adjudication** — evidence-first verdict contracts | author | 3 protocols shipped |

<br />

<div align="center"><img src="assets/sec-02.svg" width="100%" alt="02 — Hermes Agent" /></div>

<br />

<div align="center">
  <img src="assets/stats.svg" width="100%" alt="374 upstream PRs, 68 merged, 12 shipped products, 25 stars" />
</div>

<br />

Hermes is the agent that grows with you — a real agent runtime with desktop apps, gateways, channels, sandboxes, memory and a plugin catalog. I spend my time in the failure modes: a gateway that won't release a stale PID, a Windows profile path with non-ASCII characters, a WAL generation unlinked by a short-lived reader, an OAuth login that a single refresh can revive.

Shipped upstream:

| PR | What it fixes |
| --- | --- |
| [`hermes-agent#140922`](https://github.com/NousResearch/hermes-agent/pull/140922) | gateway: stamps an unproven `--replace` refusal as `startup_failed` so the next start wins |
| [`hermes-official-plugins#61`](https://github.com/NousResearch/hermes-official-plugins/pull/61) | directsdk: carries the login identity into the child env, captures native stderr |
| [`hermes-labs-plugins#3`](https://github.com/NousResearch/hermes-labs-plugins/pull/3) | record: an `autocomplete` token inside a list is still a secret field |

Open and in review: [gateway restart paths](https://github.com/NousResearch/hermes-agent/pull/142501) · [stale heartbeat requeues](https://github.com/NousResearch/hermes-agent/pull/142275) · [execute_code kernel memory caps](https://github.com/NousResearch/hermes-agent/pull/142249) · [wedged `check_fn` probes](https://github.com/NousResearch/hermes-agent/pull/142062) · [bounded inbound media download](https://github.com/NousResearch/hermes-official-plugins/pull/153) · [local-time timestamps in Home Assistant](https://github.com/NousResearch/hermes-official-plugins/pull/160).

**Surfaces touched:** TUI · gateway lifecycle · tool execution and output spilling · cron and heartbeats · desktop (Windows/macOS) · MCP · ACP · SQLite state and WAL · compression and checkpointing · installers · Discord / WhatsApp / xchat adapters · DirectSDK · Spotify · Home Assistant.

Also authored 10 Hermes skills published as standalone repos — [daily briefing](https://github.com/salch-cred/hermes-daily-briefing), [release radar](https://github.com/salch-cred/hermes-release-radar), [disk guard](https://github.com/salch-cred/hermes-disk-guard), [IP watchdog](https://github.com/salch-cred/hermes-ip-watchdog), [uptime digest](https://github.com/salch-cred/hermes-uptime-digest), [cert expiry](https://github.com/salch-cred/hermes-cert-expiry), [price digest](https://github.com/salch-cred/hermes-price-digest), [battery](https://github.com/salch-cred/hermes-battery), [dead link](https://github.com/salch-cred/hermes-dead-link), [folder size](https://github.com/salch-cred/hermes-folder-size).

<br />

<div align="center"><img src="assets/sec-03.svg" width="100%" alt="03 — Selected work" /></div>

<br />

<p align="center">
  <a href="https://github.com/salch-cred/medivault"><img src="assets/card-01.svg" width="47%" alt="MediVault" /></a>
  &nbsp;
  <a href="https://github.com/salch-cred/AgentPassport"><img src="assets/card-02.svg" width="47%" alt="AgentPassport" /></a>
</p>
<p align="center">
  <a href="https://github.com/salch-cred/provenode"><img src="assets/card-03.svg" width="47%" alt="ProvenNode" /></a>
  &nbsp;
  <a href="https://github.com/salch-cred/PolicyCourt"><img src="assets/card-04.svg" width="47%" alt="PolicyCourt" /></a>
</p>
<p align="center">
  <a href="https://github.com/salch-cred/veritas-genlayer"><img src="assets/card-05.svg" width="47%" alt="Veritas" /></a>
  &nbsp;
  <a href="https://github.com/salch-cred/aerosure-genlayer"><img src="assets/card-06.svg" width="47%" alt="AeroSure" /></a>
</p>
<p align="center">
  <a href="https://github.com/salch-cred/hydrasentinel"><img src="assets/card-07.svg" width="47%" alt="HydraSentinel" /></a>
  &nbsp;
  <a href="https://github.com/salch-cred/-Permitly"><img src="assets/card-08.svg" width="47%" alt="Permitly" /></a>
</p>
<p align="center">
  <a href="https://github.com/salch-cred/wefspan"><img src="assets/card-09.svg" width="47%" alt="wefspan" /></a>
  &nbsp;
  <a href="https://github.com/salch-cred/moovegate"><img src="assets/card-10.svg" width="47%" alt="MooveGate" /></a>
</p>
<p align="center">
  <a href="https://github.com/salch-cred/skillmint"><img src="assets/card-11.svg" width="47%" alt="SkillMint" /></a>
  &nbsp;
  <a href="https://github.com/salch-cred/RialoScan"><img src="assets/card-12.svg" width="47%" alt="RialoScan" /></a>
</p>

<br />

**Also shipped:** [JanFix](https://github.com/salch-cred/janfix) (civic reporting, zero login, ward routing) · [Monaco CLOB dashboard](https://github.com/salch-cred/monaco-clob-dashboard) (Sei order book) · [SnakeCase](https://github.com/salch-cred/snakecase) (34-lesson Python curriculum) · [ZeroSense](https://github.com/salch-cred/zero-sense) (ZK robot proofs + Stellar micropayments) · [Reso](https://github.com/salch-cred/reso) (ZK compliance engine) · [Atropos tooling](https://github.com/salch-cred/atropos).

<br />

<div align="center"><img src="assets/sec-04.svg" width="100%" alt="04 — PayMate" /></div>

<br />

### The billing rail for the agent economy

Agents can chat, code and research. They cannot collect money. Invoices are PDFs, chasing is manual, and nothing exists for a per-call micropayment. Freelancers, meanwhile, have no portable proof that they finished anything.

[PayMate](https://github.com/salch-cred/paymate-new-) closes both sides: a freelancer or an agent creates an invoice or a paywalled endpoint, the client settles in **real USDC directly to the freelancer's wallet**, and every settlement mints a portable on-chain reputation credential. No custody of principal, no API-key gatekeeping.

**Live:** [paymateagent.xyz](https://www.paymateagent.xyz) · **Docs:** [paymateagent.xyz/docs](https://www.paymateagent.xyz/docs) · **Developers:** [paymateagent.xyz/developers](https://www.paymateagent.xyz/developers)

| Piece | Mechanism |
| --- | --- |
| Settlement | USDC on GOAT mainnet (chain 2345), client → freelancer wallet, verified on-chain |
| Agent billing | `POST /api/agent-billing` mints per-call x402 challenges; replay-guarded unlock |
| Reputation | ERC-8004 soulbound credential per settlement — travels with the agent |
| Escrow | `YieldEscrow` locks funds; PR merge or AI verdict releases them |
| Disputes | Mistral arbitrator rules against the original scope: pay / refund / split |
| Cross-chain | client signs one tx on any of 39 networks; relayer converts and settles in USDC |
| Zero-custody rail | swap → approve → bridge, DOGEB lands straight in the freelancer's wallet |
| Self-refill | BSC deposits pivot, bridge and DEX-swap into the payout pool automatically |
| Operator agent | audits the ledger, checks liquidity runway, retries failed swaps under hard USD caps |

Deployed and verifiable — `YieldEscrow` `0xEbe3BE16d7fd69268BcADdB6DB25C60dFff302e0`, `PayMateReputation` `0x48B9B6BB1C4Eb4b6911D05dfd3E87F8be8a67603`, `PayMateTreasury` `0x59C4c64DF838f23b8dA77A95c18BC3520D71e25B` on GOAT mainnet. Settlement counts, fee take and every hop are on the public [growth](https://www.paymateagent.xyz/growth) and [treasury](https://www.paymateagent.xyz/treasury) pages — read from the API, not asserted in a deck.

The part I actually care about: nothing moves on trust. Bridge and DEX paths ship **fail-closed** behind verification flags until a real-money probe passes, the relayer's ledger is idempotent, and the AI operator can prioritise but never exceed a code-enforced cap.

<br />

<div align="center"><img src="assets/sec-05.svg" width="100%" alt="05 — Research systems" /></div>

<br />

Smaller, stranger builds where the constraint is the point — every one of them a working repo, not a notebook:

[quantum-entangled-transformer](https://github.com/salch-cred/quantum-entangled-transformer) (attention heads as entangled states) · [cellular-automata-transformer](https://github.com/salch-cred/cellular-automata-transformer) · [superconducting-super-computation](https://github.com/salch-cred/superconducting-super-computation) (Josephson-junction SNN simulator) · [seismic-anomaly-detection-snn](https://github.com/salch-cred/seismic-anomaly-detection-snn) · [spiking-weather-net](https://github.com/salch-cred/spiking-weather-net) · [topological-data-homology-nets](https://github.com/salch-cred/topological-data-homology-nets) · [thermodynamic-neural-annealing](https://github.com/salch-cred/thermodynamic-neural-annealing) · [viscous-fluid-neural-flow](https://github.com/salch-cred/viscous-fluid-neural-flow) · [swarm-drug-molecule-designer](https://github.com/salch-cred/swarm-drug-molecule-designer) · [symbiotic-multi-agent-rlaif](https://github.com/salch-cred/symbiotic-multi-agent-rlaif).

<br />

<div align="center"><img src="assets/sec-06.svg" width="100%" alt="06 — Stack and contact" /></div>

<br />

| | |
| --- | --- |
| **Languages** | TypeScript · Python · Solidity · Move · SQL |
| **Agents** | tool-calling runtimes · MCP · x402 · RAG with cited evidence · evaluation harnesses |
| **Infra** | Next.js · FastAPI · Postgres · Redis · Docker · CI/CD · observability |
| **Chains** | GOAT · 0G · GenLayer · Aptos/Shelby · Stellar · EVM |
| **ML** | PyTorch · scikit-learn · pandas · diffing and evidence pipelines |

<br />

Open to work on agent infrastructure, settlement and adjudication, and hard reliability problems in long-running systems.

**`salmanch98@gmail.com`** · [X](https://twitter.com/salmanch_) · [LinkedIn](https://www.linkedin.com/in/salman-chhatwal-70339227a/)
