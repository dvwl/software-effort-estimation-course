# Three-Point Estimation Guide

## Overview
Three-point estimation uses optimistic, pessimistic, and most likely estimates to calculate expected effort and assess uncertainty.

## Basic Formulas

### PERT Formula (Program Evaluation and Review Technique)
```
Expected Estimate = (O + 4M + P) / 6
```
Where:
- **O** = Optimistic estimate (best case)
- **M** = Most likely estimate (realistic case)  
- **P** = Pessimistic estimate (worst case)

### Triangular Distribution
```
Expected Estimate = (O + M + P) / 3
```

### Standard Deviation
```
Standard Deviation = (P - O) / 6
```

### Confidence Intervals
- **68% confidence**: Expected ± 1 Standard Deviation
- **95% confidence**: Expected ± 2 Standard Deviations  
- **99.7% confidence**: Expected ± 3 Standard Deviations

## Step-by-Step Process

### Step 1: Define Scenarios
| Scenario | Probability | Conditions |
|----------|-------------|------------|
| **Optimistic** | ~10% | Everything goes perfectly |
| **Most Likely** | ~60% | Normal development conditions |
| **Pessimistic** | ~10% | Major problems occur |

### Step 2: Gather Three Estimates
For each work package or feature:
1. **Optimistic (O)**: Minimal time if everything goes perfectly
2. **Most Likely (M)**: Realistic estimate under normal conditions
3. **Pessimistic (P)**: Maximum time if significant problems occur

### Step 3: Calculate Expected Values
Apply PERT or triangular distribution formula

### Step 4: Calculate Uncertainty
Determine standard deviation and confidence intervals

## Practical Examples

### Example 1: User Authentication Feature
- **Optimistic**: 3 days (perfect conditions)
- **Most Likely**: 5 days (normal development)
- **Pessimistic**: 10 days (major security issues)

**PERT Calculation:**
```
Expected = (3 + 4×5 + 10) / 6 = 33/6 = 5.5 days
Standard Deviation = (10 - 3) / 6 = 1.17 days
```

**Confidence Intervals:**
- 68% confidence: 5.5 ± 1.17 = 4.33 to 6.67 days
- 95% confidence: 5.5 ± 2.34 = 3.16 to 7.84 days

### Example 2: Database Integration
- **Optimistic**: 8 hours
- **Most Likely**: 16 hours  
- **Pessimistic**: 40 hours

**PERT Calculation:**
```
Expected = (8 + 4×16 + 40) / 6 = 112/6 = 18.67 hours
Standard Deviation = (40 - 8) / 6 = 5.33 hours
```

## Guidelines for Estimating

### Optimistic Estimate (O)
- Assume perfect conditions
- No interruptions or delays
- All dependencies available
- Team fully focused
- No rework required

### Most Likely Estimate (M)
- Normal working conditions
- Typical interruptions
- Some minor issues to resolve
- Average team productivity
- Minimal rework

### Pessimistic Estimate (P)
- Significant problems occur
- Key team members unavailable
- Major technical challenges
- Requirement changes
- Substantial rework needed

## Ratio Guidelines

### Typical Ratios
| Complexity | O:M:P Ratio | Example |
|------------|-------------|---------|
| **Simple tasks** | 1:1.5:2 | 2:3:4 days |
| **Average tasks** | 1:2:3 | 2:4:6 days |
| **Complex tasks** | 1:2:4 | 2:4:8 days |
| **High uncertainty** | 1:3:6 | 1:3:6 weeks |

### Warning Signs
- **P/O > 10**: Task too uncertain, break down further
- **M closer to O**: May be overly optimistic
- **M closer to P**: May be overly pessimistic

## Aggregating Estimates

### For Multiple Tasks
```
Total Expected = Sum of Individual Expected Values
Total Variance = Sum of Individual Variances
Total Standard Deviation = √(Total Variance)
```

### Project Level Example
| Task | O | M | P | Expected | Std Dev |
|------|---|---|---|----------|---------|
| Analysis | 5 | 8 | 15 | 8.7 | 1.67 |
| Design | 10 | 15 | 25 | 15.8 | 2.5 |
| Development | 20 | 35 | 60 | 36.7 | 6.67 |
| Testing | 8 | 12 | 20 | 12.7 | 2.0 |
| **Total** | **43** | **70** | **120** | **73.9** | **7.35** |

## Best Practices

### Estimation Quality
- Use historical data to calibrate estimates
- Have multiple people estimate independently
- Validate assumptions behind each estimate
- Document reasoning for future reference

### Team Involvement
- Include subject matter experts
- Consider different perspectives
- Use Delphi technique for consensus
- Review estimates regularly

### Risk Considerations
- Identify key assumptions
- Plan for pessimistic scenarios
- Build contingency based on uncertainty
- Monitor actuals vs estimates

## Common Pitfalls

### Estimation Errors
- Making all three estimates too similar
- Anchoring on the first estimate given
- Not considering external dependencies
- Ignoring team experience differences

### Process Mistakes
- Using arithmetic mean instead of PERT
- Not updating estimates as uncertainty reduces
- Treating expected value as commitment
- Ignoring confidence intervals

## Tools and Templates

### Simple Spreadsheet Formula
```excel
=ROUND((B2+4*C2+D2)/6,1)  // PERT expected value
=ROUND((D2-B2)/6,1)       // Standard deviation
```

### Monte Carlo Simulation
For complex projects, consider Monte Carlo simulation:
1. Define probability distributions for each task
2. Run thousands of simulations
3. Analyze results for confidence levels
4. Create realistic project schedules

### Integration with Agile
- Apply to user stories or epics
- Use for release planning
- Update estimates after each sprint
- Track estimation accuracy over time
