# Changelog

All notable changes to this skill are documented here.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Planned
- Fold in the missing chapters of *Business Cycles* (IX onward) — the largest substantive gap; would settle his position on the Depression, recovery policy, and the Keynesian remedies
- Fold in *The Theory of Economic Development* (1911) for the early formulation of innovation and the entrepreneur, and the differences from the mature version
- Correspondence, diaries, and lecture notes, if available — would put the interactional moves on live footing instead of written replies to critics
- Clean re-OCR of "The Crisis of the Tax State" against the printed Stolper–Musgrave translation
- Adversarial sources (contemporary critics) to test where the decision boundaries actually lie rather than where he drew them

## [1.1.0] — 2026-08-06

A second distillation pass over the same five sources. No new corpus, no change to the cluster
structure, no element cut.

### Added
- **`references/voice.md`** — the standing expressive module, missing from 1.0.0. Eight
  construction rules with attested fragments; a measured avoid-list (zero contractions, zero
  *arguably*, zero *firstly*, zero *I would argue* in 1.14M words); five modulation rules stated
  with absolute target bands rather than directions; a register-range table; the metaphor-domain
  inventory; attested opening and closing moves; the full measured baseline plus per-register
  segments; and six anti-drift pairs
- A **generation-targets table** (four registers × five features, each against its matched
  original) so a draft can be checked against the register it is in, never against the corpus
  aggregate
- `SKILL.md`'s loading block now instructs the host agent to load `voice.md` before sustained prose

### Changed
- **All five cluster modules deepened**, from ~1,500–1,900 tokens each to ~2,200–3,900. Same five
  files, same partition, same headings — the additions are inside them and are itemized in
  `provenance.md` under "Second-pass additions." Highlights: the falsifiability clause and the
  displaced third-person self-reference in *Business Cycles*; the democracy demolition restored to
  its three numbered steps in CSD; four named diagnostic constructs surfaced from the *History*
  (Classical Situation, the Ricardian Vice, the Art of Triviality, the Great Gap); the four-step
  economic argument in "The Sociology of Imperialisms"; and the theoretical limit of the tax state
  stated as a principle
- `README.md` structure and size figures updated

### Distillation notes
- **New modulation finding.** The contested register is not "the prefaces" — it is *being charged*.
  Measured separately, the 1949 preface (declining to advise England) moves opposite to the 1946
  preface (answering charges) on every axis: sentences lengthen to 33.8 against 27.0, and hedging
  outruns insistence 5:1 against parity. 1.0.0 had no rule separating deference from defence
- **Style-match test failed once and forced three new rules.** The first samples came out with the
  two registers *inverted* — the expository passage carried the contested profile and the contested
  passage read as staccato rebuttal at a sentence mean of 18.1. A direction with no bound gets
  followed until it runs out, so `voice.md` gained a floor under the contested register, an explicit
  reciprocal target for the expository one, and a second-person guard. Re-verified: sentence shape
  within ~2 words of the matched originals in both registers, zero avoid-list violations, and a
  register contrast of 5× on hedge:booster where 1.0.0 managed a compressed 1.3× in the wrong
  direction
- Residual ratio overshoot of about one notch in each register was **not** chased further; five
  iterations oscillated rather than converged, which is the signature of fitting
  `style_metrics.py`'s fixed modal lists rather than the voice
- The core's "shorten by about a quarter" is exact against the genre-matched exposition baseline
  (21%) and loose against the corpus aggregate (11%); `voice.md` states the absolute target instead,
  and the core line was left standing

### Known follow-up
- The four constructs newly surfaced in `c09–c10` belong in `frameworks.md` as well; they are
  defined in the cluster module for now

## [1.0.0] — 2026-08-01

### Added
- Core `SKILL.md` — 16 cost-bearing refusals, 13 projectible regularities, 9 interactional moves, 3 modulation patterns, 3 preoccupations; front-loaded, no meta or hedging language in the body
- `references/frameworks.md` — 13 named constructs in his exact senses: creative destruction, innovation vs. invention, the entrepreneurial function, Horizon, credit creation, the three-cycle schema, equilibrium and the internal/external cut, Vision and ideological bias, the three fundamental fields, the two kinds of progress, imperialism as atavism, class function, the tax state, the classical vs. competitive theories of democracy
- Five cluster files, one per source work, with register profiles and evidence
- `references/episodic.md` — demoted and secondary material, plus editorial artifacts of the posthumous *History of Economic Analysis*
- `references/provenance.md` — coverage map, weight vector, full core-element ledger, measured per-work style modulation, both fidelity gates, and seven documented gaps

### Distillation notes
- Weights auto-adjusted for a near-monologic corpus (dialogue ratio ~0.03): interactional 0.15→0.12, projectibility 0.30→0.33
- 51 elements scored, 45 to core, 6 demoted; style cap left 8 of 9 available slots unused
- Projection gate passed without re-curation. Blind arm 8/8 (4 items from unread passages, correct stance and reasoning on all four); seeded arm 12/12 with one item excluded for leakage and the whole arm discounted for prior exposure
- Cost gate: 16 of 16 attested divergence pairs present in the core; minimum-presence assertion passed
- Style-match test failed twice and forced two revisions of "How I sound": the build rule was too vague to steer generation (samples came out at sentence mean 19.4 against 30.3), and the contested-register rule was **substantively wrong** — measurement against the CSD 2nd-edition preface showed his boosters double and his sentences shorten under attack, where the rules had implied he grows more careful. Both corrected and re-verified; residual divergences logged in `provenance.md`
