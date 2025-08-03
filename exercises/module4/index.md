---
layout: default
title: Module 4 - Testing and Schedule Estimation
parent: Exercises
nav_order: 4
---

# Module 4: Testing and Schedule Estimation
{: .no_toc }

**Duration**: 55 minutes (02:35pm - 03:30pm)
{: .label .label-blue }

This final module focuses on estimating testing effort and creating realistic project schedules.

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
- Estimate testing effort based on project complexity
- Create realistic schedules with dependency management
- Apply schedule optimization techniques

---

## Quick Exercise 4.1: Testing Effort Estimation (25 minutes)

### Background
Testing typically represents 25-40% of total project effort but is often underestimated. This exercise provides practical approaches to testing estimation.

### Project: Customer Portal Web Application
- **Development Effort**: 3,200 hours
- **Technology**: React frontend, Node.js backend, PostgreSQL
- **Complexity**: Medium (business application with integrations)
- **Quality Requirements**: Standard business application

### Task 1: Testing Effort Calculation (15 minutes)

#### Method 1: Percentage of Development Effort

| Application Type | Testing % of Development |
|------------------|-------------------------|
| **Business Web Apps** | 25-35% |
| **E-commerce** | 30-40% |
| **Financial Systems** | 40-50% |
| **Safety-Critical** | 50-100% |

**Assessment:**
- Application Type: ________________
- Development Effort: 3,200 hours
- Testing Percentage: _______%
- **Testing Effort**: _____ hours

#### Method 2: By Testing Type

| Testing Type | % of Total Testing | Hours | Notes |
|--------------|-------------------|-------|-------|
| **Unit Testing** | 25% | _____ | Developer responsibility |
| **Integration Testing** | 20% | _____ | API and database testing |
| **System Testing** | 30% | _____ | End-to-end functionality |
| **User Acceptance Testing** | 15% | _____ | Business stakeholder testing |
| **Performance Testing** | 10% | _____ | Load and stress testing |

**Total Testing Effort**: _____ hours

### Task 2: Test Planning (10 minutes)

Plan test execution phases:

| Phase | Duration (weeks) | Effort (hours) | Key Activities |
|-------|------------------|----------------|----------------|
| **Test Planning** | 1 | _____ | Test strategy, case design |
| **Test Execution** | 4 | _____ | Execute test cases, log defects |
| **Defect Resolution** | 2 | _____ | Fix bugs, regression testing |
| **Final Validation** | 1 | _____ | Final smoke tests, sign-off |

**Total Test Schedule**: _____ weeks

---

## Advanced Exercise 4.2: Project Schedule Development (30 minutes)

### Background
Creating realistic schedules requires understanding task dependencies, resource constraints, and critical path management.

### Project: Mobile Banking App
- **Total Effort**: 4,800 hours
- **Team Size**: 8 people
- **Phases**: Planning, Development, Testing, Deployment

### Task 1: Work Breakdown Structure (15 minutes)

Break down the project into phases and estimate effort distribution:

| Phase | Effort % | Hours | Duration (weeks) | Team Members |
|-------|----------|-------|------------------|--------------|
| **Requirements & Design** | 20% | _____ | _____ | BA, Architect, Designer |
| **Frontend Development** | 35% | _____ | _____ | Frontend developers |
| **Backend Development** | 25% | _____ | _____ | Backend developers |
| **Testing & QA** | 15% | _____ | _____ | QA engineers |
| **Deployment & Support** | 5% | _____ | _____ | DevOps, Support |

**Total Project**: _____ hours over _____ weeks

### Task 2: Critical Path and Dependencies (15 minutes)

Map key dependencies and calculate critical path:

```
Phase Dependencies:
- Requirements → Design → Development
- Frontend Development ← → Backend Development
- Development → Testing
- Testing → Deployment

Critical Path Analysis:
```

| Task | Duration | Depends On | Earliest Start | Earliest Finish |
|------|----------|------------|----------------|-----------------|
| Requirements | 2 weeks | - | Week 1 | Week 2 |
| Design | 2 weeks | Requirements | Week 3 | Week 4 |
| Backend Dev | 6 weeks | Design | Week 5 | Week 10 |
| Frontend Dev | 5 weeks | Design | Week 5 | Week 9 |
| Integration | 1 week | Both Dev | Week 11 | Week 11 |
| Testing | 3 weeks | Integration | Week 12 | Week 14 |
| Deployment | 1 week | Testing | Week 15 | Week 15 |

**Critical Path**: _____ → _____ → _____ → _____ → _____
**Project Duration**: _____ weeks

### Task 3: Schedule Optimization (10 minutes)

Apply techniques to compress the schedule:

| Technique | Application | Time Saved | Cost Impact |
|-----------|-------------|------------|-------------|
| **Fast Tracking** | Overlap testing with development | _____ weeks | Low |
| **Crashing** | Add more developers | _____ weeks | High |
| **Scope Reduction** | Move features to Phase 2 | _____ weeks | Medium |

**Optimized Schedule**: _____ weeks (reduction of _____ weeks)

---

## Module 4 Summary

### Key Takeaways

1. **Testing is Substantial**: Plan for 25-40% of development effort for testing
2. **Dependencies Drive Schedule**: Critical path determines minimum project duration
3. **Optimization Has Trade-offs**: Faster delivery often means higher cost or reduced scope
4. **Realistic Planning Essential**: Account for all phases, not just development

### Best Practices Checklist

- [ ] Estimate testing effort based on project complexity and quality requirements
- [ ] Map all task dependencies before creating schedules
- [ ] Identify the critical path and monitor it closely
- [ ] Plan for schedule buffers and contingencies
- [ ] Consider multiple optimization strategies

### Course Completion

Congratulations! You have completed the PC2544 Software Effort Estimation course. You now have practical tools and techniques for:

- Creating work breakdown structures
- Applying multiple estimation techniques
- Converting size estimates to effort and cost
- Planning testing and project schedules

### Next Steps

- Apply these techniques to your current projects
- Build a database of historical estimation data
- Continuously refine your estimation accuracy
- Share lessons learned with your team

---

## Additional Resources

- [Testing Effort Calculator (Excel)](../../tools/testing-effort-calculator.xlsx)
- [Project Schedule Template](../../tools/project-schedule-template.xlsx)
- [Critical Path Analysis Worksheet](../../tools/critical-path-worksheet.xlsx)
- [Estimation Summary Checklist](../../references/estimation-checklist.md)

*Estimated completion time: 55 minutes*

*Estimated completion time: 55 minutes*

---

## Course Evaluation

Please provide feedback on the course content and exercises:

1. **Most Valuable Module**: ________________
2. **Most Challenging Concept**: ________________  
3. **Suggested Improvements**: ________________
4. **Overall Rating** (1-5): ______

*Thank you for completing the Software Effort Estimation course!*
