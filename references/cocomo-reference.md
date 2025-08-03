---
layout: default
title: COCOMO Quick Reference
parent: References
nav_order: 1
---

# COCOMO Quick Reference

Comprehensive reference for the Constructive Cost Model (COCOMO) family of estimation models.

## Basic COCOMO

### Model Equations
```
Effort (Person-Months) = a × (KLOC)^b
Duration (Months) = c × (Effort)^d
Team Size = Effort / Duration
```

### Project Types and Constants

| Project Mode | a | b | c | d | Description |
|--------------|---|---|---|---|-------------|
| **Organic** | 2.4 | 1.05 | 2.5 | 0.38 | Small teams, familiar problem |
| **Semi-detached** | 3.0 | 1.12 | 2.5 | 0.35 | Medium teams, mixed experience |
| **Embedded** | 3.6 | 1.20 | 2.5 | 0.32 | Complex systems, tight constraints |

### Project Mode Selection Criteria

**Organic Projects:**
- Team size: 2-8 people
- Application domain: Familiar
- Requirements: Stable and well-understood
- Environment: Stable tools and methods
- Examples: Business applications, data processing

**Semi-detached Projects:**
- Team size: 8-30 people
- Application domain: Mixed familiarity
- Requirements: Mix of familiar and new
- Environment: Some new tools/methods
- Examples: Operating systems, DBMS, complex web apps

**Embedded Projects:**
- Team size: Often > 30 people
- Application domain: Unprecedented
- Requirements: Complex, changing
- Environment: Tight hardware/software constraints
- Examples: Real-time systems, avionics, telecommunications

## Intermediate COCOMO

### Effort Multipliers

#### Product Attributes
| Attribute | Very Low | Low | Nominal | High | Very High | Extra High |
|-----------|----------|-----|---------|------|-----------|------------|
| **RELY** (Reliability) | 0.75 | 0.88 | 1.00 | 1.15 | 1.40 | - |
| **DATA** (Database Size) | - | 0.94 | 1.00 | 1.08 | 1.16 | - |
| **CPLX** (Complexity) | 0.70 | 0.85 | 1.00 | 1.15 | 1.30 | 1.65 |

#### Hardware Attributes
| Attribute | Very Low | Low | Nominal | High | Very High | Extra High |
|-----------|----------|-----|---------|------|-----------|------------|
| **TIME** (Execution Time) | - | - | 1.00 | 1.11 | 1.30 | 1.66 |
| **STOR** (Main Storage) | - | - | 1.00 | 1.06 | 1.21 | 1.56 |
| **VIRT** (Virtual Machine) | - | 0.87 | 1.00 | 1.15 | 1.30 | - |
| **TURN** (Turnaround Time) | - | 0.87 | 1.00 | 1.07 | 1.15 | - |

#### Personnel Attributes
| Attribute | Very Low | Low | Nominal | High | Very High |
|-----------|----------|-----|---------|------|-----------|
| **ACAP** (Analyst Capability) | 1.46 | 1.19 | 1.00 | 0.86 | 0.71 |
| **AEXP** (Applications Experience) | 1.29 | 1.13 | 1.00 | 0.91 | 0.82 |
| **PCAP** (Programmer Capability) | 1.42 | 1.17 | 1.00 | 0.86 | 0.70 |
| **VEXP** (Virtual Machine Experience) | 1.21 | 1.10 | 1.00 | 0.90 | - |
| **LEXP** (Language Experience) | 1.14 | 1.07 | 1.00 | 0.95 | - |

#### Project Attributes
| Attribute | Very Low | Low | Nominal | High | Very High |
|-----------|----------|-----|---------|------|-----------|
| **MODP** (Modern Practices) | 1.24 | 1.10 | 1.00 | 0.91 | 0.82 |
| **TOOL** (Software Tools) | 1.24 | 1.10 | 1.00 | 0.91 | 0.83 |
| **SCED** (Schedule Constraint) | 1.23 | 1.08 | 1.00 | 1.04 | 1.10 |

## COCOMO II

### Scale Factors
Used to calculate the scale exponent: E = B + 0.01 × Σ(Scale Factors)
where B = 0.91

| Scale Factor | Very Low | Low | Nominal | High | Very High |
|--------------|----------|-----|---------|------|-----------|
| **PREC** (Precedentedness) | 6.20 | 4.96 | 3.72 | 2.48 | 1.24 |
| **FLEX** (Development Flexibility) | 5.07 | 4.05 | 3.04 | 2.03 | 1.01 |
| **RESL** (Architecture Risk Resolution) | 7.07 | 5.65 | 4.24 | 2.83 | 1.41 |
| **TEAM** (Team Cohesion) | 5.48 | 4.38 | 3.29 | 2.19 | 1.10 |
| **PMAT** (Process Maturity) | 7.80 | 6.24 | 4.68 | 3.12 | 1.56 |

### COCOMO II Equation
```
Effort = A × (Size)^E × Π(EMi)
Duration = C × (Effort)^F
```
Where:
- A = 2.94 (calibration constant)
- Size = software size in KSLOC or unadjusted function points
- E = scale exponent
- EMi = effort multipliers
- C = 3.67 (schedule constant)
- F = D + 0.2 × (E - B) = D + 0.2 × (E - 0.91), where D = 0.28

