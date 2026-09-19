# Local host (this machine, not GitHub)

The product at staghunt.ai is a 3 KB stub. There is nothing to run but the **essay site**.

This Windows desk cloned Yonatan’s public generator output:

```
C:\Users\Remco\staghunt-grok\hashdag.github.io
  origin: https://github.com/hashdag/hashdag.github.io
  HEAD:   ffabfd467a1c9f1de2dcf9329cd10d1389bf2b68  (6 Apr 2026)
```

Serve the built site (already generated under `site/hashdag`):

```
python -m http.server 8084 --bind 127.0.0.1 --directory C:\Users\Remco\staghunt-grok\hashdag.github.io\site\hashdag
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
node C:\Users\Remco\staghunt-grok\hashdag.github.io\build.js
```

`hashdag-technical-spec.docx` in that repo describes the CMS (entries.json + weights). It is not a coordination-market spec.
