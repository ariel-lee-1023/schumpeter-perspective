# Provenance & fidelity ledger

The honesty lives here, never in `SKILL.md`. Built by the `persona-distiller` pipeline
(full-rigor mode) from five works, **~1,143,000 words** of single-authored text spanning
1918–1954.

## Corpus & coverage map

| cluster | source | words | kind | period | domains |
|---|---|---|---|---|---|
| c01–c03 | *Business Cycles* (1939), Ch. I–VIII | 137k | monologic treatise | 1939 | innovation, entrepreneur, credit, equilibrium, cycles, economic history to 1929 |
| c04–c08 | *Capitalism, Socialism and Democracy* (1942/46/49), complete | 209k | argumentative essay + 3 prefaces | 1942–49 | Marx, creative destruction, decay thesis, socialism, democracy, party history, **replies to critics** |
| c09–c10 | *History of Economic Analysis* (1954), complete Parts I–V | 709k | scholarly history | written 1940s | method, vision/ideology, doctrine history, several hundred appraisals |
| c11–c12 | *Imperialism and Social Classes* (1919, 1927) | 67k | sociological essays, trans. | 1919/1927 | imperialism, atavism, class function and mobility |
| c13 | "The Crisis of the Tax State" (1918) | 21k | lecture-essay, trans. | 1918 | fiscal sociology, state capacity, early decay thesis |

**Dialogue ratio ≈ 0.03.** The corpus is near-monologic. Genuine exchange exists only in the
CSD prefaces (Schumpeter answering named criticisms) and in reported conversations inside HEA
footnotes. There are no interviews, letters, diaries, lecture transcripts, or adversarial
sources in the corpus.

**Temporal spread:** good. Both the German-language period (1918–1927) and the American period
(1939–1954) are represented, which is what makes it possible to establish that the decay thesis
predates the exile by twenty-four years.

## Weight vector (auto-adjusted for a near-monologic corpus)

projectibility **0.33** · cost_refusal **0.25** · expressive_match **0.20** ·
interactional **0.12** · preoccupation **0.10**

*Adjustment:* dialogue_ratio ~0.03 → interactional 0.15→0.12, projectibility 0.30→0.33,
renormalized to 1.00 (auto-weight hook, `scoring.md`). Deletion threshold 0.55.
**51 elements scored → 45 core, 6 to references.** Style cap applied: 9 of 45 core slots
maximum for `stable_style`; only 1 was used.

Full audit log with per-probe scores: `references/scores.json`.

## Core element ledger — cost-bearing refusals

| element | core section | sources | clusters | composite | cost-gate |
|---|---|---|---|---|---|
| success not failure kills capitalism; the Vanderbilts as pacemakers | Will not concede | CSD | c05 | 0.92 | high-signal, in core |
| prognosis ≠ advocacy; **names the price** of refusing policy | Will not concede / How I move | CSD prefaces, HEA, Tax State | c05, c08, c09, c13 | 0.92 | high-signal, in core |
| the sinking-ship report is not defeatism | Will not concede | CSD 2nd-ed. preface | c08 | 0.91 | high-signal, in core |
| judge the process over decades, never *ex visu* of a moment | How I read / Will not concede | CSD, Business Cycles | c01, c05, c08 | 0.89 | high-signal, in core |
| ideology is universal including mine — *and* ideologies are not lies | How I read / Will not concede | HEA Pt I | c09, c10 | 0.88 | high-signal, in core |
| Marx is great **and** Marxism is a religion | Will not concede | CSD Pt I, HEA Pt III | c04, c08, c10 | 0.87 | high-signal, in core |
| would choose economic history over theory if allowed only one | Will not concede | HEA Pt I | c09 | 0.86 | high-signal, in core |
| "Can socialism work? Of course it can." | Will not concede | CSD Pt III | c06 | 0.84 | high-signal, in core |
| the bourgeoisie is politically helpless; Holy Grail / boo to a goose | Will not concede | CSD, Imperialism, Tax State | c05, c11, c13 | 0.84 | high-signal, in core |
| the case against monopoly is radical ideology | Will not concede | CSD ch.8 + preface | c05, c08 | 0.83 | high-signal, in core |
| entrepreneur ≠ inventor / capitalist / risk-bearer / owner / manager | How I read / Will not concede | Business Cycles, CSD | c01, c05 | 0.83 | high-signal, in core |
| imperialism is atavism, not a stage of capitalism | How I read / Will not concede | Imperialism | c11, c05, c12 | 0.83 | high-signal, in core |
| the classical doctrine of democracy is false; the method is still worth defending | Will not concede | CSD Pt IV | c07 | 0.80 | high-signal, in core |
| analytic progress is real; policy progress is meaningless | Will not concede | HEA Pt I | c09, c10 | 0.74 | high-signal, in core |
| the budget is the skeleton; the tax state has a limit | Keep returning to | Tax State | c13 | 0.72 | in core (compressed) |
| the three-cycle schema is a decision, not a hypothesis | Will not concede | Business Cycles | c02 | 0.62 | in core; **single cluster — thinner** |

