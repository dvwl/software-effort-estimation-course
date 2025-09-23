---
layout: default
title: Module 3 - Development Effort and Cost
parent: Exercises
nav_order: 3
---

# Module 3: Development Effort and Cost Estimation
{: .no_toc }

**Duration**: 105 minutes (01:30pm - 03:15pm)
{: .label .label-blue }

This module focuses on converting size estimates into effort and cost projections using established models and techniques.

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

---

## Learning Objectives

By the end of this module, you will be able to:
- Apply the COCOMO model for effort estimation
- Perform task-based estimation with confidence intervals
- Assess developer productivity factors
- Calculate project costs including overhead and contingency
- Compare different estimation approaches for accuracy

---

## Quick Exercise 3.1: COCOMO Model Application (30 minutes)

### Background
The Constructive Cost Model (COCOMO) provides a systematic approach to effort estimation using project size and complexity factors.

### Project: E-commerce Web Application
- **Size**: 25 KSLOC (thousands of lines of code)
- **Type**: Web application with moderate complexity
- **Team**: Mixed experience level

### Task 1: Basic COCOMO Calculation (15 minutes)

**Basic COCOMO Formula:** Effort = a × (Size)^b

| Project Mode | a | b | When to Use |
|--------------|---|---|-------------|
| **Organic** | 2.4 | 1.05 | Small teams, familiar technology |
| **Semi-detached** | 3.0 | 1.12 | Medium teams, mixed experience |
| **Embedded** | 3.6 | 1.20 | Complex systems, tight constraints |

**Your Assessment:**
1. Project mode for e-commerce web app: ________________
2. Effort calculation: _____ × (25)^_____ = _____ person-months
3. Convert to hours: _____ PM × 152 hours/PM = _____ hours

### Task 2: Effort Adjustments (15 minutes)

Apply key adjustment factors to your base estimate:

| Factor | Low (0.8x) | Normal (1.0x) | High (1.3x) | Your Rating |
|--------|------------|---------------|-------------|-------------|
| **Product Complexity** | Simple forms | Standard e-commerce | Advanced features | |
| **Team Experience** | Junior team | Mixed experience | Senior team | |
| **Development Tools** | Basic tools | Standard IDE | Advanced tools | |
| **Time Constraints** | Relaxed | Normal | Tight deadline | |

**Adjustment Calculation:**
- Base Effort: _____ hours
- Combined Multiplier: _____ × _____ × _____ × _____ = _____
- **Adjusted Effort**: _____ hours × _____ = _____ hours

---

## Advanced Exercise 3.2: Cost Estimation and Budgeting (30 minutes)

### Background
Convert effort estimates into comprehensive project costs including all components and contingencies.

### Project Team Structure

| Role | Count | Rate ($/hour) | Allocation % | Hours | Cost |
|------|-------|---------------|--------------|-------|------|
| **Project Manager** | 1 | $90 | 100% | | $ |
| **Senior Developer** | 2 | $85 | 100% | | $ |
| **Mid-level Developer** | 2 | $65 | 100% | | $ |
| **QA Engineer** | 1 | $60 | 100% | | $ |
| **UI/UX Designer** | 1 | $70 | 50% | | $ |

**Total Direct Labor**: $__________

### Task 1: Indirect Costs (10 minutes)

| Cost Category | Calculation | Amount |
|---------------|-------------|--------|
| **Benefits & Taxes** | 25% of labor | $ |
| **Equipment/Software** | $1,500 per person | $ |
| **Overhead** | 20% of total | $ |

**Total Project Cost**: $__________

### Task 2: Risk and Contingency (10 minutes)

Assess project risk level and apply contingency:

| Risk Factor | Low | Medium | High | Assessment |
|-------------|-----|--------|------|------------|
| **Technology Risk** | Known tech | Some new tech | Bleeding edge | |
| **Team Risk** | Stable team | Some changes | New team | |
| **Requirements Risk** | Clear/stable | Some changes | Evolving | |

**Contingency Percentage**: _____% (10% low, 20% medium, 35% high)
**Contingency Amount**: $__________
**Final Budget**: $__________

### Task 3: Budget Phasing (10 minutes)

Distribute budget across project phases:

| Phase | Duration | Effort % | Budget | Key Deliverables |
|-------|----------|----------|--------|------------------|
| **Planning & Design** | 3 weeks | 20% | $ | Requirements, architecture |
| **Development** | 8 weeks | 60% | $ | Code, unit tests |
| **Testing & Deployment** | 3 weeks | 20% | $ | QA, production setup |

**Total Project Duration**: _____ weeks

---

## Module 3 Summary

### Key Takeaways

1. **COCOMO Provides Structure**: Systematic approach to effort estimation with clear adjustment factors
2. **Costs Extend Beyond Development**: Include overhead, infrastructure, and contingency planning
3. **Risk Assessment Drives Contingency**: Higher risk projects need larger buffers
4. **Team Rates Vary Significantly**: Account for different skill levels and experience

### Best Practices Checklist

- [ ] Apply COCOMO or similar parametric models for baseline estimates
- [ ] Include all cost components, not just development effort
- [ ] Apply appropriate contingency based on project risk level
- [ ] Phase budget distribution to manage cash flow
- [ ] Document assumptions and methods used

### Next Steps

Continue to [Module 4: Testing and Schedule Estimation](../module4/) to learn about estimating testing effort and creating realistic project schedules.

---

## Additional Resources

- [COCOMO Calculator (Excel)](../../tools/cocomo-calculator.xlsx)
- [Cost Planning Worksheet](../../tools/cost-planning-worksheet.xlsx)
- [Budget Template](../../tools/budget-template.xlsx)

*Estimated completion time: 60 minutes*
