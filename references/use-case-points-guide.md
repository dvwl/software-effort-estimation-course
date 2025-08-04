---
layout: default
title: Use Case Points Guide
parent: References
nav_order: 6
---

# Use Case Points (UCP) Guide

## Overview
Use Case Points is a software estimation technique that calculates project effort based on use cases and complexity factors.

## Step-by-Step Calculation Process

### Step 1: Count Unadjusted Use Case Points (UUCP)

#### Use Case Complexity Classification

| Type | Description | Weight |
|------|-------------|--------|
| **Simple** | 1-3 transactions | 5 |
| **Average** | 4-7 transactions | 10 |
| **Complex** | 8+ transactions | 15 |

#### Actor Complexity Classification

| Type | Description | Weight |
|------|-------------|--------|
| **Simple** | System interface (API) | 1 |
| **Average** | Protocol interface (HTTP, database) | 2 |
| **Complex** | Human user interface (GUI) | 3 |

#### UUCP Calculation
```
UUCP = (Use Case Points) + (Actor Points)
```

### Step 2: Apply Technical Complexity Factor (TCF)

#### Technical Factors

| Factor | Description | Weight | Rating (0-5) |
|--------|-------------|--------|--------------|
| T1 | Distributed system | 2 | |
| T2 | Response time/performance | 2 | |
| T3 | End-user efficiency | 1 | |
| T4 | Complex internal processing | 1 | |
| T5 | Reusable code | 1 | |
| T6 | Easy to install | 0.5 | |
| T7 | Easy to use | 0.5 | |
| T8 | Portable to other platforms | 2 | |
| T9 | Easy to change | 1 | |
| T10 | Concurrent users | 1 | |
| T11 | Security features | 1 | |
| T12 | Access for third parties | 1 | |
| T13 | Training needs | 1 | |

#### TCF Calculation
```
TFactor = Sum of (Weight × Rating)
TCF = 0.6 + (0.01 × TFactor)
```

### Step 3: Apply Environmental Complexity Factor (ECF)

#### Environmental Factors

| Factor | Description | Weight | Rating (0-5) |
|--------|-------------|--------|--------------|
| E1 | Familiar with development process | 1.5 | |
| E2 | Application experience | 0.5 | |
| E3 | Object-oriented experience | 1 | |
| E4 | Lead analyst capability | 0.5 | |
| E5 | Motivation | 1 | |
| E6 | Stable requirements | 2 | |
| E7 | Part-time staff | -1 | |
| E8 | Difficult programming language | -1 | |

#### ECF Calculation
```
EFactor = Sum of (Weight × Rating)
ECF = 1.4 + (-0.03 × EFactor)
```

### Step 4: Calculate Use Case Points
```
UCP = UUCP × TCF × ECF
```

### Step 5: Convert to Effort
```
Person-Hours = UCP × Productivity Factor
```

#### Productivity Factor Guidelines

| Project Type | Hours per UCP |
|--------------|---------------|
| Simple project | 20 |
| Average project | 28 |
| Complex project | 36 |

## Quick Reference Example

### Sample Project
- 5 Simple Use Cases (5 × 5 = 25)
- 8 Average Use Cases (8 × 10 = 80) 
- 3 Complex Use Cases (3 × 15 = 45)
- 2 Simple Actors (2 × 1 = 2)
- 3 Average Actors (3 × 2 = 6)
- 1 Complex Actor (1 × 3 = 3)

**UUCP = 25 + 80 + 45 + 2 + 6 + 3 = 161**

### Technical Factors (Example)
- T1=3, T2=4, T3=3, T4=2, T5=3, T6=2, T7=3, T8=1, T9=3, T10=4, T11=3, T12=1, T13=2
- TFactor = (2×3)+(2×4)+(1×3)+(1×2)+(1×3)+(0.5×2)+(0.5×3)+(2×1)+(1×3)+(1×4)+(1×3)+(1×1)+(1×2) = 39
- **TCF = 0.6 + (0.01 × 39) = 0.99**

### Environmental Factors (Example)
- E1=4, E2=3, E3=3, E4=3, E5=4, E6=2, E7=1, E8=2
- EFactor = (1.5×4)+(0.5×3)+(1×3)+(0.5×3)+(1×4)+(2×2)+(-1×1)+(-1×2) = 18.5
- **ECF = 1.4 + (-0.03 × 18.5) = 0.845**

### Final Calculation
```
UCP = 161 × 0.99 × 0.845 = 135 Use Case Points
Effort = 135 × 28 = 3,780 person-hours
```

## Best Practices

### Accuracy Tips
- Have experienced analysts classify use cases
- Be consistent in complexity classification
- Review ratings with the development team
- Consider project-specific productivity factors

### Common Pitfalls
- Inconsistent use case granularity
- Overly optimistic environmental ratings
- Ignoring project-specific factors
- Not updating estimates as requirements evolve

### Validation
- Compare with historical project data
- Cross-check with other estimation methods
- Review complexity ratings regularly
- Adjust productivity factors based on team experience

## Integration with Other Methods

### Use Case Points + COCOMO
1. Use UCP for initial sizing
2. Apply COCOMO adjustments for technology
3. Combine for more robust estimates

### Use Case Points + Planning Poker
1. Use UCP for baseline estimates
2. Validate with team planning poker sessions
3. Reconcile differences through discussion
