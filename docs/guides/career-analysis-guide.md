# Career Analysis Guide

Complete guide to the Career Path Analysis Tool — methodology, customization, and interpretation.

## Methodology

### 1. Data Definition
Each career role is defined with:
- **9 attributes** scored 1-10 (higher is better unless noted)
- **Salary**: Average junior gross annual salary (EUR, Portuguese market)
- **Required tools**: List of tools/technologies with proficiency requirements

### 2. Attribute Definitions

| Attribute | Description | Scale |
|-----------|-------------|-------|
| Stability | Job security and market demand | 1 (low) - 10 (high) |
| Visual Output | Amount of visual/deliverable output | 1 (low) - 10 (high) |
| Work-Life Balance | Expected balance between work and personal life | 1 (poor) - 10 (excellent) |
| Innovation | Opportunity for creative/innovative work | 1 (low) - 10 (high) |
| Remote-Friendly | Suitability for remote work | 1 (office-only) - 10 (fully remote) |
| Math Intensity | Level of mathematical complexity | 1 (minimal) - 10 (heavy math) |
| Entry Difficulty | How hard to break into the field | 1 (easy) - 10 (very hard) |
| Customer-Facing | Amount of direct client interaction | 1 (none) - 10 (constant) |
| Growth Potential | Career growth and advancement opportunities | 1 (limited) - 10 (excellent) |

### 3. Personal Inputs

#### Weights (`my_weights`)
Set importance (0-1) for each attribute. Higher weight = more important in the fit score calculation.

#### Current Skills (`my_current_skills`)
Rate your proficiency (0-10) for each tool/technology. Used to calculate learning gaps.

#### Priorities
Three weights that must sum to 1.0:
- **Fit priority** (default: 0.6): Weight of the fit score
- **Money priority** (default: 0.2): Weight of the salary score
- **Speed priority** (default: 0.2): Weight of the speed-to-hire score

### 4. Scoring Algorithm

1. **Fit Score**: Weighted sum of role attributes × personal weights
2. **Learning Gap**: Sum of (required proficiency - current skill) for each tool
3. **Salary Check**: Filter roles below minimum acceptable salary
4. **Ultimate Score**: Normalized combination of fit, salary, and speed

## Supported Roles

| Role | Description |
|------|-------------|
| Data Analyst | Analyze data, create reports and dashboards |
| Data Engineer | Build and maintain data pipelines and infrastructure |
| BI Developer | Create business intelligence solutions and dashboards |
| Database Admin (DBA) | Manage and optimize database systems |
| Crypto Developer | Develop blockchain and cryptocurrency applications |
| Product Manager | Define product strategy and coordinate teams |
| Analytics Engineer | Transform data and build analytical models |
| Technical Writer | Create technical documentation and guides |

## Visualizations

1. **The Money**: Bar chart of salaries for qualifying roles
2. **The Love**: Bar chart of fit scores showing job compatibility
3. **The Effort**: Bar chart of learning gap points (lower is better)
4. **The Strategy Matrix**: Scatter plot showing effort vs reward
5. **Final Decision**: Ultimate ranking with best career path highlighted

## Customization

### Adding a New Role
```python
data["New Role"] = {
    "stability": 7,
    "visual_output": 5,
    "work_life_balance": 6,
    "innovation": 8,
    "remote_friendly": 9,
    "math_intensity": 4,
    "entry_difficulty": 6,
    "customer_facing": 3,
    "growth_potential": 7,
    "avg_junior_salary": 25000,
}
```

### Adding a New Tool
```python
tools_data["New Tool"] = ["Role 1", "Role 2"]
tool_profile["New Tool"] = {"pain": 5, "reward": 7}
my_current_skills["New Tool"] = 3
```

## Tips

- Start with the default weights, then adjust based on what matters most
- Be honest about your current skill levels for accurate gap analysis
- The strategy matrix helps identify "easy wins" (high reward, low effort)
- Run the analysis multiple times with different priorities to explore scenarios

---

[Back to Documentation](../README.md)
