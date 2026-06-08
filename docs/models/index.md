---
title: Models
---

# Models

The Omni Family — every model, named, with current status.

<div class="tow-badge">TOWARDS SELF-IMPROVEMENT</div>

---

## Naming refresher

- **Omni** = multimodal native (text + vision + audio + video + music)
- **Senter** = Omni with the **agentic core** wired in
- **Ohm** = the **self-evolution engine**
- **Senter Ohm** = the flagship ~32A8B MoE (all three composited)
- **OmniSenter** = the **project** (umbrella), also the small Senter (`OmniSenter 12B`)

[Read the full naming post →](../blog/the-omni-family.md)

---

## Transitional v1 (currently on HuggingFace)

These are the published v1 models. The new architecture will replace them.

### [OmniStep 12A3B](https://huggingface.co/sovthpaw/omnistep-12a3b) — 12B total / 3B active

The published multimodal baseline. Darwin-merged from Qwen2.5-Omni-3B +
ACE-Step v1.5 XL 4B DiT. 4 GGUFs + 4 safetensors shards.

| Quant | Size | VRAM |
|---|---|---|
| F16 | 6.4GB | 6.4GB |
| Q8_0 | 3.4GB | 3.4GB |
| **Q4_K_M** | **2.0GB** | **2.0GB** ← recommended |
| Q4_0 | 1.9GB | 1.9GB |

[→ View on HuggingFace](https://huggingface.co/sovthpaw/omnistep-12a3b){.md-button}

### [Omni-Senter 3B](https://huggingface.co/sovthpaw/Omni-Senter-3B) — 3B

The early Senter. LoRA + GGUF. Predecessor of [OmniSenter 12B](../wiki/entities/omnisenter-12b.md).

[→ View on HuggingFace](https://huggingface.co/sovthpaw/Omni-Senter-3B){.md-button}

### [OmniSenter-Base 16B](https://huggingface.co/sovthpaw/OmniSenter-Base-16B) — 16B

The 16B base. Qwen3-8B + Cosmos3-Nano Darwin merge. Multimodal
(vision + audio + video). 7 safetensors shards.

[→ View on HuggingFace](https://huggingface.co/sovthpaw/OmniSenter-Base-16B){.md-button}

---

## Planned (the new architecture)

These will be built and published as the 5-stage pipeline completes.

### OmniSenter 12B — the small Senter

~12B active, dense, function-calling + omnimodal fusion. The
**shipping target** for routine use.

[→ Wiki page](../wiki/entities/omnisenter-12b.md)

### OmniSenterStep (Omni SS) — + music

OmniSenter + AceStep Darwin fusion. The most capable single model short
of the flagship.

[→ Wiki page](../wiki/entities/omnisenterstep.md)

### Senter Ohm 32A8B — the flagship

~32B total / 8B active MoE with the Ohm self-evolution engine bundled
in. The destination.

[→ Wiki page](../wiki/entities/senter-ohm-32a8b.md) ·
[→ Flagship blog post](../blog/senter-ohm-flagship.md)

---

## Local (on the rig)

| Model | GPU | Port |
|---|---|---|
| Darwin-28B (Q4_K_M) | GPU 0 | `:11401` |
| APEX-MTP I-Compact (speculative-decode partner) | GPU 1 | `:11401` |

See [Darwin-28B wiki page](../wiki/entities/darwin-28b.md) for details.

---

<div class="tow-callout">TOWARDS SELF-IMPROVEMENT</div>
