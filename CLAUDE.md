# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is a reading club resource repository for **Hands-On Large Language Models** (Jay Alammar & Maarten Grootendorst). It stores slides, discussion notes, and Jupyter Notebooks for weekly sessions held every Sunday at 20:00.

## Structure

Each chapter lives in its own folder (e.g., `ch1/`, `ch2/`) containing:
- `README.md` — chapter resources, links, and notes
- `Chapter_N_*.ipynb` — official book notebook (unmodified)
- `Chapter_N_*_twinkleai_version.ipynb` — TwinkleAI customized version using `twinkle-ai/gemma-3-4B-T1-it`
- `*.pdf` — slide deck for the session

## Notebooks

Notebooks are designed to run on **GPU** (Google Colab T4 or equivalent). Key dependencies:

```bash
pip install transformers>=4.50.0 accelerate>=0.31.0
```

The TwinkleAI notebooks use the custom model `twinkle-ai/gemma-3-4B-T1-it` (requires HF token with access). Load pattern:

```python
from transformers import AutoModelForCausalLM, AutoTokenizer, pipeline

model = AutoModelForCausalLM.from_pretrained("twinkle-ai/gemma-3-4B-T1-it", device_map="cuda", torch_dtype="auto")
tokenizer = AutoTokenizer.from_pretrained("twinkle-ai/gemma-3-4B-T1-it")
generator = pipeline("text-generation", model=model, tokenizer=tokenizer, ...)
```

## Adding a New Chapter

1. Create `chN/` directory with `README.md` (follow `ch1/README.md` as template).
2. Add the banner image at the top: `![TwinkleAI Reading Club Banner](../images/TwinkleAI_Reading_Club_00800_x_320_px.png)`
3. Update the chapter table in the root `README.md` with date, description, and resource links.
4. Mark completed chapters with `- [x]` and upcoming with `- [ ]`.
