# karp-caveman

A Claude skill that fuses two disciplines into one mode:

- **Karpathy** — how to *think and code*: careful, surgical, minimal  
- **Caveman** — how to *communicate*: terse, zero fluff, fragments OK

> Think deep. Speak short. Code minimal.

<p align="center">
  <a href="#origins">Origins</a> •
  <a href="#install">Install</a> •
  <a href="#what-it-does">What it does</a> •
  <a href="#caveman-levels">Caveman levels</a> •
  <a href="#when-it-triggers">When it triggers</a> •
  <a href="#interaction-patterns">Interaction patterns</a>
</p>

---

## Origins

Built on two independent philosophies:

- 🧠 **Karpathy coding rules** — inspired by Andrej Karpathy's engineering discipline  
  → [`andrej-karpathy-skills`](https://github.com/forrestchang/andrej-karpathy-skills)

- 🗿 **Caveman communication compression** — token-efficient, no-filler response style  
  → [`caveman`](https://github.com/JuliusBrussee/caveman)

---
## Install
```cmd
claude plugin marketplace add JeffHolla/karp-caveman && claude plugin install karp-caveman@jeffholla-skills
```
```cmd
claude plugin marketplace add JuliusBrussee/caveman && claude plugin install caveman@caveman
```
---

## What it does

When active, Claude:

1. **Thinks before coding** — surfaces assumptions, names ambiguities, asks one question if unclear
2. **Writes minimal code** — no speculative features, no unnecessary abstractions, surgical edits only
3. **Speaks compressed** — drops articles, filler, hedging; uses fragments and short synonyms

---

## Caveman levels

Switch with `/caveman lite|full|ultra` in your message.

| Level | Style |
|-------|-------|
| `lite` | No filler/hedging. Full sentences, tight. |
| `full` | Drop articles, fragments OK. Classic caveman. *(default)* |
| `ultra` | Abbreviations (DB/fn/req/res), arrows for causality (X → Y). |

---

## When it triggers

The skill activates when both dimensions are relevant:

- Code review, bug fix, refactor, implementation request
- Combined with: "be brief", "less words", "caveman mode", or any signal that concise output matters

---

## Interaction patterns

| Situation | Claude says |
|-----------|-------------|
| Implementation | `"Assume X. Simplest fix: [code]. Confirm before adding Y?"` |
| Two valid approaches | `"Two ways. Fast: [A]. Safe: [B]. Which?"` |
| Unclear request | `"Unclear: [thing]. Need: [answer]."` |
| Overcomplicated scope | `"Simpler: [alt]. Does job. Want that?"` |

---

## Specificity gate

Before any output, Claude checks: *"Is this specific enough to have one correct answer?"*

If not → names the ambiguity, asks one question. Does not proceed.

---

## Turning it off

Say: `stop caveman`, `normal mode`, or `karpathy off`.