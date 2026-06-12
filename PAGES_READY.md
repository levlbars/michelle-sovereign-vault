# PAGES_READY — PUBLIC_STAGING build summary (2026-06-12)

## Guard result
`bash release_guard.sh PUBLIC_STAGING` → EXIT 0, 0 leak signals.
No keys, tokens, PII, weights, or methodology exposed.

## Files in PUBLIC_STAGING

| File | Purpose |
|---|---|
| `index.html` | Main GitHub Pages landing — hero, interactive benchmark charts, env collapsibles, recipe timeline, access CTA |
| `model-card.html` | HuggingFace-style model card — spec table, benchmark table, architecture, version pins, limitations |
| `PAGES_READY.md` | This file (can be removed before push) |

## Free tools used (all CDN, no paid services)

| Tool | Version | Role | Source |
|---|---|---|---|
| Chart.js | 4.4.3 | Interactive benchmark bar charts | https://www.chartjs.org · MIT |
| highlight.js | 11.9.0 | Code block syntax highlighting | https://highlightjs.org · BSD-3 |
| GitHub Pages | free | Static hosting | https://pages.github.com |
| HuggingFace Spaces (static) | free | Model card hosting | https://huggingface.co/spaces |

No Node.js build step required. All CDN assets loaded from `cdn.jsdelivr.net`.

## IP gate status

GATED (not in PUBLIC_STAGING, will NOT ship):
- Model weights (*.bin, *.safetensors, *.dlc, *.gguf)
- 16_SOVEREIGN_DISTILL_HONEST.py / 17_QNN_STAGE_HONEST.py
- LANE compiler configs (LANE_A, LANE_B, LANE_C)
- MONOLITH_* orchestration scripts
- SOVEREIGN_METHODOLOGY.md
- tower-split details, W8A16 quantization path, AIMET encoding patch logic
- FORGE_VENV.lock full contents (key pins shown only)

PUBLIC (proof tier — in pages):
- Real S24+ benchmark numbers with honest caveats
- Hardware specs (device model, GPU, NPU)
- Blackwell sm_120 + causal-conv1d achievement
- Key version pins (10 packages shown)
- Architecture description (two-graph split, W8A16 LM + FP16 tower)
- Reproduction RECIPE (what, not how)
- Free tools list with citations
- Access request CTA (GitHub Issues URL, no email in page source)

## Contact / CTA

Access requests use a GitHub Issues link (`levander-little/michelle-vlm`) — no email address
in page source. Before publishing, update the GitHub URL to the real repo path if different.

## Push commands

### GitHub Pages (repo root or docs/ branch)

```bash
# Option A: push PUBLIC_STAGING contents as repo root
cd /workspace/MICHELLE_SOVEREIGN_VAULT/PUBLIC_STAGING
git init
git remote add origin https://github.com/<YOUR_USERNAME>/<REPO>.git
git checkout -b gh-pages
git add index.html model-card.html
git commit -m "Launch public proof pages"
git push -u origin gh-pages

# Option B: copy into existing repo's docs/ folder
cp /workspace/MICHELLE_SOVEREIGN_VAULT/PUBLIC_STAGING/index.html <REPO>/docs/
cp /workspace/MICHELLE_SOVEREIGN_VAULT/PUBLIC_STAGING/model-card.html <REPO>/docs/
# Then in GitHub repo settings: Pages -> Source -> /docs
```

### HuggingFace Spaces (static HTML)

```bash
# Create a new Space of type "static" on HuggingFace, then:
git clone https://huggingface.co/spaces/<YOUR_HF_USERNAME>/<SPACE_NAME>
cp /workspace/MICHELLE_SOVEREIGN_VAULT/PUBLIC_STAGING/index.html <SPACE_NAME>/
cp /workspace/MICHELLE_SOVEREIGN_VAULT/PUBLIC_STAGING/model-card.html <SPACE_NAME>/
cd <SPACE_NAME>
git add .
git commit -m "Launch MICHELLE proof pages"
git push
```

### Final guard re-check (run before every push)

```bash
bash /workspace/MICHELLE_SOVEREIGN_VAULT/release_guard.sh /workspace/MICHELLE_SOVEREIGN_VAULT/PUBLIC_STAGING
```
