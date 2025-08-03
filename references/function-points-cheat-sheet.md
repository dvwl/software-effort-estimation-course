# Function Points Cheat Sheet

Quick reference for Function Point Analysis (FPA) including counting rules, complexity assessment, and calculations.

## Function Point Components

### 1. External Inputs (EI)
**Definition**: Data or control information provided by the user to the application

**Examples**:
- Add customer record
- Update inventory item
- Delete employee
- Login authentication
- File upload

**Complexity Assessment**:
| Complexity | Data Elements | File Types | Complexity Points |
|------------|---------------|------------|-------------------|
| **Low** | 1-4 | 0-1 | 3 |
| **Average** | 5-15 | 2 | 4 |
| **High** | 16+ | 3+ | 6 |

### 2. External Outputs (EO)
**Definition**: Data or control information sent to the user from the application

**Examples**:
- Customer report
- Invoice generation
- Email notifications
- Dashboard charts
- Export files

**Complexity Assessment**:
| Complexity | Data Elements | File Types | Complexity Points |
|------------|---------------|------------|-------------------|
| **Low** | 1-5 | 0-1 | 4 |
| **Average** | 6-19 | 2-3 | 5 |
| **High** | 20+ | 4+ | 7 |

### 3. External Inquiries (EQ)
**Definition**: Online inputs that result in the retrieval of data

**Examples**:
- Customer lookup
- Product search
- Account balance inquiry
- Order status check
- Help system queries

**Complexity Assessment**:
| Complexity | Data Elements | File Types | Complexity Points |
|------------|---------------|------------|-------------------|
| **Low** | 1-5 | 0-1 | 3 |
| **Average** | 6-19 | 2-3 | 4 |
| **High** | 20+ | 4+ | 6 |

### 4. Internal Logical Files (ILF)
**Definition**: User identifiable group of logically related data maintained within the application

**Examples**:
- Customer master file
- Product catalog
- Employee records
- Order database
- Configuration settings

**Complexity Assessment**:
| Complexity | Record Types | Data Elements | Complexity Points |
|------------|--------------|---------------|-------------------|
| **Low** | 1 | 1-19 | 7 |
| **Average** | 2-5 | 20-50 | 10 |
| **High** | 6+ | 51+ | 15 |

### 5. External Interface Files (EIF)
**Definition**: User identifiable group of logically related data used by the application but maintained by another application

**Examples**:
- Third-party payment gateway
- External user directory
- Vendor catalog feeds
- Government tax tables
- Partner inventory systems

**Complexity Assessment**:
| Complexity | Record Types | Data Elements | Complexity Points |
|------------|--------------|---------------|-------------------|
| **Low** | 1 | 1-19 | 5 |
| **Average** | 2-5 | 20-50 | 7 |
| **High** | 6+ | 51+ | 10 |

## General System Characteristics (GSC)

Rate each characteristic from 0-5:
- **0**: No influence
- **1**: Incidental influence
- **2**: Moderate influence
- **3**: Average influence
- **4**: Significant influence
- **5**: Strong influence throughout

### GSC Factors

| # | Characteristic | Weight | Description |
|---|----------------|--------|-------------|
| 1 | **Data Communications** | 1 | Distributed processing, online data entry |
| 2 | **Distributed Data Processing** | 1 | Application runs on multiple processors |
| 3 | **Performance** | 1 | Response time, throughput requirements |
| 4 | **Heavily Used Configuration** | 1 | Utilization of computing resources |
| 5 | **Transaction Rate** | 1 | How frequently transactions are executed |
| 6 | **Online Data Entry** | 1 | Interactive input of data |
| 7 | **End-User Efficiency** | 1 | Human factors, ease of use |
| 8 | **Online Update** | 1 | Online update of internal logical files |
| 9 | **Complex Processing** | 1 | Complex algorithms, extensive calculations |
| 10 | **Reusability** | 1 | Code designed and developed for reuse |
| 11 | **Installation Ease** | 0.5 | Ease of installation and setup |
| 12 | **Operational Ease** | 0.5 | Automated operations, error recovery |
| 13 | **Multiple Sites** | 1 | Application designed for multiple locations |
| 14 | **Facilitate Change** | 1 | Ease of modification and enhancement |

## Calculation Process

### Step 1: Count Unadjusted Function Points (UFP)
```
UFP = (EI × 3/4/6) + (EO × 4/5/7) + (EQ × 3/4/6) + (ILF × 7/10/15) + (EIF × 5/7/10)
```

