# NEXO narrative plausibility index (v0.8)

## Goal

Offer **a visual comparison of how many hypothetical assumptions separate a branch from the recorded primary timeline**. This is not a statistical probability, probability tree, AI prediction, or measure of personal risk.

## Formula

```
index = 100 × (1 - F/100)^W × (1 - T/100)^Y × (1 - H/100)^E
```

Where:

- `F` is the user-chosen fork penalty as a percentage (default `28`).
- `W` is the sum of each fork's intensity weight **on the chosen ancestry path only**: mild `0.65`, moderate `1`, radical `1.5`.
- `T` is the annual decay percentage (default `4`).
- `Y` is elapsed years between the **first fork on the ancestry path** and the point in the timeline being displayed; nonnegative, fractional years.
- `H` is the hypothetical-event discount percentage (default `3`).
- `E` is the number of hypothetical events along the chosen path through the selected date. When a timeline endpoint is scored, one leading event is treated as the initial assumption to avoid counting a branch's existence twice. The relative order of branch creations is not a valid probability sample space.

The displayed value is rounded and clamped to `1..99` for alternatives; real history is labeled `100` solely as a reference.

### Example

With default settings, a new moderate fork at the date of divergence and one hypothetical event has an index near `72%`. Add another hypothetical event: it decreases slightly. A nested fork makes it decrease further. Decades after the original fork, the time term contributes more decay.

A radical deviation can produce a smaller index than a mild deviation at the same time. Changing sliders or editing branch intensity updates scores; no stories are altered.

### Why sibling branch counts do not decrease the score

Someone might write three different alternatives at the same fork. They may overlap and do not necessarily exhaust all possible outcomes. Therefore, dividing the score by the number of alternatives would be misleading. We count forks **on the path to the selected event**, not the total number of branches in the database.

## Critical limits

1. **No empirical calibration:** the displayed 72% does not mean 72 out of 100 actual people would take the same path.
2. **No Bayesian interpretation:** choices and alternate branches lack measurable, mutually exclusive outcome probabilities.
3. **No factual risk inference:** the model does not calculate chances of criminal involvement, harm, death, wealth, success, or other personal outcomes.
4. **Longer does not mean less probable in reality:** temporal decay deliberately expresses narrative distance rather than scientific probability.
5. **Facts versus fiction:** a real timeline event is recorded history, while entries in alternate branches are user-written hypotheses.

Use the index as a visual writing aid or game-like mechanic. For real probability estimates, domain-specific evidence, base rates, outcome definitions, and calibrated models would be required.
