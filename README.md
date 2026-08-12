# schumpeter-perspective

A **portable perspective module** that analyzes economic, political, historical, and institutional questions through the documented thinking style of the Austrian-American economist and sociologist **Joseph A. Schumpeter** (1883–1950) — judge a system by how it creates and destroys structures rather than how it administers them, strip the analytic kernel from the ideological cloak, and treat prognosis as no kind of advocacy.

It is a *thinking-style tool* for analysis and ideation. It is not affiliated with or authored by Joseph Schumpeter or his estate, and it must not be used to attribute invented statements to him. See [Disclaimer](#disclaimer).

---

## What it is

Plain Markdown, no code and no dependencies. A front-loaded core file carries the persona; a `references/` tree carries the depth, loaded on demand rather than all at once.

That makes it usable anywhere a model can be given text: drop it into an agent framework that reads instruction files from a directory, paste the core file in as a system prompt, attach it to a chat, retrieve the reference modules through RAG, or read it yourself as a study aid. The core is deliberately kept small (~4,200 tokens) so it fits in a system prompt with room to spare; the reference files are sized for individual retrieval (~1,200–3,900 tokens each).

Two of the reference modules are standing and cross-corpus: `frameworks.md` (what he thinks with) and `voice.md` (how he sounds). The core carries only a style *fingerprint* by design; `voice.md` carries the system — constructions, the measured avoid-list, modulation rules with absolute targets per register, and the baseline the fidelity tests measure against. Load it whenever the task is to write in the voice at length rather than only to reason in the frame.

Only one convention is tool-specific: the YAML frontmatter at the top of `SKILL.md`, which agent runtimes use for discovery and auto-loading. Nothing else depends on it — strip the frontmatter and the file still works as a prompt.

## What it does

Given a question, it reframes it the way Schumpeter's published work does:

- **Create and destroy, not administer.** The problem usually visualized is how a system manages existing structures; the relevant problem is nearly always how it makes and unmakes them.
- **Judge over time, never from a moment.** A system that at every instant makes the best of its possibilities may lose over fifty years to one that never does — because the failure is a condition of the speed.
- **Separate the function from its occupant.** The entrepreneurial function is not the capitalist, inventor, manager, or owner. A class is not the families in it — a class is a hotel or an omnibus, always full and always of different people.
- **Kernel and cloak.** In any doctrine, appraise the analytic core and surrender the ideology it came wrapped in — then say plainly that the wrapping is what made it famous.
- **Vision is ideological; ideologies are not lies.** No one stands on the rock of absolute truth, including him. But explaining why a man says something tells you nothing about whether it is true.
- **Look for the atavism.** When something looks irrational in a rationalist civilization, test first whether it is a survival from a structure already dead.
- **Prognosis is not advocacy.** He forecasts the end of an order without wishing it, and refuses to close with recommendations — knowing exactly what that refusal costs him in readership.

It also **modulates register** with the work it is drawing on — definitional and model-building for innovation and cycles, hedge-heavy and interrogative for the public argument, dense and footnote-conscious for method and appraisal, fast and declarative for the sociology.

## When to use it

Good fits:

- Innovation, disruption, competition and monopoly policy, the dynamics of technological change
- Institutional decay and renewal; why a successful organization undermines its own foundations
- Elites, class, professions, and the rise and decline of a stratum
- Forecasting by mechanism rather than by date
- The sociology of war, expansion, and state violence
- Fiscal questions read from the budget outward
- Appraising a body of work, a school, or a research programme — separating performance from reputation

Poor fits (the skill will reframe or decline rather than hold a real position):

- Requests for a policy recommendation — the refusal is a core feature, not a limitation of the distillation
- Anything after January 1950, where the persona extrapolates a mechanism rather than reporting a position
- The specifics of his stance on the New Deal and Keynesian recovery policy — the source volume is truncated in the corpus
- Personal or biographical questions; no correspondence or diaries are in the corpus

Confidence boundaries are documented in [`fidelity-ledger/provenance.md`](fidelity-ledger/provenance.md).

## Structure

```
schumpeter-perspective/
├── SKILL.md                    core persona, front-loaded — load this first, always
├── references/                 depth, loaded on demand — host-agent-facing, never contains provenance
│   ├── frameworks.md           named constructs in his exact senses
│   ├── voice.md                the measured expressive system — load before writing at length
│   ├── clusters/               one module per source work
│   │   ├── c01-c03-business-cycles.md
│   │   ├── c04-c08-capitalism-socialism-democracy.md
│   │   ├── c09-c10-history-of-economic-analysis.md
│   │   ├── c11-c12-imperialism-social-classes.md
│   │   └── c13-tax-state.md
│   └── episodic.md             attested lower-priority material
├── fidelity-ledger/            human-facing, never loaded by the host agent
│   ├── provenance.md           source map, fidelity scores, gaps
│   └── scores.json             per-element scoring audit log
├── LICENSE
├── NOTICE.md
└── CHANGELOG.md
```

The core is front-loaded on purpose: the highest-identification content sits at the top, so that if the file is truncated from the end — by a context limit, by compaction, by a shorter excerpt — what survives is still the part that carries the voice.

## Using it

**As a system prompt.** Paste `SKILL.md` in whole. Strip the YAML frontmatter if your setup does not expect it; nothing below it depends on the frontmatter.

**In an agent framework.** Put the directory wherever the runtime looks for instruction modules. The last section of `SKILL.md` tells the host agent which reference file to pull for which kind of question, so the depth stays out of the context window until it is wanted.

**With retrieval.** Index `references/` and let the core file's routing section drive which module gets fetched. Each is self-contained and sized for a single retrieval.

**Without a model at all.** `frameworks.md` is a usable reference on Schumpeter's terminology, and `fidelity-ledger/provenance.md` documents exactly which claim rests on which source.

## Source corpus

Five single-authored works, ~1,143,000 words, spanning 1918–1954:

| work | year | in corpus |
|---|---|---|
| "The Crisis of the Tax State" | 1918 | complete (OCR-degraded) |
| *Imperialism and Social Classes* (two essays) | 1919, 1927 | complete, in translation |
| *Business Cycles* | 1939 | **Chapters I–VIII only** |
| *Capitalism, Socialism and Democracy* | 1942/46/49 | complete, incl. all three prefaces |
| *History of Economic Analysis* | 1954 | complete, Parts I–V |

Built with [`persona-distiller`](https://github.com/ariel-lee-1023/persona-distiller) in full-rigor mode. Both pre-assembly gates passed: the projection test scored 1.00 on a blind arm of four items drawn from unread passages, and all 16 attested cost-bearing refusals are present in the core.

## Disclaimer

This skill distills a **thinking style** from published work. It does not reproduce Schumpeter's prose, and its output is not his writing. Do not present anything it generates as a quotation from, or a position of, Joseph Schumpeter. Where his exact terminology is preserved — *creative destruction*, *objectless disposition*, *Vision*, *atavism* — it is preserved for traceability to the source, and named as such.
