---
hide:
  - navigation
  - toc
---

# OmniSenter

**A multi-stage agentic MoE with the Ohm self-evolution engine.**<br>
Built on Darwin Family weight-space recombination. Auxiliary to Hermes Agent.

<div class="tow-badge">TOWARDS SELF-IMPROVEMENT</div>

---

<div class="hero">
  <h1>OMNISENTER</h1>
  <p class="tagline">Multimodal · Agentic · Self-Evolving</p>
</div>

![Cosmic convergence: three streams of text, audio, and image flowing into a single bright point of memory.](assets/images/synesthesia-concept.png){.hero-image}

---

## The Omni Family

A naming convention that ties together:

- **Omni** — multimodal native (text + vision + audio + video + music)
- **Senter** — Omni with the **agentic core** wired in (function calling,
  tool use, the notebook)
- **Ohm** — the **self-evolution engine** (CMA-ES background loop, atomic
  weight swap, strict improvement acceptance)
- **Senter Ohm** — the **flagship** ~32B-total / 8B-active MoE with all
  three composited

[Read the naming post →](blog/the-omni-family.md){.md-button}

---

## The flagship

**Senter Ohm** is a ~32B total / 8B active sparse-upcycled MoE with the
Ohm self-evolution engine bundled in. The 256K context window is for
**the notebook** — the structured state object that flows between Senter
Ohm and Hermes Agent.

| | |
|---|---|
| **Total params** | ~32B |
| **Active per token** | ~8B (top-1 routing) |
| **Context** | 256K (YaRN-extended) |
| **Modalities** | text + vision + audio + video + music |
| **Self-evolution** | continuous, background, strict-acceptance |
| **Inference VRAM** | ~22GB at 4-bit Q4_K_M (1× RTX 3090) |

[Read the flagship post →](blog/senter-ohm-flagship.md){.md-button}
[Read the math post →](blog/senter-ohm-32a8b-math.md){.md-button}

---

## The build

A 5-stage pipeline takes an 8B base to the 32B flagship:

1. **Agentic SFT** (QLoRA on 34K convs) → 8B Senter
2. **Evolutionary merge** (CMA-ES across 3 variants) → 8B merged
3. **Sparse upcycle to MoE** → 32B MoE with 8B active
4. **256K YaRN context** → long-context SFT
5. **Plugin + Notebook + Ohm wiring** → deployable `.ohm` bundle

[Read the pipeline post →](blog/the-5-stage-pipeline.md){.md-button}

---

## The new ideas

**Synthesia** — every notebook entry indexed as a joint `(text, audio,
image)` embedding. Recall by sound, by image, or by text. 10 concrete
benefits. [Read it →](blog/the-synthesia-layer.md){.md-button}

**Ohm** — the model file *is* the engine. Background CMA-ES loop, atomic
weight swap, strict-acceptance. The model never serves worse outputs.
[Read it →](blog/the-ohm-runtime.md){.md-button}

---

## Current state (transitional)

The models currently published on HuggingFace under `sovthpaw/` are the
**v1 lineage**:

- [`sovthpaw/omnistep-12a3b`](https://huggingface.co/sovthpaw/omnistep-12a3b) — 12B total / 3B active, multimodal (the OmniStep baseline)
- [`sovthpaw/Omni-Senter-3B`](https://huggingface.co/sovthpaw/Omni-Senter-3B) — 3B early Senter
- [`sovthpaw/OmniSenter-Base-16B`](https://huggingface.co/sovthpaw/OmniSenter-Base-16B) — 16B base (Qwen3-8B + Cosmos3-Nano)

The new architecture (Senter Ohm 32A8B, OmniSenter 12B, OmniSenterStep)
will **replace** these as it ships. Foundation, not destination.

[Browse all 13 blog posts →](blog/index.md){.md-button .md-button--primary}
[Browse the wiki →](wiki/index.md){.md-button}

---

<div class="tow-callout">TOWARDS SELF-IMPROVEMENT</div>
