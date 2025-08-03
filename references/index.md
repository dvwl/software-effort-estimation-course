---
layout: default
title: References
nav_order: 6
has_children: true
permalink: /references/
---

# Quick Reference Guides

Essential reference materials, cheat sheets, and quick lookup guides for software estimation techniques and best practices.

## Quick Reference Cards

### Estimation Methods
- [**COCOMO Quick Reference**](cocomo-reference.md) - Models, formulas, and adjustment factors
- [**Function Points Cheat Sheet**](function-points-cheat-sheet.md) - Classification rules and complexity factors
- [**Use Case Points Guide**](use-case-points-guide.md) - Step-by-step calculation process
- [**Three-Point Estimation**](three-point-estimation-guide.md) - PERT and Beta distribution formulas

### Best Practices
- [**Estimation Checklist**](estimation-checklist.md) - Quality assurance for estimates
- [**Common Pitfalls**](common-pitfalls.md) - What to avoid and how to prevent errors
- [**Risk Factors**](risk-factors.md) - Comprehensive risk assessment guide
- [**Team Productivity Factors**](productivity-factors.md) - Factors affecting development speed

### Industry Data
- [**Productivity Benchmarks**](productivity-benchmarks.md) - Industry-standard productivity rates
- [**Technology Comparison**](technology-comparison.md) - Development speed by language/platform
- [**Project Type Multipliers**](project-type-multipliers.md) - Adjustment factors by project category

## Quick Lookup Tables

### COCOMO Constants

| Model | a | b | c | d |
|-------|---|---|---|---|
| Organic | 3.2 | 1.05 | 2.5 | 0.38 |
| Semi-detached | 3.0 | 1.12 | 2.5 | 0.35 |
| Embedded | 2.8 | 1.20 | 2.5 | 0.32 |

### Function Point Weights

| Component | Simple | Average | Complex |
|-----------|--------|---------|---------|
| External Input (EI) | 3 | 4 | 6 |
| External Output (EO) | 4 | 5 | 7 |
| External Inquiry (EQ) | 3 | 4 | 6 |
| Internal Logical File (ILF) | 7 | 10 | 15 |
| External Interface File (EIF) | 5 | 7 | 10 |

### Programming Language Productivity

| Language | LOC per Day | LOC per Function Point |
|----------|-------------|----------------------|
| Assembly | 25-50 | 320 |
| C | 75-150 | 128 |
| C++ | 100-200 | 64 |
| Java | 150-300 | 53 |
| C# | 150-300 | 53 |
| Python | 200-400 | 32 |
| JavaScript | 200-400 | 47 |
| Go | 175-350 | 42 |

## Conversion Tables

### Time Units
- 1 person-month = 160-180 hours (depending on organization)
- 1 person-year = 1,800-2,000 hours (accounting for holidays, training)
- 1 sprint (2 weeks) = 80 hours per person
- 1 iteration (4 weeks) = 160 hours per person

### Effort Distribution (Typical)
- Requirements: 10-15%
- Design: 15-20%
- Implementation: 40-50%
- Testing: 20-25%
- Deployment: 5-10%

## Decision Trees

### Estimation Method Selection

```
Is this a new development project?
├─ Yes → Do you have clear functional requirements?
│  ├─ Yes → Use Function Points or Use Case Points
│  └─ No → Use Analogy-based or Expert Judgment
└─ No → Is this similar to past projects?
   ├─ Yes → Use Analogy-based estimation
   └─ No → Use bottom-up estimation with high contingency
```

### Risk Assessment

```
Project Size (Function Points)
├─ < 100 FP → Low complexity baseline
├─ 100-500 FP → Medium complexity
├─ 500-1000 FP → High complexity
└─ > 1000 FP → Very high complexity, consider breaking down
```

## Templates & Forms

### Quick Estimation Form

**Project**: ________________  
**Estimator**: ________________  
**Date**: ________________  

**Size Metrics**:
- Function Points: ________
- Use Case Points: ________
- Lines of Code: ________

**Effort Estimates**:
- Optimistic: ________ hours
- Most Likely: ________ hours  
- Pessimistic: ________ hours
- Expected (PERT): ________ hours

**Risk Factors** (Rate 1-5):
- Requirements clarity: ____
- Technology familiarity: ____
- Team experience: ____
- Schedule pressure: ____
- Integration complexity: ____

**Contingency**: ________% (Recommended: 15-40%)  
**Final Estimate**: ________ hours  

## Formulas & Calculations

### Three-Point Estimation (PERT)
```
Expected Time = (Optimistic + 4 × Most Likely + Pessimistic) ÷ 6
Standard Deviation = (Pessimistic - Optimistic) ÷ 6
Variance = (Standard Deviation)²
```

### COCOMO Basic Model
```
Effort = a × (KLOC)^b person-months
Development Time = c × (Effort)^d months
People = Effort ÷ Development Time
```

### Function Points Calculation
```
UFP = (EI × 3-6) + (EO × 4-7) + (EQ × 3-6) + (ILF × 7-15) + (EIF × 5-10)
VAF = 0.65 + (0.01 × TDI)
AFP = UFP × VAF
```

## Contact & Support

For questions about these references or suggestions for additional content:
- Course materials: Available during training session
- Online resources: Updated regularly on this site
- Community: Join discussions in course forums

---

*These references are designed for quick lookup during estimation activities. For detailed explanations, refer to the full course modules and exercises.*
