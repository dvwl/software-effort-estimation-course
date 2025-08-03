---
layout: default
title: Module 2 - Approaches to Software Estimation
parent: Exercises
nav_order: 2
---

# Module 2: Approaches to Software Estimation
{: .no_toc }

**Duration**: 115 minutes (10:35am - 12:30pm)
{: .label .label-blue }

This module explores various approaches to software estimation, focusing on analogy-based estimation, software size estimation techniques, and selecting appropriate methods for different project types.

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
- Select appropriate estimation approaches based on project characteristics
- Apply analogy-based estimation using historical project data
- Calculate software size using Lines of Code (LOC), Use Case Points, and Function Points
- Understand when to use gross vs. detailed estimation approaches
- Combine multiple estimation techniques for improved accuracy

---

## Quick Exercise 2.1: Function Point Analysis (30 minutes)

### Background
You're estimating a **Document Management System** for a law firm.

**System Requirements:**
- Document upload and storage
- Document search and retrieval
- User access control and permissions
- Document versioning and history
- Basic reporting (usage statistics)
- Integration with email system

### Task 1: Count Function Points (20 minutes)

Identify and classify the main functions:

#### External Inputs (EI) - Users entering data
| Function | Complexity | Weight | Count | Total FP |
|----------|------------|--------|-------|----------|
| Document Upload | Average | 4 | 1 | 4 |
| User Registration | Simple | 3 | 1 | 3 |
| Permission Settings | Complex | 6 | 1 | 6 |
| **EI Subtotal** | | | | **13** |

#### External Outputs (EO) - Reports and displays
| Function | Complexity | Weight | Count | Total FP |
|----------|------------|--------|-------|----------|
| Usage Reports | Average | 5 | 1 | |
| Document List | Simple | 4 | 1 | |
| **EO Subtotal** | | | | **___** |

#### External Inquiries (EQ) - Search functions
| Function | Complexity | Weight | Count | Total FP |
|----------|------------|--------|-------|----------|
| Document Search | Average | 4 | 1 | |
| User Lookup | Simple | 3 | 1 | |
| **EQ Subtotal** | | | | **___** |

#### Internal Files (ILF) - Data stored by system
| Function | Complexity | Weight | Count | Total FP |
|----------|------------|--------|-------|----------|
| Document Repository | Complex | 15 | 1 | |
| User Profiles | Simple | 7 | 1 | |
| **ILF Subtotal** | | | | **___** |

#### External Files (EIF) - Data from other systems
| Function | Complexity | Weight | Count | Total FP |
|----------|------------|--------|-------|----------|
| Email System | Simple | 5 | 1 | |
| **EIF Subtotal** | | | | **___** |

**Total Unadjusted Function Points**: _____ FP

### Task 2: Convert to Effort Estimate (10 minutes)

Using productivity rate of **12 FP per person-month** for web applications:

**Estimated Effort**: _____ FP ÷ 12 FP/PM = _____ person-months

**With 25% contingency**: _____ PM × 1.25 = _____ person-months

---

## Advanced Exercise 2.2: Analogical Estimation (35 minutes)
{: .label .label-purple }

*For participants who complete the quick exercise early*

### Background
Use historical project data to estimate a **Mobile Banking App**.

**Historical Projects:**
| Project | Type | Size (KLOC) | Team | Duration | Effort (PM) |
|---------|------|-------------|------|----------|-------------|
| **Web Banking** | Financial | 45 | 6 | 10 months | 48 |
| **Mobile Shopping** | E-commerce | 35 | 5 | 8 months | 32 |
| **Insurance Portal** | Financial | 52 | 7 | 12 months | 65 |
| **Mobile Wallet** | FinTech | 28 | 4 | 6 months | 20 |

**New Project: Mobile Banking App**
- Estimated size: 40 KLOC
- Team: 5 developers
- Technology: React Native, Node.js
- Complexity: High (security, compliance)

### Task 1: Similarity Analysis (15 minutes)

Rate similarity to new project (1-10 scale):

| Historical Project | Technology Match | Size Match | Complexity Match | Team Match | Overall Similarity |
|-------------------|------------------|------------|------------------|------------|-------------------|
| Web Banking | 7 (same domain) | 9 (45 vs 40) | 9 (high security) | 8 (6 vs 5) | |
| Mobile Shopping | 8 (mobile) | 8 (35 vs 40) | 6 (lower complexity) | 10 (5 vs 5) | |
| Insurance Portal | 6 (financial) | 7 (52 vs 40) | 8 (compliance) | 7 (7 vs 5) | |
| Mobile Wallet | 9 (FinTech mobile) | 6 (28 vs 40) | 9 (security) | 9 (4 vs 5) | |

### Task 2: Calculate Analogical Estimates (20 minutes)

#### Method 1: Most Similar Project
**Selected**: ________________
**Direct scaling**: _____ PM × (40 KLOC / _____ KLOC) = _____ PM

#### Method 2: Weighted Average (Top 3)
| Project | Weight | Historical PM | Size Ratio | Adjusted PM |
|---------|--------|---------------|------------|-------------|
| 1st: _____ | ___/10 | _____ | 40/_____ | _____ |
| 2nd: _____ | ___/10 | _____ | 40/_____ | _____ |
| 3rd: _____ | ___/10 | _____ | 40/_____ | _____ |

**Weighted Average**: _____ PM

**Final Estimate Range**: _____ to _____ person-months

---

## Module 2 Summary

### Key Takeaways

1. **Function Points**: Size-independent measurement based on user functionality
2. **Analogical Estimation**: Most reliable when you have similar, recent projects
3. **Multiple Methods**: Cross-check estimates using different approaches
4. **Similarity Matters**: Technology, domain, and team experience affect accuracy

### Quick Reference

**Function Point Weights:**
- External Inputs: Simple=3, Average=4, Complex=6
- External Outputs: Simple=4, Average=5, Complex=7  
- External Inquiries: Simple=3, Average=4, Complex=6
- Internal Files: Simple=7, Average=10, Complex=15
- External Files: Simple=5, Average=7, Complex=10

**Analogical Estimation:**
- ✅ Use projects within last 2-3 years
- ✅ Consider technology similarity
- ✅ Adjust for team experience differences
- ✅ Account for complexity variations

### Next Steps

Continue to [Module 3: Development Effort and Cost Estimation](../module3/) to learn about COCOMO and cost calculations.


