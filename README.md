# THE SOVEREIGN LATTICE™ — On-Device Qwen3.5-4B VLM
**MICHELLE™** · by LeVander Little

> A Qwen3.5-4B VLM running **W8A16 on a Galaxy S24+ Hexagon NPU** — vision tower **removed and branched to the GPU backend** (two-graph split). We solved the **RoPE cos/sin + rotate_half shape problem** that breaks Qwen QNN export — the wall most developers hit.

## ✅ Proven (real hardware)
- **~54 tok/s prefill** on physical Galaxy S24+ (SM8650, Hexagon v75), W8A16
- 5-bin context-binary chain, vision tower FP16 on Adreno GPU
- Compiled on Blackwell sm_120 (CUDA 13) — full env pinned

## 🧠 What it does
On-device multi-domain reasoning — **8,710 reasoning permutations** spanning finance, signal analysis, display, acoustics, and open-source intelligence.

## 🔒 Gated
Weights, the QNN/RoPE methodology, and the permutation corpus are **private**. The public proof + reproduction recipe are here. **[Request access →](https://github.com/levlbars/michelle-sovereign-vault/issues)** to license the techniques.

## 📊 Live demo
→ **https://levlbars.github.io/michelle-sovereign-vault/**

---
© 2026 LeVander Little. THE SOVEREIGN LATTICE™ and MICHELLE™ are trademarks. All rights reserved.
