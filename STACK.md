# Stack — six-pager requirements vs live Kaspa

Not a protocol spec. Mapping Yonatan’s own §6 list onto what this desk already pins. Date: **20 Sep 2026**.

## Four axioms

| Axiom | Meaning | Live? |
| --- | --- | --- |
| Coordinated atomicity | Qualifying subset executes together; no partial fill | **Not as a hunt object.** L1 txs are atomic *per transaction*. A multi-party “everyone migrates” event needs a constructed all-or-nothing set. Covenants can lock spends. They do not, by themselves, scan a hidden pack and fire N spends at once. |
| Accumulation opacity | Nobody — user or operator — sees progress to threshold | **No.** Public UTXO / public mempool is the default. thFHE + DKG is named, not shipped. |
| Capital multiplexing | Same funds back several hunts; first snap consumes them | **No product.** UTXO double-spend / first-seen is a race, not a pack solver. Conflicting intendos “whatever triggers first” is MEV-adjacent. |
| Composability | Hunt output is another hunt’s input | **No hunt type** to compose. Covenants compose with other covenants in a limited, loop-free way. That is not “users + capital + infra in one event.” |

## Six-pager §6 components

### i. Intendos

Persistent, conditional, composable intents. He cites CowSwap as a limited ancestor.

| Nearby Kaspa object | Status | Gap |
| --- | --- | --- |
| Toccata covenants | **Live** | Spend rules on a UTXO. No “if N others also signed this template.” |
| SilverScript v1.0.0 | **Tagged** | Compiler for those rules. Not an intent pool. |
| Argent | **No tag** | Higher language. Still not release-ready. |
| KIP-21 sequencing commitments | **Live as consensus primitive** | Not an app-level pack. |

Verdict: the word “intendo” is not a type in rusty-kaspa.

### ii. Pack solver

“Current maximum subset with internally-satisfying thresholds.” Claimed class: monotone fixed-point, incremental O(polylog) or O(1) amortized.

If every agent i has threshold t_i in *count* or *capital*, and you need a set S such that for all i in S, t_i is met by S, the greatest such S under inclusion is a greatest fixed point of a monotone operator (throw out anyone whose t_i is unmet, repeat). For **count** thresholds that is cheap. For **capital** thresholds it is still monotone. For **arbitrary predicates** (oracles, other hunts, off-chain facts) it is not.

The six-pager also wants solvers/searchers paid to keep doing this continuously. That is a new market. No repo.

### iii. Computation fee / “gas per intendo”

Metering the solver. No KIP, no fee market, no operator set.

### iv. Opacity crypto

He rejects interactive sMPC over an open validator set. Alternative: **threshold FHE**, DKG once, light sMPC only at decrypt. Mixed-mode: encrypt only the essential bits.

Kaspa L1 does not run FHE. Toccata’s ZK precompile is a different object (proof verify), not a shared encrypted pack accumulator.

**Designated verifier proofs** (DVPs / MDVS) are proposed for p2p gossip that remains deniable if leaked. Not in the node.

## Settlement: RTD

Yonatan’s metaproperty: each consensus epoch (at least one internet RTT, probably several) contains an honest majority of blocks. He writes

Pr(byzantine ≥ 50%) ≤ O(exp(−c · T · λ))

with λ = block rate. 10 BPS already makes a ~1s window sharp; 100 BPS is the dream. DAGKnight is the parameterless ordering rule that is supposed to make 100 BPS not pay a worst-case-latency k penalty.

| Piece | Status |
| --- | --- |
| 10 BPS GHOSTDAG | **Live** (Crescendo) |
| DAGKnight | **Not shipped** |
| 100 BPS | **Not shipped** (he has said ~2027 HF in the Feb essay) |
| Miner oracles / no-slash handicap | **Proposal** in the Feb essay |
| TangVM / UniSc | **Proposal** |

10 BPS is enough for *human* coordination latency. It is not the missing piece. The missing pieces are opacity, the solver, and a hunt object.

## What covenants actually give you (honest subset)

A visible, on-chain **assurance contract** is constructible in principle:

- N parties lock KAS (or a covenant UTXO) to a template “payout if threshold, else refund.”
- A final tx spends all of them together.
- If the pack fails, refund paths fire after timeout.

That is Kickstarter-on-UTXO. It **violates axiom 2** (everyone can count the locks). It **can** satisfy a weak form of axiom 1 (atomic payout tx). It does **not** multiplex conflicting destinations without extra rules.

If Staghunt shipped *that* on TN10, this desk would re-open the file as a covenant demo, not as “the missing layer of the internet.”

## Fan-site mapping (wrong)

coordmarket.com maps:

- Commitment → Covenants (partial)
- Opacity → “ZK Programs” (vProgs; research; also ZK verify ≠ FHE pack)
- Multiplexing → UTXO model (possible, not built)
- Resistance → PoW (true of Kaspa, not of Staghunt)

Then: “Kaspa satisfies all four at once.” **False.** The six-pager is the rebuttal.

## Re-open criteria

Re-score only if at least one of these exists:

1. Public repo with a pack solver and tests.
2. A Kaspa (mainnet or TN10) transaction that is a hunt snap, with a hash this desk can fetch from REST.
3. A KIP (Proposed/Active) for opaque accumulation or intendos.
4. A tagged Intendo Terminal that is more than a word on a Vercel page.