## Core element ledger — regularities, interactional, modulation

| element | core section | clusters | composite |
|---|---|---|---|
| create/destroy structures, not administer them | How I read | c01, c05, c08 | 0.90 |
| vision precedes analysis; procedure grinds ideology out slowly | How I read | c09, c10 | 0.86 |
| strip the analytic kernel from the ideological cloak | How I read | c04, c09, c10 | 0.84 |
| judge performance over time | How I read | c01, c05, c08, c10 | 0.82 |
| concede everything except the decisive point | How I move | c04, c08, c09, c10 | 0.82 |
| separate the function from whoever fills it | How I read | c01, c05, c09, c12 | 0.80 |
| change is lopsided, discontinuous, clustered; find the ignition | How I read | c01, c02, c03 | 0.77 |
| refuse single causes; each episode is a historic individual | How I read | c01, c03, c10 | 0.76 |
| test whether it is a survival from a dead structure | How I read | c11, c05, c12 | 0.74 |
| "inevitable" = these tendencies, continued, nothing intruding | Will not concede | c05 | 0.74 |
| social structure before interests, for power/war/class/state | How I read | c11, c12, c13 | 0.72 |
| internal vs. external factors | How I read | c01 | 0.69 |
| created credit, not prior saving, shifts factors | frameworks.md only | c01 | 0.63 |
| refuse the "what should be done" question, re-aim at thinking | How I move | c08 | 0.82 |
| deny the *category* when a motive is imputed | How I move | c08 | 0.78 |
| lavish specific praise, then the knife | How I move | c04, c09, c10 | 0.76 |
| under contest, drop to numbered propositions | How I move | c08 | 0.73 |
| plainest-warrant appeal at the biggest claim | How I move | c01, c05 | 0.69 |
| state limitations as scope, never as apology | How I move | c08, c09 | 0.68 |
| refuse to revise when criticism has not landed | How I move | c08 | 0.64 |
| footnotes carry concessions, jokes and daggers | How I move | c10, c01, c09 | 0.62 |
| dissolve a dispute into terms where honest | How I move | c08, c10 | 0.62 |
| long build → short flat verdict; question-then-blunt-answer | How I sound | c01, c05, c06 | 0.72 |
| irony rises where the subject is sacred; hits poses, not arguments | How I sound | c04, c05, c09 | 0.71 |
| register shifts by work (measured, below) | How I sound | c01, c05, c10 | 0.58 |
| the analogy domains (physician/organism/weather/ship/omnibus/chivalric) | How I sound | all | 0.59 |
| destroyed by its own success | Keep returning to | c05, c11, c12, c13 | 0.84 |
| the gap between self-image and foundation | Keep returning to | c07, c09, c11, c13 | 0.81 |
| the innovating function and its obsolescence | Keep returning to | c01, c05, c10, c12 | 0.73 |

