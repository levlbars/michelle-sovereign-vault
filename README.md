# THE SOVEREIGN LATTICE™ — On-Device Qwen3.5-4B VLM
**MICHELLE™** · by LeVander Little

> A Qwen3.5-4B VLM running **W8A16 on a Galaxy S24+ Hexagon NPU** — vision tower branched to the GPU backend as a separate FP16 graph (two-graph split, never rejoined). Proven end-to-end from Blackwell sm_120 training to on-device Hexagon HTP inference.

## Proven (real hardware)
- **~54 tok/s prefill** on physical Galaxy S24+ (SM8650, Hexagon v75), W8A16
- 5-bin context-binary chain, vision tower FP16 on Adreno GPU
- Compiled on Blackwell sm_120 (CUDA 13) — full env pinned in FORGE_VENV.lock

## What it does
On-device multi-domain intelligence — **8,710 reasoning permutations** spanning finance, signal analysis, display, acoustics, and open-source intelligence. All running privately, at the edge, without a cloud call.

## Gated
Weights, the QNN methodology, tower-split compiler, and permutation corpus are **private**. The public proof + reproduction recipe are on the site. **[Request access](https://github.com/levlbars/michelle-sovereign-vault/issues)** to license the techniques.

## Live demo
**https://levlbars.github.io/michelle-sovereign-vault/**

---
© 2026 LeVander Little. THE SOVEREIGN LATTICE™ and MICHELLE™ are trademarks. All rights reserved.
