# Quick Start Guide

Get started with the Career Path Analysis Tool in 5 minutes.

## Setup

```bash
git clone https://github.com/neardaniel-pls/near-work-analysis.git
cd near-work-analysis

pip install -r requirements.txt
```

## Run the Analysis

```bash
jupyter notebook career-path-analysis.ipynb
```

Run all cells to see the default analysis with 8 career roles.

## Customize for Yourself

In the "Personal Inputs" section of the notebook, update:

1. **`my_weights`** — Adjust weights for each criterion based on what matters to you
2. **`my_current_skills`** — Set your proficiency level (0-10) for each tool/technology
3. **`min_acceptable_salary`** — Set your minimum salary threshold
4. **`priority_*` values** — Adjust fit/salary/speed-to-hire priorities (must sum to 1.0)

## Next Steps

- [Career Analysis Guide](guides/career-analysis-guide.md) — Full methodology explained
- [FAQ](FAQ.md) — Common questions

---

**Last Updated**: 2026-05-25