### Effort Multipliers (COCOMO II)

#### Product Factors
| Factor | Very Low | Low | Nominal | High | Very High | Extra High |
|--------|----------|-----|---------|------|-----------|------------|
| **RELY** | 0.82 | 0.92 | 1.00 | 1.10 | 1.26 | - |
| **DATA** | - | 0.90 | 1.00 | 1.14 | 1.28 | - |
| **CPLX** | 0.73 | 0.87 | 1.00 | 1.17 | 1.34 | 1.74 |
| **RUSE** | - | 0.95 | 1.00 | 1.07 | 1.15 | 1.24 |
| **DOCU** | 0.81 | 0.91 | 1.00 | 1.11 | 1.23 | - |

#### Platform Factors
| Factor | Very Low | Low | Nominal | High | Very High | Extra High |
|--------|----------|-----|---------|------|-----------|------------|
| **TIME** | - | - | 1.00 | 1.11 | 1.29 | 1.63 |
| **STOR** | - | - | 1.00 | 1.05 | 1.17 | 1.46 |
| **PVOL** | - | 0.87 | 1.00 | 1.15 | 1.30 | - |

#### Personnel Factors
| Factor | Very Low | Low | Nominal | High | Very High |
|--------|----------|-----|---------|------|-----------|
| **ACAP** | 1.42 | 1.19 | 1.00 | 0.85 | 0.71 |
| **PCAP** | 1.34 | 1.15 | 1.00 | 0.88 | 0.76 |
| **PCON** | 1.29 | 1.12 | 1.00 | 0.90 | 0.81 |
| **APEX** | 1.22 | 1.10 | 1.00 | 0.88 | 0.81 |
| **PLEX** | 1.19 | 1.09 | 1.00 | 0.91 | 0.85 |
| **LTEX** | 1.20 | 1.09 | 1.00 | 0.91 | 0.84 |

#### Project Factors
| Factor | Very Low | Low | Nominal | High | Very High |
|--------|----------|-----|---------|------|-----------|
| **TOOL** | 1.17 | 1.09 | 1.00 | 0.90 | 0.78 |
| **SITE** | 1.22 | 1.09 | 1.00 | 0.93 | 0.86 |
| **SCED** | 1.43 | 1.14 | 1.00 | 1.00 | 1.00 |

## Size Estimation Guidelines

### Lines of Code (SLOC)
- **Physical LOC**: Count actual lines in source files
- **Logical LOC**: Count executable statements
- **Exclude**: Comments, blank lines, data declarations
- **Include**: Modified and reused code with effort multipliers

### Function Points to SLOC Conversion
| Language | SLOC per FP | Range |
|----------|-------------|-------|
| Assembly | 320 | 213-427 |
| C | 128 | 85-171 |
| COBOL | 106 | 71-141 |
| Java | 53 | 35-71 |
| C++ | 53 | 35-71 |
| Visual Basic | 32 | 21-43 |
| Python | 27 | 18-36 |
| SQL | 12 | 8-16 |

## Model Selection Guidelines

### When to Use Basic COCOMO
- Early project phases
- Rough order-of-magnitude estimates
- Limited project information available
- Simple, straightforward projects

### When to Use Intermediate COCOMO
- Detailed estimates needed
- Project characteristics well understood
- Risk assessment required
- Budget and schedule planning

### When to Use COCOMO II
- Modern development environments
- Object-oriented or component-based development
- Reuse considerations important
- Process maturity variations

## Common Applications

### Project Planning
1. **Effort Estimation**: Total person-months required
2. **Schedule Estimation**: Project duration
3. **Team Sizing**: Number of people needed
4. **Cost Estimation**: Budget requirements

### Risk Assessment
1. **Sensitivity Analysis**: Impact of parameter changes
2. **Best/Worst Case**: Range of possible outcomes
3. **Critical Factors**: Most sensitive parameters
4. **Mitigation Planning**: Address high-risk factors

### Process Improvement
1. **Benchmark Current Performance**: Compare to model predictions
2. **Identify Improvement Areas**: Low-performing factors
3. **Track Progress**: Monitor improvements over time
4. **Set Goals**: Target productivity levels

## Model Limitations

### Assumptions
- **Stable requirements**: Changes increase effort significantly
- **Competent management**: Poor management can double effort
- **Reasonable budget and schedule**: Extreme constraints reduce productivity
- **Lifecycle consistency**: Single development approach throughout

### Not Suitable For
- **Maintenance projects**: Different effort patterns
- **Very small projects** (< 2 KLOC): High overhead percentage
- **Non-procedural languages**: Different productivity characteristics
- **Prototyping**: Exploratory development

## Calibration Guidelines

### Organizational Calibration
1. **Collect historical data** from completed projects
2. **Calculate actual vs. predicted** ratios
3. **Adjust model constants** based on organizational factors
4. **Validate calibration** on new projects
5. **Update regularly** as organization matures

### Industry-Specific Adjustments
- **Financial services**: +20-30% for regulatory compliance
- **Healthcare**: +30-40% for safety requirements
- **Embedded systems**: +40-60% for hardware constraints
- **Web applications**: -10-20% for rapid development tools

---

*COCOMO models provide a systematic approach to estimation but require calibration to organizational and project-specific factors for maximum accuracy.*
