<div align="center">
  <img src="assets/banner.svg" width="100%" alt="Salman Chhatwal â€” systems, agents, settlement rails" />
</div>

<br />

Full-stack and AI/ML engineer. Most of what I build sits under agents rather than inside them: settlement rails, permission layers, adjudication, the machinery that has to hold when nobody is watching.

I work upstream too. 374 pull requests and 58 commits to Nous Research's Hermes Agent and its plugin repos â€” TUI, gateway, tool layer, desktop runtimes, state stores, adapters.

<br />

<div align="center"><img src="assets/rule.svg" width="100%" alt="" /></div>

<br />

<div align="center"><img src="assets/sec-01.svg" width="100%" alt="01 â€” Now" /></div>

<br />

| Working on | Role | State |
| --- | --- | --- |
| **PayMate** â€” non-custodial USDC billing rail for agents | author | live on GOAT mainnet |
| **MediVault** â€” private AI health vault on 0G | author | live, ERC-7857 contract on mainnet |
| **Hermes Agent** â€” agent runtime and plugin catalog | upstream contributor | 374 PRs · 58 commits |
| **GenLayer adjudication** â€” evidence-first verdict contracts | author | 3 protocols shipped |

<br />

<div align="center"><img src="assets/sec-02.svg" width="100%" alt="02 â€” Hermes Agent" /></div>

<br />

<div align="center">
  <img src="assets/stats.svg" width="100%" alt="374 upstream PRs, 58 commits authored, 3 merged, 10 skills published" />
</div>

<br />

Hermes is the agent that grows with you â€” a real agent runtime with desktop apps, gateways, channels, sandboxes, memory and a plugin catalog. I spend my time in the failure modes: a gateway that won't release a stale PID, a Windows profile path with non-ASCII characters, a WAL generation unlinked by a short-lived reader, an OAuth login that a single refresh can revive.

Shipped upstream:

