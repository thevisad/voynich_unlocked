# Voynich Unlocked
### Structural Analysis of the Voynich Manuscript

---

> **This is not a decipherment.** It is a demonstration that the manuscript contains a consistent, measurable, non-random structural system — and that this system must be explained.

---

| Field | Detail |
|---|---|
| Status | Active Research |
| Corpus | 37,671 tokens · 226 folios (EVA transcription) |
| Focus | Structural analysis — not translation |
| Release | March 2026 |

---

## What Was Found

The Voynich corpus is best modeled as a **three-role structural system**, not a flat sequence of words.

```
[ Role A ]  ──operator──>  [ Role B ]  ──>  [ Role C ]
 Variable      (2 families,    Operator        Terminal
               mutually        Slot            Outcome
               exclusive)
```

**The two operator families never co-occur in the same structural slot.**
This holds without exception across the entire corpus.

---

## Key Results at a Glance

### Operator Differentiation

For every testable context word (Role A), the two operators route the outcome (Role C) to completely different distributions:

| Metric | Value |
|---|---|
| Contexts tested | 43 word-family · 60 cluster-level |
| Mean JS divergence | **0.838** (word-family) · **0.845** (cluster) |
| Range | \[0.48 → 1.00\] |
| Near-identical outcomes (JS < 0.05) | **0 / 43** |
| High-divergence outcomes (JS > 0.30) | **43 / 43** |

> JS divergence = 0 means the operators produce identical outcomes.
> JS divergence = 1 means completely different outcomes.
> Null models (shuffled/randomized corpus) score below 0.1.

---

### Two-Tier Encoding

| Layer | Value |
|---|---|
| Unique surface word types | 8,231 |
| Unique structural patterns | 836 |
| Compression ratio | **9.84×** |
| Entropy reduction | **33.9%** (3.54 bits) |

The manuscript's surface complexity conceals a far smaller structural inventory. Folios with near-identical structural profiles (JS = 0.094) share only ~20% of their surface words — **structure is more stable than lexicon**.

---

### Non-Commutative Operator Chains

Order matters. The system is not linear:

| Transition | Entropy Change | Count |
|---|---|---|
| A → B | +2.708 bits | 631 |
| B → A | +3.524 bits | 315 |
| B → B | **−1.512 bits** (collapse) | 327 |
| A → A | +0.443 bits | 20 |

B→B is the only combination that *reduces* entropy — consistent with a structured compositional system, not a substitution cipher or random process.

---

### Null Model Rejection

Tested against three model classes:

- Random token shuffling
- Bigram-preserving Markov models
- Frequency-matched substitution models

**Observed JS ≈ 0.8–1.0.** All null models collapse to **JS < 0.1**.
The observed behavior does not reproduce under any null model.

---

## What This Does NOT Claim

```
NOT claimed                         IS established
──────────────────────────────────  ────────────────────────────────────
A decipherment                      Internal structural regularity
A translation                       Operator mutual exclusion
A known language mapping            Non-random, context-dependent behavior
Any semantic referent               Functionally distinct operator roles
Any known writing system match      Non-commutative operator chaining
```

---

## Visual Evidence

The JS divergence histogram is the clearest summary of the finding:

![JS Divergence Distribution](js_divergence_histogram.png)

*Each bar = one context word (Role A). All 43 bars score > 0.48 — far above where null models score. The operators are doing different things across the entire corpus.*

---

## Reproducibility

You can independently verify these claims using the public EVA interlinear transcription:

1. Compute operator co-occurrence distributions (Role B mutual exclusion)
2. Measure conditional distributions P(C | A, operator) for each Role A context
3. Calculate Jensen-Shannon divergence across the 43 qualifying contexts
4. Compare entropy between the surface-word layer and structural-pattern layer

**If you can reproduce JS ≈ 0.838 across 43 contexts under a null model — that directly challenges this work.**

---

## Full Community Findings

The detailed methodology notes, full metric tables, and peer review invitation are in the companion document:

### [Community Findings Release →](community_findings.md)

Includes:
- Complete validation metric tables (Sections 2.1–2.7)
- Latent state cluster analysis (60 clusters)
- Null model robustness discussion
- Invitation for independent replication and challenge

---

## Contributing / Review

We welcome:
- Independent replication attempts
- Statistical critiques
- Null model challenges
- Alternative structural interpretations

Open an issue or submit a pull request.

---

## License

TBD — MIT or research-use license recommended.

---

*All metrics derived from the publicly available EVA interlinear transcription of the Voynich manuscript. No external data sources used.*
