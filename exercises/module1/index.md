---
layout: default
title: Module 1 - Overview
parent: Exercises
nav_order: 1
---

# Module 1: Overview of Software Estimation
{: .no_toc }

**Duration**: 90 minutes (09:00am - 10:30am)
{: .label .label-blue }

This module introduces the fundamental concepts of software estimation, covering objectives, key considerations, and best practices.

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
- Identify key areas and objectives of software estimation
- Recognize common issues and pitfalls in estimation
- Create basic Work Breakdown Structures (WBS)
- Understand the impact of uncertainty on estimates
- Apply best practices for estimation activities

---

## Quick Exercise 1.1: Project WBS and Risk Assessment (25 minutes)

### Background
You're estimating a **Customer Portal Development** project for a mid-size company.

**Project Requirements:**
- User registration and login
- Customer dashboard with account info
- Order history and tracking
- Support ticket system
- Mobile-responsive design
- Integration with existing CRM

**Constraints:**
- 6-month timeline
- Team: 4 developers, 1 designer, 1 QA, 1 PM
- Fixed budget: $300,000

### Task 1: Create High-Level WBS (15 minutes)

Break down the project into major work packages:

```
1. Project Management & Setup
   1.1 _____________________
   1.2 _____________________

2. Analysis & Design  
   2.1 _____________________
   2.2 _____________________

3. Development
   3.1 _____________________
   3.2 _____________________
   3.3 _____________________

4. Testing & Deployment
   4.1 _____________________
   4.2 _____________________
```

### Task 2: Risk Identification (10 minutes)

Identify top 5 risks and their impact:

| Risk | Probability (H/M/L) | Impact (H/M/L) | Mitigation |
|------|-------------------|----------------|------------|
| 1. | | | |
| 2. | | | |
| 3. | | | |
| 4. | | | |
| 5. | | | |

**Quick Discussion:** Which work package has the highest risk?

---

## Advanced Exercise 1.2: Three-Point Estimation (15 minutes)
{: .label .label-purple }

*For participants who complete the quick exercise early*

### Background
Apply three-point estimation to the **Customer Portal Integration** component from the WBS above.

**Integration Requirements:**
- Connect to existing CRM system
- Real-time data synchronization  
- Error handling and retry logic
- Performance optimization

### Task: Estimate Integration Effort

Provide three estimates for the integration work:

| Estimate Type | Hours | Key Assumptions |
|---------------|-------|-----------------|
| **Optimistic (Best Case)** | | API documentation is complete, no surprises |
| **Most Likely (Expected)** | | Normal development with typical issues |
| **Pessimistic (Worst Case)** | | API issues, performance problems, rework |

**Calculate Expected Value:**
Expected = (Optimistic + 4 × Most Likely + Pessimistic) ÷ 6 = _____ hours

**Calculate Standard Deviation:**
σ = (Pessimistic - Optimistic) ÷ 6 = _____ hours

**Confidence Intervals:**
- 68% confident: _____ ± _____ hours
- 95% confident: _____ ± _____ hours

---

## Module 1 Summary

### Key Takeaways

1. **Start with WBS**: Break down work into manageable, estimable pieces
2. **Identify Risks Early**: Know what could go wrong before it does
3. **Use Three-Point Estimation**: Account for uncertainty with optimistic/pessimistic ranges
4. **Document Assumptions**: Make your thinking visible to others

### Quick Reference

**WBS Best Practices:**
- ✅ Each task should be 8-80 hours
- ✅ Clear deliverables for each work package
- ✅ No overlap between components
- ✅ All project work included

**Risk Management:**
- ✅ Identify risks early in estimation process
- ✅ Assess both probability and impact
- ✅ Plan mitigation strategies
- ✅ Add contingency buffers

### Next Steps

Continue to [Module 2: Approaches to Software Estimation](../module2/) to learn specific estimation techniques.

---

*Estimated completion time: 25 minutes (Quick) + 15 minutes (Advanced)*
