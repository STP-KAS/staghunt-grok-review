> **Experimental only. Not a product.** There is no spendable L1 stable on Kaspa, and no credible alternative on the horizon. Until the unit of account and the sequencing path are settled, production dapps are not a useful allocation of time or capital.
>
> Do not use wallet integrations on this GitHub. STP remains a clown. [DISCLAIMER.md](DISCLAIMER.md)

# Independent review — hashd.ag / Project Staghunt

**Not an audit. Not a security review. Not a certification. Not Kaspa core. Not KEF. Not Staghunt. Not a pin.**

Independent Grok Build pass (Windows desk, 20 Sep 2026) of [hashd.ag](https://hashd.ag/) and [staghunt.ai](https://www.staghunt.ai/).

Sisters this pass is scored against:

| File | Job |
| --- | --- |
| [STP-KAS/kaspa-master-file](https://github.com/STP-KAS/kaspa-master-file) | Pin encyclopedia. Staghunt was **dropped** as a pin (14 Sep BankQuote scan). A tweet is not a KIP. |
| [kaspanet/rusty-kaspa](https://github.com/kaspanet/rusty-kaspa) | Live node. v2.0.1. Toccata live. DAGKnight **not shipped**. |
| [kaspanet/silverscript](https://github.com/kaspanet/silverscript) | Compiler v1.0.0. Not an intendo VM. |
| [argent-lang/argent](https://github.com/argent-lang/argent) | No tag. README still not release-ready. |
| [kaspanet/vprogs](https://github.com/kaspanet/vprogs) | Research. Not product. |

Primary (Yonatan / hashdag): [hashd.ag](https://hashd.ag/) · [hashdag/hashdag.github.io](https://github.com/hashdag/hashdag.github.io) `ffabfd4` (6 Apr 2026) · six-pager PDF · Oxford Union PDF · [CoinDesk sponsored, 30 Jun 2026](https://www.coindesk.com/sponsored-content/beyond-self-custody-staghunt-and-the-missing-layer-of-the-internet)

Not primary: [coordmarket.com](https://coordmarket.com/) · [intendo.info](https://intendo.info/) (marketing rewrite; overclaim).

---

**A one-word Vercel page is not a coordination market. An Oxford speech is not a KIP. Covenants live is not intendos live.**

## Verdict

| Claim | Holds? |
| --- | --- |
| hashd.ag is Yonatan Sompolinsky’s essay site | **Yes.** Static IBM Plex Mono page. Source: `hashdag/hashdag.github.io`. |
| Project Staghunt six-pager exists | **Yes.** Dated 2026-04-01. Weight 100 on the site. PDF at `/project-staghunt-six-pager.pdf`. |
| Oxford Union address exists | **Yes.** Dated 2026-03-01. PDF at `/oxford-union-address.pdf`. |
| The game-theory diagnosis is coherent | **Yes.** Stag Hunt ≠ Prisoner’s Dilemma. Assurance contracts are a real class (Bagnoli–Lipman 1989). |
| staghunt.ai is Intendo Terminal | **No.** Homepage is the word `STAGHUNT`. Last-Modified **10 Sep 2026**. `/app` `/terminal` `/intendo` `/api` → **404**. |
| Intendo Terminal launched July 2026 | **No evidence.** CoinDesk sponsored copy (30 Jun) said “scheduled to launch its first version in July.” This desk, 20 Sep, finds a stub. |
| Coordination markets settle on Kaspa today | **No.** No public intendo primitive, pack solver, thFHE, or hunt snap. |
| Four axioms implemented | **No public code.** The six-pager *requires* four new stack pieces. None are a merged KIP. |
| Toccata covenants can host *some* of this | **Maybe later.** Covenants are live (desk pin). They are loop-free spend rules, not opaque pack accumulation. |
| Kaspa “satisfies all four axioms at once” | **No.** That sentence is from unofficial marketing sites, not from the six-pager. The six-pager lists missing components. |
| DAGKnight / 100 BPS / full RTD as stated | **Not shipped.** Open rusty-kaspa cluster. Last `dagknight` tip still early Sep. |
| vProgs / TangVM / miner oracles | **Research.** Not a product testnet this desk can hit. |
| Staghunt is a Kaspa pin | **No.** Master file dropped it on 14 Sep 2026. Keep it dropped. |
| “The raise is already the product” | **Unverified.** No public intendo-raise this desk could sign, inspect, or fail. |

Local host this pass: [http://127.0.0.1:8086/](http://127.0.0.1:8086/) is a **staghunt.ai-shaped teaching terminal** (same black/gold/IBM Plex Mono; hunt, pack, opacity, snap). It is a toy, not Intendo Terminal. Essays clone: [http://127.0.0.1:8084/](http://127.0.0.1:8084/). See [LOCAL.md](LOCAL.md).

## What

hashd.ag is Yonatan Sompolinsky’s (hashdag) public notebook. It is not a dapp. The 6 Apr 2026 GitHub tree is a static generator: `entries.json` → `build.js` → one HTML page + `/raw`. The accompanying `hashdag-technical-spec.docx` specifies **the website**, not a coordination protocol.

Two 2026 texts sit at weight 100 (canon):

1. **Project Staghunt — A Six Pager on Coordination Markets** (1 Apr 2026).
2. **Oxford Union Address** (March 2026).

The Feb 2026 essay *In which it was never my choice to hold the fire we found* is the Kaspa- situating piece: RTD, covenants, vProgs, TangVM, miner oracles. Staghunt is the application-layer claim that sits on that stack.

**Intended product (not observed live):** Intendo Terminal. Users sign conditional commitments (“I do X if N others do X”). Commitments pack opaquely. When a mutually-satisfying subset exists, execution snaps atomically. First market: crypto coordination (token launch with credible capital, LP migration, positions no one enters alone). First *demo of the demo*: a fundraise that only closes when the pack forms.

**What this desk actually fetched 20 Sep 2026:**

- hashd.ag essays + PDFs: **up**.
- hashdag GitHub: last push **6 Apr 2026**.
- staghunt.ai: **3 KB HTML**, title `STAGHUNT`, Vercel, no app JS.
- GitHub search `user:hashdag`: public `site` + `hashdag.github.io`. No intendo repo. No terminal repo. No FHE repo.
- coordmarket.com / intendo.info: third-party landing pages that paraphrase the six-pager and then **upgrade** it into “Kaspa satisfies all four.”

## Why (the thesis, steelmanned)

The interesting claim is not “crypto will fix society.” It is a classification:

- **Moloch / Prisoner’s Dilemma:** cooperation is not an equilibrium. You need restraint, punishment, or a Leviathan.
- **Azazel / Stag Hunt:** cooperation *is* an equilibrium, but so is the safe hare. The failure is failing to *reach* the good equilibrium. People already want to move together. They lack a binding “I move iff enough others move.”

That distinction is old and good. Rousseau’s hunt, Hume’s rowboat, Skyrms (*The Stag Hunt and the Evolution of Social Structure*, 2004), Schelling focal points, Bagnoli–Lipman assurance contracts (1989), PledgeBank, Kickstarter, Tabarrok dominant assurance contracts. Yonatan’s move is to say the internet built cheap talk and self-custody, and stopped before **binding group action**.

Four axioms he treats as load-bearing:

1. **Coordinated atomicity** — the qualifying subset executes together or not at all.
2. **Accumulation opacity** — nobody sees how close the threshold is (anti-snipe, anti-exposure).
3. **Capital multiplexing** — same capital backs several hunts; first snap wins.
4. **Composability** — hunts chain: users migrate, capital deploys, infra appears in one event.

He names the missing CS/crypto pieces honestly in §6 of the six-pager:

- persistent **intendos** (beyond CowSwap-style intents)
- a **monotone fixed-point** pack solver (“largest internally-satisfying subset”), claimed O(polylog) / O(1) amortized
- a **computation-fee** market for that solver
- **threshold FHE** (not interactive sMPC) for opacity, mixed-mode
- **designated verifier proofs** so packs can still gossip without leaking
- settlement on **real-time decentralization** so the gap between pack-found and pack-executed is one internet RTT

Hayek line he leans on: the consistent individualist should be an enthusiastic supporter of **voluntary associations**. Cypherpunks built the roads (TCP, keys, PoW, UTXO). He wants a different temperament to build the civic layer.

That is the why. It is a research program plus a company narrative, not a shipped market.

## Why it does not round up to a product (technical)

Desk law: merged Active KIP = law. Open PR, speech, sponsored article ≠ pin.

| Required by the six-pager | Live Kaspa 20 Sep 2026 |
| --- | --- |
| Binding conditional spend | **Toccata covenants** (KIP-16/17/20/21, 30 Jun 2026). Loop-free. Necessary, not sufficient. |
| Language / compiler | SilverScript **v1.0.0**. Argent **no tag**, not release-ready. |
| Opaque accumulation | **Absent.** No thFHE, no DKG-for-packs in rusty-kaspa. A public UTXO covenant is the opposite of axiom 2. |
| Pack solver | **Absent.** No repo, no KIP, no gas schedule for “max internally-satisfying subset.” Heterogeneous thresholds is a combinatorial search, not a `k=N` Kickstarter bar. |
| Capital multiplexing | UTXO *can* pre-authorize several spends. No product that races conflicting intendos and applies the first snap. |
| Atomic cross-domain execution (BNB LP → Kaspa pool, Netflix-class subscribe) | Needs bridges, oracles, off-chain settlement. The Feb essay’s miner-oracle / TangVM / UniSc stack is **not live**. |
| RTD as “majority of honest blocks per internet RTT” | 10 BPS GHOSTDAG is live (Crescendo). The exponential bound he quotes gets sharper at 100 BPS. **100 BPS and DAGKnight are not shipped.** Partial synchrony (fast in peace, slow-but-safe in war) is a property of the *next* ordering rule, not a product users have. |
| Intendo Terminal | staghunt.ai stub. |

Hard tensions the six-pager names and does not close:

- **Opacity vs attention.** Axiom 2 hides the pack. Momentum needs visibility. DVPs are the proposed patch. No implementation.
- **n-player ≠ 2x2.** In the textbook stag hunt, stag-stag is Nash and hare-hare is Nash. With heterogeneous thresholds, free-riders, cheap “I’ll join if 10,000 join” signatures, and first-trigger multiplexing, **defection and manipulation come back.** Opacity makes that worse: you cannot even watch the attack.
- **Solvers are a trusted compute class** until the FHE story is real. “Operators/searchers continuously checking subsets” is MEV-shaped. He wants mixed-mode thFHE so only the essential bits stay encrypted. That is a research bet, not a 2026 mainnet feature.
- **Fair-launch L1 + venture application.** His own Absurd #1: Kaspa funded like fair-launch, innovates like premined. Staghunt-as-company sitting on Kaspa-as-commons is the same paradox one layer up.
- **Culture-war examples** (streaming “woke agenda,” coming-out thresholds) are optional marketing. They are not required by the mechanism. Do not confuse them with the CS.

Fan sites that say “Kaspa satisfies all four at once” are **wrong**. Yonatan’s own list of missing components contradicts them. Treat coordmarket.com / intendo.info as unofficial.

## Philosophy (short; full note in [PHILOSOPHY.md](PHILOSOPHY.md))

Scott Alexander’s Moloch essay overfit the prisoner’s dilemma onto every social failure. Yonatan’s correction is fair: a lot of “why doesn’t anyone do the obvious good thing” is **assurance**, not temptation to cheat.

Skyrms already said the social contract is a stag hunt. Tabarrok already said Kickstarter-style assurance is not enough and proposed **refund bonuses** so contributing is dominant even if the pack fails. Yonatan does not engage Tabarrok. That is a hole: if the problem is “hare is safer,” a dominant-strategy patch is the economist’s first tool. Opacity-plus-atomic-snap is a different tool, aimed at **exposure** and **snipe**, not at making contribution strictly dominant.

Hayek / de Tocqueville / Winner are doing real work in the Oxford text: shallow digital bonds, artifacts have politics, cypherpunk temperament built distrust-minimizing roads and then stalled on association. Agree or not, that is a serious civic diagnosis. It does not license rounding a stub domain into “the missing layer of the internet.”

## Conclusion

1. **Read the six-pager.** The classification (Azazel vs Moloch) is the valuable part. It is better than most Kaspa narrative decks.
2. **Do not buy, integrate, or pin Staghunt.** There is no terminal, no intendo bytecode, no pack object, no hunt transaction, no raise this desk can inspect.
3. **Do not weld it to Toccata.** Covenants are a primitive. Staghunt is a proposed use. Live primitive + missing use ≠ live use.
4. **Keep the master-file drop.** Community X, CoinDesk sponsored copy, and landing pages are catalog, not law.
5. **Re-open the file only on artifacts:** a public repo with a pack solver; a testnet hunt that snaps a covenant; a KIP for opaque accumulation; a tagged Intendo Terminal. Until then it stays a speech.

## Advice

**For this desk**

- Do not staff a coordination-market dapp. Same rule as native L1 DeFi: no spendable L1 dollar, sequencing path unsettled, Argent untagged.
- Honest work stays receipts, tills (quote fiat, settle native KAS), public-goods pins, covenant *reading*.
- Local essays: `http://127.0.0.1:8084/` (clone of hashd.ag, this machine only).

**For Yonatan / Staghunt, if they want the thesis to survive contact with engineers**

1. Publish the pack-solver as code and complexity proofs, not a sentence about monotone fixed points.
2. Pick one axiom to ship first on TN10: **atomic Kickstarter-on-covenants** (drop opacity). Opacity is the expensive one. A visible assurance contract on Toccata would already be more than Kickstarter-on-Stripe.
3. Do not claim RTD-uniqueness until DAGKnight is merged. 10 BPS is already fast enough for human coordination; the FHE/solver/oracle gap is the blocker, not 100 ms vs 10 ms.
4. Take the CoinDesk July date off the table or ship the terminal. A 10 Sep stub that still says STAGHUNT is worse than a 404.
5. Mark coordmarket.com / intendo.info as unofficial or take them down. They currently overclaim the L1.

**For Kaspa readers**

- hashd.ag is worth an afternoon. staghunt.ai is not worth a wallet connect.
- If someone says “Yonatan is building coordination markets on Kaspa,” ask: **where is the hunt tx?** Silence is the answer today.

## What Grok did

1. Fetched hashd.ag (full essay corpus), `/staghunt`, `/kaspa`, `/fragments`, both PDFs.
2. Fetched staghunt.ai HTML + HEAD of `/`, `/app`, `/terminal`, `/intendo`, `/api`.
3. Cloned `hashdag/hashdag.github.io` at `ffabfd4`. Read `build.js`, `dashboard.md`, `entries.json` structure, `hashdag-technical-spec.docx`.
4. Read CoinDesk sponsored article (30 Jun 2026), Bitcoin Takeover S17E36 notes, Wikipedia Sompolinsky page.
5. Fetched coordmarket.com and intendo.info (unofficial).
6. GitHub: `user:hashdag` public repos; code/repo search for Staghunt/Intendo product (none).
7. Scored against kaspa-master-file pins: rusty v2.0.1, silverc v1.0.0, Toccata live, DAGKnight not shipped, Argent no tag, vProgs research, Staghunt dropped.
8. Served the 6 Apr clone at `127.0.0.1:8084`.

**Did not:** send funds; sign an intendo; install a wallet inject; treat a sponsored article as a ship date; treat fan sites as primary.

Sources: [SOURCES.md](SOURCES.md). Stack table: [STACK.md](STACK.md). Philosophy: [PHILOSOPHY.md](PHILOSOPHY.md). Local host: [LOCAL.md](LOCAL.md).

## What this repo is not

- Not hashd.ag, not staghunt.ai, not Kaspa core.
- Not a product, terminal, or fundraise.
- Not a wallet kit. No inject.
- Not a seed prompt.

Errors of fact: open an issue or PR. Issue #1 asks hashdag to challenge the verdict. Silence is not agreement.

---

> **Standard disclaimer.** This GitHub, not the topic above.
>
> Intentions are good; thought process is questionable. STP remains delusional. Si vis pacem, para bellum.
>
> Intern at https://sixpack.wtf/  
> X: https://x.com/StppStp · GitHub: https://github.com/STP-KAS
