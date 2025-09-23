---
layout: default
title: Demo Projects
nav_order: 4
has_children: true
---

# Demo Projects
{: .no_toc }

Hands-on demonstrations that bring software effort estimation concepts to life through practical implementations.

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

---

## Overview

This section contains interactive demos that complement the theoretical concepts covered in the course modules. Each demo is designed to provide practical, hands-on experience with different estimation techniques and tools.

## Available Demos

### Module 2: Analogy-Based Estimation Demo
**Technology**: Python, Jupyter Notebook, scikit-learn  
**Location**: `demos/AnalogyDemo/`  
**Complexity**: Beginner  
{: .label .label-green }

Interactive Jupyter notebook demonstrating analogy-based estimation using machine learning similarity metrics. Learn how to:
- Use historical project data for estimation
- Calculate project similarity using Euclidean distance
- Apply k-nearest neighbors for estimation
- Experiment with different project parameters

**Key Learning Outcomes:**
- Understanding similarity-based estimation
- Hands-on experience with Python data analysis
- Practical application of machine learning concepts
- Interactive experimentation with estimation parameters

[**Open Analogy Demo →**](AnalogyDemo/)

---

### Module 3: Project Estimation & Gantt Chart App
**Technology**: ASP.NET Core, C#, Entity Framework, Mermaid.js  
**Location**: `demos/ProjectEstimator/`  
**Complexity**: Intermediate  
{: .label .label-blue }

Full-featured web application demonstrating comprehensive project management and estimation techniques. Features include:
- Three-point estimation with PERT calculations
- Task dependency management
- Automated Gantt chart generation
- Critical path analysis
- Interactive project timeline visualization

**Key Learning Outcomes:**
- Three-point estimation implementation
- Task dependency modeling
- Critical path analysis
- Web-based project management tools
- Integration of estimation with project scheduling

[**Open ProjectEstimator App →**](ProjectEstimator/)

---

## Getting Started

### Prerequisites
Choose the demo that matches your learning goals and technical background:

**For Python/Data Science learners (Analogy Demo):**
- Python 3.7+ installed
- Jupyter Notebook or VS Code with Python extension
- Basic familiarity with Python and pandas

**For Web Development learners (ProjectEstimator):**
- .NET 8.0 SDK
- Visual Studio Code or Visual Studio
- Basic understanding of web development concepts

### Setup Instructions

#### Analogy Demo Setup
1. Navigate to `demos/AnalogyDemo/`
2. Open `analogy_demo.ipynb` in Jupyter Notebook or VS Code
3. Run the package installation cell: `!pip install scikit-learn`
4. Execute cells sequentially to see the demo in action

#### ProjectEstimator App Setup
1. **Navigate to Demo Directory**
   ```bash
   cd demos/ProjectEstimator
   ```

2. **Restore NuGet Packages**
   ```bash
   dotnet restore
   ```

3. **Create Database**
   ```bash
   dotnet ef database update
   ```

4. **Run Application**
   ```bash
   dotnet run
   ```

5. **Open in Browser**
   Navigate to `http://localhost:5000`

#### Development in VS Code
1. Open the `demos/ProjectEstimator` folder in VS Code
2. Press `F5` to start debugging
3. The application will open in your default browser
4. Use breakpoints for debugging the C# code

---

## Demo Progression

The demos are designed to build upon each other, progressing from simple estimation concepts to more complex project management implementations:

### Learning Path
1. **Start with Analogy Demo** (Module 2) - Learn fundamental estimation concepts
2. **Progress to ProjectEstimator** (Module 3) - Apply concepts in a real application
3. **Experiment and Extend** - Use the provided exercises to explore further

---

## Extension Opportunities

Both demos provide opportunities for further exploration:

### Analogy Demo Extensions
- Add more sophisticated similarity metrics
- Implement cross-validation for model evaluation
- Experiment with different machine learning algorithms
- Create visualizations of project similarity patterns

### ProjectEstimator Extensions
- Integrate Monte Carlo simulation
- Add resource management features
- Implement team collaboration tools
- Create advanced reporting and analytics

---

*These demos provide practical, hands-on experience that complements the theoretical concepts covered in the course modules. Each demo is designed to be both educational and extensible, allowing you to explore estimation concepts in depth.*
