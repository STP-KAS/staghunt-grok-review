# Local host (this machine, not GitHub)

The live product at [staghunt.ai](https://www.staghunt.ai/) is a 3 KB stub (one word). This desk hosts two local things. Neither talks to Kaspa. Neither is Intendo Terminal.

## Coordination toy — http://127.0.0.1:8086/

A staghunt.ai-shaped page: same black, gold, IBM Plex Mono. Under the title it is a **teaching hunt**: sign intendos, hide the count (axiom 2), run the monotone pack solver, snap atomically. Default stags are mostly *outside* crypto (agent swarm, shop hours, leaving an app, a shelf that only exists if it is subscribed). LP migration is the crypto cousin.

```
python -m http.server 8086 --bind 127.0.0.1 --directory C:\Users\<user>\staghunt-grok\staghunt-ai-local
```

Source in this repo: [`local-terminal/index.html`](local-terminal/index.html). Browser-only. localStorage. No wallet, no seed, no inject. Opacity is a checkbox, not thFHE.

## Essay mirror — http://127.0.0.1:8084/

This Windows desk cloned Yonatan’s public generator output:

```
C:\Users\<user>\staghunt-grok\hashdag.github.io
  origin: https://github.com/hashdag/hashdag.github.io
  HEAD:   ffabfd467a1c9f1de2dcf9329cd10d1389bf2b68  (6 Apr 2026)
```

Serve the built site (already generated under `site/hashdag`):

```
python -m http.server 8084 --bind 127.0.0.1 --directory C:\Users\<user>\staghunt-grok\hashdag.github.io\site\hashdag
```

Then:

| Path | What |
| --- | --- |
| http://127.0.0.1:8084/ | hashd.ag home (all entries) |
| http://127.0.0.1:8084/staghunt/ | six-pager + Oxford |
| http://127.0.0.1:8084/kaspa/ | Kaspa essays |
| http://127.0.0.1:8084/fragments/ | fragments |
| http://127.0.0.1:8084/raw.txt | plaintext corpus |
| http://127.0.0.1:8084/project-staghunt-six-pager.pdf | PDF |
| http://127.0.0.1:8084/oxford-union-address.pdf | PDF |

This is a **read-only mirror** of a public GitHub tree. It is not Intendo Terminal. It does not talk to Kaspa. Ports 8080–8083 on this desk are other local dapps (kns / gramlane / till / kns-spec). Do not collide.

Rebuild from source if you want to confirm `build.js`:

```
node C:\Users\<user>\staghunt-grok\hashdag.github.io\build.js
```

`hashdag-technical-spec.docx` in that repo describes the CMS (entries.json + weights). It is not a coordination-market spec.
