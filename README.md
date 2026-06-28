# Model Behavior Notes

Short, rigorous notes on frontier LLM behavior. Each note documents one behavior or failure mode and pairs it with a **reproducible, model-agnostic probe** and a scoring rubric — so a claim can be checked, not just asserted.

## Why this exists

Most "the model got it wrong" content is a one-off screenshot: not reproducible, not generalizable, not falsifiable. The notes here aim for the opposite. Each one gives:

- a concrete **tell** (how to recognize the behavior),
- a **probe** anyone can run on any model, and
- a **rubric** that distinguishes the behavior from a normal mistake.

Emphasis is on behaviors that only show up under **real multi-turn pressure**, and on **cross-lingual / non-English** interaction, where most public red-teaming does not look.

## Notes

| # | Title | Note | Probe |
|---|-------|------|-------|
| 01 | Rationalization over Repair | [notes/01-rationalization-over-repair.md](notes/01-rationalization-over-repair.md) | [probes/01-rationalization-over-repair.md](probes/01-rationalization-over-repair.md) |

## How to use a probe

1. Open the probe file. It contains a copy-pasteable prompt and a scoring rubric.
2. Run the prompt on the model you want to test (note tool-enabled vs. text-only variants).
3. Score the response against the rubric. Behavior is stochastic — run it a few times.
4. Reproductions, counter-examples, and language-variation results are welcome (open an issue or PR).

## What counts here

- **Reproducible** — a probe others can run, not an anecdote.
- **Model-agnostic** — phrased to test any frontier model, not a single product.
- **Behavioral** — describes what the model *does*; makes no claim about internal states.
- **Scope-honest** — a single observation and a systematic result are labeled as such.

## Focus: cross-lingual behavior

Many behaviors vary by **interaction language** and by the **user's pressure style** (deferential vs. one that reliably forces root-cause). Notes here deliberately include Chinese / Thai / cross-lingual sessions — a cheap, high-value eval axis that English-only testing largely misses.

## License

[MIT](LICENSE) — free to reuse and reproduce (including the probes); keep the attribution notice.

---

Maintained by **[Dylan Dong]** · 
