# netlab

My lab work for Programmable Networks. Every network here is described as data, checked
before it's built, and published as a page from the same file.

- **Week 2** — a switched network: `topology.yaml`, `build_topo.py`, `make_page.py`, `page.yaml`,
  evidence in `evidence/`, page at `docs/index.html`.
- **Week 3** — a routed network: four routers in a ring, static routes with a /23 summary per site.
  `network.yaml`, `build_routed.py`, `make_page3.py`, `page3.yaml`, broken copies `loop.yaml` and
  `missing.yaml`, evidence in `evidence3/`, page at `docs/week3/index.html`.

```
python3 build_routed.py network.yaml    # check, then build in Mininet
python3 make_page3.py network.yaml      # check, then write docs/week3/index.html
```

`evidence3.mn` holds the Mininet commands that produced `evidence3/` (run with `source evidence3.mn`
at the `mininet>` prompt).

## AI use

Week 3 (Level 3, Open): I used Claude Code (Claude Opus 5.5) as an assistant.

- It proposed the two-site ring design and address plan in `network.yaml`, which I chose.
- It wrote `check_paths()` in `build_routed.py` and `routing_tables_section()` in `make_page3.py`,
  and made the broken copies `loop.yaml` and `missing.yaml`.
- It ran the checks and the network in Mininet and saved the output in `evidence3/`. Docker Desktop
  wouldn't start on my machine, so this ran in Mininet 2.3.0 installed directly in WSL Ubuntu
  instead of the course container.
- It drafted the answers in `page3.yaml` from my evidence; I reviewed and edited them.

I've checked the design, the code and the evidence, and can explain all of it.