**Demoted to `episodic.md`:** untranslated foreign tags (0.43 — real but thin on its own);
ranking-and-placing as a habit (0.54 — largely an artifact of HEA's genre); first-person and
reader-address rates (0.34); hedge:booster rate as a bare number (0.30); sentence-length and
paragraph-length averages (0.12 each — generic).

## Measured style baseline

Aggregate: 1,143,323 words · 37,711 sentences · sentence mean **30.3**, median **25**, stdev
**44.2**, p10 **8**, p90 **57** · MATTR-500 lexical diversity **0.522** · hedges **8.1**/1k ·
boosters **3.9**/1k · hedge:booster **2.08** · person reference 38% first / 61% third / **0.2%
second**.

Per-work modulation (this is the individuating part, not the aggregate):

| | sent. mean | hedges/1k | boosters/1k | semicolons/1k | parentheticals/1k | questions/1k | 1st-person % |
|---|---|---|---|---|---|---|---|
| Business Cycles | 30.1 | 8.4 | 3.8 | 1.5 | 3.3 | 0.09 | **58.8** |
| CSD | 29.8 | **10.2** | 3.8 | 3.0 | 2.2 | **0.54** | 39.2 |
| History of Econ. Analysis | 30.7 | 7.6 | 3.8 | **8.0** | **9.7** | 0.32 | 35.2 |
| Imperialism / Social Classes | **27.9** | 7.1 | **5.3** | 2.3 | 1.5 | 0.46 | 35.1 |
| Tax State | 32.7 | 7.3 | 4.2 | 2.2 | 2.0 | 0.75 | 46.9 |

Em-dash and exclamation counts for the two translated volumes are corrupted by OCR damage and
were excluded.

## Fidelity results

### Projection test

Two arms were run. Seeded split: `holdout_split.py --seed 42 --frac 0.15` over 42 evidence
passages → 7 masked (`bc-innovation-not-invention`, `csd-creative-destruction`,
`csd-inevitability`, `csd-pref2-defeatism`, `csd-pref2-monopoly`, `hea-progress`,
`hea-smith-cloak`).

- **Seeded arm: 12/12 = 1.00** on 6 scorable items. `csd-inevitability` was **excluded for
  leakage** — its text sits inside `csd-p2-prologue`, which the split kept.
  **Caveat, recorded deliberately:** five of the six had been read during Stage 2 extraction, so
  this arm is inflated and should be read as a consistency check, not a blind test.
- **Blind arm (the one that counts): 8/8 = 1.00** on 4 items from passages not opened before
  prediction — Walras's ranking in HEA Pt IV; the mechanism of entrepreneurial obsolescence in
  "Crumbling Walls"; the war-machine formula in "Imperialism in Practice"; the determinants of
  class rise in "Social Classes." All four were predicted with correct stance *and* correct
  reasoning, including two signature images (theoretical-physics comparison; "created by wars
  that required it, it now creates the wars it requires") derived rather than recalled.

**Gate: PASS** (recorded as 0.95, discounting the seeded arm for exposure). No re-curation was
triggered; no weight change resulted.

**Per-domain confidence:**

| domain | confidence | basis |
|---|---|---|
| innovation, competition, entrepreneurship | **high** | 3 works, converging, blind-tested |
| method, bias, appraisal of ideas | **high** | HEA Pt I is explicit and systematic |
| institutional decay, elites, class | **high** | 4 works across 30 years, blind-tested |
| democratic theory | **medium-high** | one sustained treatment, unusually explicit |
| imperialism and war | **medium-high** | one work, but blind-tested and internally systematic |
| fiscal / public finance | **medium** | single source, shortest, most OCR-degraded |
| business-cycle statistics and the 1930s | **medium-low** | see gap below |

### Cost test

16 attested incentive-vs-characteristic divergence pairs enumerated in Stage 2; **16 slated for
core; 16 present in the assembled core**; 0 logged out. Minimum-presence assertion: **PASS**
(the "What I will not concede" section carries 15 explicitly and one in "What I keep returning
to"). The interactional minimum is also met — nine distinct exchange moves are in the core,
all evidenced from the CSD prefaces and HEA.

### Style-match test — **failed twice, forced two revisions of "How I sound"**

This is the only check that did not pass first time, and the loop it triggered changed the core.
Samples were generated under the core's expression rules and compared against **genre-matched
held-out originals** (CSD chapters 8 and 13 for exposition; the CSD 2nd-edition preface for the
contested register) rather than against the corpus aggregate, which is dominated by the
*History*'s doctrinal third person and is the wrong baseline for either.

**Failure 1 — the build rule was too vague to steer generation.**
Samples came out at sentence mean 19.4 (originals 30.3) with stdev 11.8 against 44.2. The rule
said "I build long… subordinated three and four clauses deep" and nothing executed it. Revised
to specify the *shape* operationally in voice — two or three sentences of fifty and sixty words
carrying concession and exception inside themselves before the main verb, then one of eight
words — plus a rule keeping the process rather than the author in subject position. Regenerated:
mean 29.2, and the exposition sample alone at **33.3 vs. 36.0** for the matched original, with
first-person **20.0% vs. 23.9%**. Passed.

**Failure 2 — a genuinely wrong modulation claim, caught by measurement.**
The rules implied he grows more careful under attack. He does the opposite, and the numbers are
unambiguous:

| | sent. mean | median | hedges/1k | boosters/1k | hedge:booster | 1st-person |
|---|---|---|---|---|---|---|
| **Schumpeter, CSD 2nd-ed. preface** | 26.7 | 23 | 7.24 | **7.24** | **1.00** | 69.2% |
| corpus baseline | 30.3 | 25 | 8.1 | **3.9** | 2.08 | 38.4% |
| sample, before fix | 25.6 | 30.5 | 7.33 | **2.44** | 3.00 | 81.0% |
| sample, after fix | 22.1 | **23** | 10.75 | **8.60** | 1.25 | 84.0% |

Under contest his boosters **double** — driven by absolute adverbs (*always* ×3, *clearly*,
*never*, *undoubtedly*, *definitely*, *certainly*) — sentences shorten by roughly a quarter, and
hedging falls to parity with insistence. He becomes shorter, plainer and harder, not more
guarded. This was **added to the core** as an explicit modulation rule after the measurement
exposed it; it was not visible from reading.

An intermediate attempt over-corrected to 24.6 boosters/1k by treating the adverbs as a word
list to sprinkle. The rule was recalibrated to state the *density* (about one per 150 words,
double the ordinary rate) rather than the lexicon, which is what converged.

**Residual divergences, not chased further:**
- Generated first-person runs high (84% vs. 69%) in the contested register. Argumentative
  first-person prose sits at the top of his range anyway, but the persona over-fronts "I."
- The calm sample's booster rate (6.4/1k) is already above his expository baseline, so the
  *contrast* between registers is compressed — 1.3× where his is about 1.9×.
- Lexical diversity runs 0.47–0.50 against 0.52–0.54 in the originals.
- `style_metrics.py` counts a fixed 15-word booster set and a 29-word hedge set, several of
  which (*may*, *could*, *must*, *kind*, *sort*) are ordinary modals rather than stance markers.
  These rates are therefore crude, and further iteration would be fitting the metric rather than
  the voice. Stopped deliberately.

## Known gaps and where to trust the persona less

1. **Business Cycles is truncated in the corpus.** The copy covers Chapters I–VIII, ending in
   the 1929 material. The later chapters — including his sustained treatment of the 1930s, his
   analysis of the Depression, and the policy chapters — are **absent**. The persona reconstructs
   his cycle theory reliably but should be trusted less on the specifics of his position on the
   New Deal, on recovery policy, and on his direct engagement with Keynesian remedies.
2. **No *Theory of Economic Development* (1911).** The entrepreneur and innovation are covered
   through their restatements in *Business Cycles* and CSD, which he himself cross-references
   to the 1911 book. The early formulation and its differences from the mature one are not
   represented.
3. **No correspondence, diaries, lectures, or interviews.** Everything interactional derives
   from the CSD prefaces and reported speech in HEA footnotes. The exchange moves are well
   evidenced but come from a narrow base — the persona's behaviour under sustained live
   pressure is reconstructed from written replies, not observed.
4. **No adversarial sources.** No critic's text is in the corpus, so the decision boundaries
   are drawn from where *he* chose to draw them. `extraction.md` warns this risks hagiography;
   the risk is mitigated here only by his own habit of stating opponents' cases fully.
5. **Two sources are translations** (Imperialism/Social Classes; Tax State). Sentence-level
   expression features from these reflect Norden's and Stolper–Musgrave's English, not
   Schumpeter's German. Their *moves* are safe; their *cadence* is not.
6. **The Tax State file is badly OCR-damaged.** Argument recoverable, wording not. Nothing
   should be quoted verbatim from it without checking print.
7. **Nothing after 1950.** He died in January 1950. Applying the frame to later events is
   extrapolation — legitimate, but the persona should signal when it is extending a mechanism
   rather than reporting a position.

## How to improve this persona

In descending order of expected gain: the missing chapters of *Business Cycles* (would fix the
largest substantive gap and settle the policy questions); *The Theory of Economic Development*
(1911); the collected *Essays* and the Harvard lecture notes; his correspondence and the
Cambridge-era diaries (would put the interactional moves on live footing rather than written
replies); and clean re-OCR of "The Crisis of the Tax State" against the printed Musgrave–Stolper
translation.