| PR | What it fixes |
| --- | --- |
| [`hermes-agent#140922`](https://github.com/NousResearch/hermes-agent/pull/140922) | gateway: stamps an unproven `--replace` refusal as `startup_failed` so the next start wins |
| [`hermes-official-plugins#61`](https://github.com/NousResearch/hermes-official-plugins/pull/61) | directsdk: carries the login identity into the child env, captures native stderr |
| [`hermes-labs-plugins#3`](https://github.com/NousResearch/hermes-labs-plugins/pull/3) | record: an `autocomplete` token inside a list is still a secret field |

The patches themselves — 58 commits across 20+ topic branches:

| Commit | What it does |
| --- | --- |
| `fix(gateway): park a unit on unprovable --replace ownership instead of restart-looping` | stops a restart loop when ownership of a gateway unit can't be proven |
| `fix(gateway): rescue orphaned FIFO overflow when session goes idle (#99882)` | drains the FIFO a dead session leaves behind |
| `fix(gateway): log every missed liveness probe and dump the loop's task state` | makes a wedged loop diagnosable instead of silent |
| `fix(tools): bound a check_fn probe so a wedged availability check cannot hang the turn` | time-boxes tool availability probes |
| `fix(state): key display identity of tool rows on stable tool identity, not payload bytes (#117750)` | rows stop re-keying on every payload change |
| `fix(state): implement lazy flock single-writer gate to prevent WAL corruption` | single-writer gate over short-lived connections |
| `fix(desktop): assistant rows whose text persisted to sidecars no longer vanish on rehydrate (#68321)` | restores rows that rehydrated blank |
| `fix(discord): dispatch-side liveness dimension detects an ACKing-but-deaf gateway socket (#109521)` | catches a socket that ACKs but never delivers |
| `fix(agent): mirror Claude Code OAuth refresh into the macOS Keychain (#98334)` | keeps the refresh token where the OS expects it |
| `fix(checkpoints): drop oversize files from the index by literal pathspec` | oversized blobs no longer wedge the checkpoint index |
| `fix(backup): percent-encode path in _query_ro_sqlite URI` | backup paths with spaces resolve |
| `fix(cron): keep a sticky last_failure stamp so a healed run stays visible` | a healed cron run still shows it failed |
| `fix(whatsapp): adapter reads WHATSAPP_GROUP_ALLOWED_USERS for the group allowlist (#72529)` | group allowlist honours the documented env var |
| `fix(preview): use proper input events for React/contenteditable/submit in drive_preview type` | typing lands in React and contenteditable fields |

Open and in review: [gateway restart paths](https://github.com/NousResearch/hermes-agent/pull/142501) Â· [stale heartbeat requeues](https://github.com/NousResearch/hermes-agent/pull/142275) Â· [execute_code kernel memory caps](https://github.com/NousResearch/hermes-agent/pull/142249) Â· [wedged `check_fn` probes](https://github.com/NousResearch/hermes-agent/pull/142062) Â· [bounded inbound media download](https://github.com/NousResearch/hermes-official-plugins/pull/153) Â· [local-time timestamps in Home Assistant](https://github.com/NousResearch/hermes-official-plugins/pull/160).

**Surfaces touched:** TUI Â· gateway lifecycle Â· tool execution and output spilling Â· cron and heartbeats Â· desktop (Windows/macOS) Â· MCP Â· ACP Â· SQLite state, WAL, backups Â· compression and checkpointing Â· installers Â· Discord / WhatsApp / xchat adapters Â· DirectSDK Â· Spotify Â· Home Assistant.

Also authored 10 Hermes skills published as standalone repos â€” [daily briefing](https://github.com/salch-cred/hermes-daily-briefing), [release radar](https://github.com/salch-cred/hermes-release-radar), [disk guard](https://github.com/salch-cred/hermes-disk-guard), [IP watchdog](https://github.com/salch-cred/hermes-ip-watchdog), [uptime digest](https://github.com/salch-cred/hermes-uptime-digest), [cert expiry](https://github.com/salch-cred/hermes-cert-expiry), [price digest](https://github.com/salch-cred/hermes-price-digest), [battery](https://github.com/salch-cred/hermes-battery), [dead link](https://github.com/salch-cred/hermes-dead-link), [folder size](https://github.com/salch-cred/hermes-folder-size).

<br />

<div align="center"><img src="assets/sec-03.svg" width="100%" alt="03 â€” Selected work" /></div>

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

**Also shipped:** [JanFix](https://github.com/salch-cred/janfix) (civic reporting, zero login, ward routing) Â· [Monaco CLOB dashboard](https://github.com/salch-cred/monaco-clob-dashboard) (Sei order book) Â· [SnakeCase](https://github.com/salch-cred/snakecase) (34-lesson Python curriculum) Â· [ZeroSense](https://github.com/salch-cred/zero-sense) (ZK robot proofs + Stellar micropayments) Â· [Reso](https://github.com/salch-cred/reso) (ZK compliance engine) Â· [Atropos tooling](https://github.com/salch-cred/atropos).

<br />

<div align="center"><img src="assets/sec-04.svg" width="100%" alt="04 â€” PayMate" /></div>

<br />

### The billing rail for the agent economy

Agents can chat, code and research. They cannot collect money. Invoices are PDFs, chasing is manual, and nothing exists for a per-call micropayment. Freelancers, meanwhile, have no portable proof that they finished anything.

[PayMate](https://github.com/salch-cred/paymate-new-) closes both sides: a freelancer or an agent creates an invoice or a paywalled endpoint, the client settles in **real USDC directly to the freelancer's wallet**, and every settlement mints a portable on-chain reputation credential. No custody of principal, no API-key gatekeeping.

**Live:** [paymateagent.xyz](https://www.paymateagent.xyz) Â· **Docs:** [paymateagent.xyz/docs](https://www.paymateagent.xyz/docs) Â· **Developers:** [paymateagent.xyz/developers](https://www.paymateagent.xyz/developers)

| Piece | Mechanism |
| --- | --- |
| Settlement | USDC on GOAT mainnet (chain 2345), client â†’ freelancer wallet, verified on-chain |
| Agent billing | `POST /api/agent-billing` mints per-call x402 challenges; replay-guarded unlock |
| Reputation | ERC-8004 soulbound credential per settlement â€” travels with the agent |
| Escrow | `YieldEscrow` locks funds; PR merge or AI verdict releases them |
| Disputes | Mistral arbitrator rules against the original scope: pay / refund / split |
| Cross-chain | client signs one tx on any of 39 networks; relayer converts and settles in USDC |
| Zero-custody rail | swap â†’ approve â†’ bridge, DOGEB lands straight in the freelancer's wallet |
| Self-refill | BSC deposits pivot, bridge and DEX-swap into the payout pool automatically |
| Operator agent | audits the ledger, checks liquidity runway, retries failed swaps under hard USD caps |

Deployed and verifiable â€” `YieldEscrow` `0xEbe3BE16d7fd69268BcADdB6DB25C60dFff302e0`, `PayMateReputation` `0x48B9B6BB1C4Eb4b6911D05dfd3E87F8be8a67603`, `PayMateTreasury` `0x59C4c64DF838f23b8dA77A95c18BC3520D71e25B` on GOAT mainnet. Settlement counts, fee take and every hop are on the public [growth](https://www.paymateagent.xyz/growth) and [treasury](https://www.paymateagent.xyz/treasury) pages â€” read from the API, not asserted in a deck.

The part I actually care about: nothing moves on trust. Bridge and DEX paths ship **fail-closed** behind verification flags until a real-money probe passes, the relayer's ledger is idempotent, and the AI operator can prioritise but never exceed a code-enforced cap.

<br />

<div align="center"><img src="assets/sec-05.svg" width="100%" alt="05 â€” Research systems" /></div>

<br />

Smaller, stranger builds where the constraint is the point â€” every one of them a working repo, not a notebook:

[quantum-entangled-transformer](https://github.com/salch-cred/quantum-entangled-transformer) (attention heads as entangled states) Â· [cellular-automata-transformer](https://github.com/salch-cred/cellular-automata-transformer) Â· [superconducting-super-computation](https://github.com/salch-cred/superconducting-super-computation) (Josephson-junction SNN simulator) Â· [seismic-anomaly-detection-snn](https://github.com/salch-cred/seismic-anomaly-detection-snn) Â· [spiking-weather-net](https://github.com/salch-cred/spiking-weather-net) Â· [topological-data-homology-nets](https://github.com/salch-cred/topological-data-homology-nets) Â· [thermodynamic-neural-annealing](https://github.com/salch-cred/thermodynamic-neural-annealing) Â· [viscous-fluid-neural-flow](https://github.com/salch-cred/viscous-fluid-neural-flow) Â· [swarm-drug-molecule-designer](https://github.com/salch-cred/swarm-drug-molecule-designer) Â· [symbiotic-multi-agent-rlaif](https://github.com/salch-cred/symbiotic-multi-agent-rlaif).

<br />

<div align="center"><img src="assets/sec-06.svg" width="100%" alt="06 â€” Stack and contact" /></div>

<br />

Everything I actually work in, no padding.

<br />

<div align="center">
  <img src="assets/stack.svg" width="100%" alt="Stack: languages, frontend, backend, data, AI/ML, agents, chains, infra, testing and design" />
</div>

<br />

Open to work on agent infrastructure, settlement and adjudication, and hard reliability problems in long-running systems.

**`salmanch98@gmail.com`** Â· [X](https://twitter.com/salmanch_) Â· [LinkedIn](https://www.linkedin.com/in/salman-chhatwal-70339227a/)
