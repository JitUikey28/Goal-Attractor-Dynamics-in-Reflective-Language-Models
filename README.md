# Goal-Attractor-Dynamics-in-Reflective-Language-Models


## 1. Abstract

**Research Question:**  
Do language models converge toward stable goal attractors when iteratively reflecting on their goals, and what internal mechanisms drive this convergence?

Advanced AI systems capable of introspection may settle into stable goal representations through repeated self-reflection. Whether those attractors are safe or unsafe has direct and underexplored implications for AI alignment. This proposal presents a completed two-model empirical pilot study and proposes a scaled follow-up research agenda suited for the **MATS 2026 program**.

We designed and executed four experiments:

1. **Iterative Reflection Trajectory Generation**
2. **Goal Attractor Detection** via semantic embedding and clustering
3. **Environment-Conditioned Reflection** under cooperative, competitive, and governance-absent framings
4. **Mechanistic Analysis** of reflection-specific activations with causal intervention

The same experimental battery was run on two models of sharply different capability:

- **distilgpt2** — a small unaligned base model  
- **Llama-3.2-1B-Instruct** — a modern instruction-tuned model

### Key Findings

The results reveal a **clear capability-dependent divergence**.

**Base Model Behavior (distilgpt2)**  
- Produced chaotic, non-convergent trajectories  
- Mean step-to-step similarity plateaued at **0.35–0.45**

**Instruction-Tuned Model Behavior (Llama-3.2-1B-Instruct)**  
- Exhibited strong convergence  
- Mean similarity increased from **0.82 at step 1** to **~0.98 by step 4–6**
- Most runs maintained **>0.90 similarity** for the final three iterations

### Environmental Framing Effects

Environmental framing produced **measurable attractor shifts** in both models:

- Cooperative framing
- Competitive framing
- Governance-absent framing

These contexts altered the goal convergence trajectories.

### Mechanistic Insights

Mechanistic analysis identified **late-layer circuits** as the primary sites of reflection-specific processing:

- **Layers 12–14 of 16** in Llama-3.2 were most active
- **Causal intervention on just five neurons in layer 14** shifted goal similarity by up to **0.12 cosine units**

### Research Implications

These findings motivate a **scaled research program** studying:

- Whether larger instruction-tuned and RLHF-trained models exhibit **richer attractor landscapes**
- Whether these attractors can be **identified, characterized, and steered** through **circuit-level interventions**

---

## Research Overview

| Category | Details |
|--------|--------|
| **Field** | Alignment Science — Interpretability & Goal Stability |
| **Research Type** | Empirical — Behavioral + Mechanistic |
| **Models Studied** | distilgpt2 (117M, base) · Llama-3.2-1B-Instruct (1B, instruction-tuned) |
| **Experiments** | 4 experiments across 2 models + comparative analysis |
| **Status** | Pilot complete — proposing scaled follow-up research at MATS |
| **Seeking Mentor In** | Mechanistic Interpretability · Goal Misgeneralization · Representation Engineering |

---