### Step 2: Calculate Total Degree of Influence (TDI)
```
TDI = Σ(GSC Rating × Weight) for all 14 characteristics
```

### Step 3: Calculate Value Adjustment Factor (VAF)
```
VAF = 0.65 + (TDI × 0.01)
```
Range: 0.65 to 1.35

### Step 4: Calculate Adjusted Function Points (AFP)
```
AFP = UFP × VAF
```

## Counting Guidelines

### What to Count as Separate Functions

**External Inputs (EI)**:
- Different logical files updated
- Different processing logic
- Different input formats
- Different validation rules

**External Outputs (EO)**:
- Different report formats
- Different calculations
- Different data sources
- Different selection criteria

**External Inquiries (EQ)**:
- Different search criteria
- Different display formats
- Different data sources
- Different access levels

### What NOT to Count
- Error messages (part of primary function)
- Help text (unless complex help system)
- System administration functions (unless user-requested)
- Duplicate reports with minor format differences
- Navigation elements (menus, buttons)

## Data Element Counting

### Count as Data Elements
- User recognizable fields
- System-generated fields (timestamps, IDs)
- Foreign keys when displayed to user
- Calculated fields displayed to user
- Control information (action codes, function keys)

### Do NOT Count as Data Elements
- Literal values, headings, titles
- Paging information
- Physical implementation fields not visible to user
- Derived attributes stored for performance only

## File Type Counting

### Count as File Types Referenced
- Master files read/updated
- Transaction files processed
- Reference tables accessed
- Control files used
- Interface files accessed

### Logical vs. Physical Files
- Count logical files, not physical implementation
- Related tables that represent single logical entity = 1 file type
- Junction/intersection tables usually don't count separately

## Common Estimation Patterns

### Typical Function Point Distribution
| Component | % of Total FP | Typical Range |
|-----------|---------------|---------------|
| **EI** | 20-30% | Simple forms and updates |
| **EO** | 15-25% | Reports and exports |
| **EQ** | 10-20% | Searches and lookups |
| **ILF** | 30-50% | Core business entities |
| **EIF** | 5-15% | External system interfaces |

### Complexity Distribution Guidelines
| Complexity | Typical % | When to Use |
|------------|-----------|-------------|
| **Low** | 35% | Simple, straightforward functions |
| **Average** | 50% | Standard business functions |
| **High** | 15% | Complex, multi-step processes |

## Quick Estimation Techniques

### Early Estimation (Requirements Phase)
1. **Count major business entities** → estimate ILFs
2. **Identify key user processes** → estimate EIs
3. **List important reports** → estimate EOs
4. **Consider search/inquiry needs** → estimate EQs
5. **Identify external systems** → estimate EIFs

### Rough Sizing Formula
```
Rough FP = (# of Inputs × 4) + (# of Outputs × 5) + (# of Files × 10) + (# of Interfaces × 7)
```

## Conversion to Other Metrics

### Function Points to Lines of Code
See [Productivity Benchmarks](productivity-benchmarks.md) for language-specific conversion rates

### Function Points to Development Effort
| Application Type | Hours per FP | Range |
|------------------|--------------|-------|
| **Business Applications** | 10-20 | Standard complexity |
| **Web Applications** | 8-16 | Modern frameworks |
| **System Software** | 15-30 | High complexity |
| **Real-time Systems** | 20-35 | Embedded constraints |

## Quality Assurance Checklist

### During Counting
- [ ] All user-requested functions identified
- [ ] Complexity consistently assessed
- [ ] Data elements properly counted
- [ ] File references validated
- [ ] No double-counting of functions

### Final Review
- [ ] Function point distribution reasonable
- [ ] Complexity distribution follows guidelines
- [ ] GSC ratings justified and documented
- [ ] Calculations verified
- [ ] Results compared to similar projects

## Common Pitfalls

### Over-counting
- Counting technical functions not visible to users
- Double-counting related functions
- Counting every screen as separate function
- Including infrastructure/framework functions

### Under-counting
- Missing batch processing functions
- Forgetting interface/integration functions
- Underestimating complexity factors
- Missing control/administrative functions

### Complexity Errors
- All functions rated as "Average"
- Not considering data element counts
- Ignoring file reference counts
- Inconsistent complexity criteria

---

*Function Point Analysis requires practice and consistency. When in doubt, document assumptions and maintain counting standards across projects.*
