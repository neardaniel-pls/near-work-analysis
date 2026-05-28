# Frequently Asked Questions

## General

### Is this specific to the Portuguese market?
Salary data is based on the Portuguese market (EUR). You can adjust salary values in the notebook for other markets.

### Can I add my own career roles?
Yes. See the [Career Analysis Guide](guides/career-analysis-guide.md) for instructions on adding new roles.

## Analysis

### How are fit scores calculated?
Each role has 9 attributes scored 1-10. Your personal weights are applied to calculate a weighted fit score. Higher = better match.

### What is the ultimate score?
A weighted combination of three normalized metrics:
- **Fit Score** (default 60%): How well the role matches your preferences
- **Salary** (default 20%): Normalized salary relative to other roles
- **Speed to Hire** (default 20%): How quickly you could get hired

### What is the learning gap?
Points representing how much you need to learn for each role. It's based on the difference between required tool proficiency and your current skill levels. Lower = less learning needed.

## Customization

### How do I change the weights?
Edit `my_weights` in the notebook's "Personal Inputs" section. Each weight corresponds to one of the 9 attributes.

### How do I add a new tool?
1. Add the tool to `tools_data` with associated roles
2. Add it to `tool_profile` with pain (0-10) and reward (0-10) scores
3. Add it to `my_current_skills` with your proficiency level

---

**Last Updated**: 2026-05-25
