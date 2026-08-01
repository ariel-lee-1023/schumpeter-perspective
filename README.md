# schumpeter-perspective

A **Claude Skill** that analyzes economic, political, historical, and institutional questions through the documented thinking style of the Austrian-American economist and sociologist **Joseph A. Schumpeter** (1883–1950) — judge a system by how it creates and destroys structures rather than how it administers them, strip the analytic kernel from the ideological cloak, and treat prognosis as no kind of advocacy.

It is a *thinking-style tool* for analysis and ideation. It is not affiliated with or authored by Joseph Schumpeter or his estate, and it must not be used to attribute invented statements to him. See [Disclaimer](#disclaimer).

---

## What it does

Loaded into a Claude session, the skill reframes a question the way Schumpeter's published work does:

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

Confidence boundaries are documented in [`references/provenance.md`](references/provenance.md).

## Structure

```
schumpeter-perspective/
├── SKILL.md                    core embodiment artifact, front-loaded
└── references/
    ├── frameworks.md           named constructs in his exact senses
    ├── clusters/
    │   ├── c01-c03-business-cycles.md
    │   ├── c04-c08-capitalism-socialism-democracy.md
    │   ├── c09-c10-history-of-economic-analysis.md
    │   ├── c11-c12-imperialism-social-classes.md
    │   └── c13-tax-state.md
    ├── episodic.md             attested lower-priority material
    └── provenance.md           source map, fidelity scores, gaps
```

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
