# 7-Day Meal Plan Prompt Engineering Library

A curated collection of **advanced prompt engineering frameworks** for generating safe, practical, and highly personalized 7-day meal plans. This repository demonstrates how to combine the **RTCFR framework** with chain-of-thought, ReAct, reverse prompting, multi-agent prompting, and prompt-chaining techniques.

[![GitHub](https://img.shields.io/badge/GitHub-7--day--meal--plan-blue?logo=github)](https://github.com/Karthickbalakrishnan/7-day-meal-plan)
[![License](https://img.shields.io/badge/license-Unspecified-lightgrey)](#license)
[![Markdown](https://img.shields.io/badge/format-Markdown-purple)](#)
[![Prompt Engineering](https://img.shields.io/badge/topic-Prompt%20Engineering-orange)](#)

---

## Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Repository Structure](#repository-structure)
- [RTCFR Framework](#rtcfr-framework)
- [Prompt Techniques](#prompt-techniques)
- [Getting Started](#getting-started)
- [Usage Examples](#usage-examples)
- [Example Core Prompt](#example-core-prompt)
- [Customization Guide](#customization-guide)
- [Safety and Medical Disclaimer](#safety-and-medical-disclaimer)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

Planning an effective meal plan requires more than asking an AI for seven days of recipes. It involves nutritional calculations, dietary restrictions, medical considerations, meal timing, preparation constraints, and structured output.

This repository provides reusable prompt templates that guide AI systems through those considerations using the following workflow:

```text
User Profile
     |
     v
Role and Task Selection
     |
     v
Clinical and Nutritional Analysis
     |
     v
Meal Plan Construction
     |
     v
Grocery and Meal-Prep Planning
     |
     v
Final Structured Response
```

The included templates support vegetarian, non-vegetarian, therapeutic, weight-loss, sports-nutrition, kidney-health, liver-health, lactose-intolerance, and multi-condition use cases.

---

## Key Features

- **RTCFR-based prompt templates**
- **Seven-day structured meal planning**
- **Therapeutic nutrition considerations**
- **Vegetarian and lacto-ovo dietary support**
- **Low-GI and weight-loss planning concepts**
- **Multi-step clinical reasoning**
- **ReAct-style Thought–Action–Observation workflows**
- **Multi-agent specialist collaboration**
- **Tree-of-Thoughts pathway evaluation**
- **Reverse prompt generation**
- **Grocery and batch-preparation guidance**
- **Markdown-ready AI responses**
- **Few-shot examples for consistent outputs**

---

## Repository Structure

| File | Description |
|---|---|
| [`README.md`](README.md) | Repository overview and documentation |
| [`Core RTCFR Base Prompt Template.md`](Core%20RTCFR%20Base%20Prompt%20Template.md) | Primary RTCFR template for generating a 7-day therapeutic meal plan |
| [`Core RTCFR Base Prompt Template - table format please.pdf`](Core%20RTCFR%20Base%20Prompt%20Template%20-%20table%20format%20please.pdf) | PDF reference for the table-format RTCFR template |
| [`Chain of Thought (CoT) Prompting.md`](Chain%20of%20Thought%20%28CoT%29%20Prompting.md) | Step-by-step nutritional reasoning prompt |
| [`ReAct (Reasoning + Acting) Prompting.md`](ReAct%20%28Reasoning%20%2B%20Acting%29%20Prompting.md) | Iterative Thought–Action–Observation prompt for complex restrictions |
| [`Reverse Prompting Technique.md`](Reverse%20Prompting%20Technique.md) | Reconstructs the original RTCFR prompt from a sample result |
| [`Sequence Chaining Prompting.md`](Sequence%20Chaining%20Prompting.md) | Sequential eight-to-nine-step meal-planning workflow |
| [`prompt chaining.md`](prompt%20chaining.md) | Multi-stage profile, meal-plan, and grocery-planning chain |
| [`Tree of Thoughts (ToT) Prompting.md`](Tree%20of%20Thoughts%20%28ToT%29%20Prompting.md) | Compares multiple dietary strategies before selecting the optimal path |
| [`Multi-Agent Prompting.md`](Multi-Agent%20Prompting.md) | Simulates a specialist panel for collaborative meal-plan decisions |

---

## RTCFR Framework

RTCFR is a structured prompt-design framework that separates:

| Component | Purpose |
|---|---|
| **R — Role** | Assigns the AI a relevant professional persona |
| **T — Task** | Defines the objective and required actions |
| **C — Context** | Supplies demographics, medical constraints, preferences, and goals |
| **F — Few-Shots** | Provides representative input/output examples |
| **R — Response Format** | Defines headings, tables, fields, tone, and constraints |

### RTCFR Example Structure

```markdown
### ROLE
You are a clinical nutrition specialist.

### TASK
Create a safe and practical 7-day meal plan.

### CONTEXT
- Age:
- Gender:
- Dietary preference:
- Health conditions:
- Allergies:
- Activity level:
- Cooking constraints:
- Cuisine preference:
- Goal:

### FEW-SHOT EXAMPLES
Provide one or two examples of the required meal and formatting style.

### RESPONSE FORMAT
Return:
1. Nutrition strategy
2. 7-day meal plan
3. Grocery list
4. Meal-preparation guide
5. Safety guidance
```

---

## Prompt Techniques

### 1. Core RTCFR Prompt

The core prompt defines a clinical-dietitian role and generates a culturally appropriate lacto-ovo vegetarian plan for a specific Type 2 diabetes and hypertension profile.

Best suited for:

- Balanced personalized plans
- Standardized AI output
- Few-shot formatting
- Grocery-list creation
- Therapeutic meal explanations

### 2. Chain-of-Thought Prompting

The Chain-of-Thought prompt instructs the model to reason through calorie needs, protein, fibre, carbohydrate quality, fats, meal timing, preparation, and regional availability before producing the final table.

Best suited for:

- Transparent planning decisions
- Complex nutrition constraints
- Educational outputs
- Preparing or refining a detailed plan

> **Note:** The model should present a concise clinical rationale rather than expose unnecessary private chain-of-thought or hidden reasoning.

### 3. ReAct Prompting

ReAct combines:

```text
Thought → Action → Observation
```

This approach is useful for constrained scenarios such as chronic kidney disease and gout.

Best suited for:

- Ingredient filtering
- Medical restriction analysis
- Iterative safety checks
- Low-purine or electrolyte-controlled diets

### 4. Prompt Chaining

Prompt chaining divides planning into specialized stages:

1. Assess the user and calculate nutritional requirements.
2. Generate the 7-day meal plan.
3. Generate the grocery list and preparation guide.

Best suited for:

- Long prompts
- Complex workflows
- Modular AI applications
- Manual approval between stages

### 5. Sequence Chaining

Sequence chaining executes an ordered set of planning steps, including calorie calculations, protein-source identification, breakfast design, packed lunches, evening snacks, dinners, shopping, and meal preparation.

Best suited for:

- Busy professionals
- Repeatable workflows
- Step-by-step automation
- Consistent meal-plan formatting

### 6. Tree-of-Thoughts Prompting

The Tree-of-Thoughts template explores multiple dietary pathways:

- Mediterranean
- DASH
- Low-carbohydrate, plant-forward

It compares the approaches according to compliance, liver health, and blood-pressure control before selecting the final strategy.

Best suited for:

- Comparing dietary approaches
- Choosing among equally viable plans
- Medical optimization
- Decision documentation

### 7. Multi-Agent Prompting

Multi-agent prompting simulates collaboration between specialists, for example:

- Clinical gastroenterologist
- Sports nutrition specialist
- Executive chef
- Clinical dietitian
- Meal-preparation specialist

Best suited for:

- Plans involving competing requirements
- Gastrointestinal and performance goals
- Taste-versus-health trade-offs
- Practical meal delivery

### 8. Reverse Prompting

Reverse prompting uses an existing meal-plan output to reconstruct the RTCFR prompt that likely generated it.

Best suited for:

- Prompt extraction
- Prompt documentation
- Style replication
- Converting existing examples into reusable templates
- Training prompt libraries

---

## Getting Started

### Prerequisites

- A text editor or Markdown viewer
- Access to an AI text-generation model
- Optional: access to a clinician or registered dietitian for medical review

### 1. Choose a Prompt Template

Select a template according to the required complexity:

| Requirement | Recommended Template |
|---|---|
| General personalized plan | Core RTCFR |
| Detailed nutritional reasoning | Chain-of-Thought |
| Strict therapeutic restrictions | ReAct |
| Modular automation | Prompt Chaining |
| Sequential workflow | Sequence Chaining |
| Multiple dietary options | Tree-of-Thoughts |
| Conflicting specialist requirements | Multi-Agent |
| Reverse-engineer an existing output | Reverse Prompting |

### 2. Copy the Template

Open the relevant Markdown file and copy the prompt into your preferred AI interface.

### 3. Replace the Placeholder Values

Update fields such as:

- Age
- Gender
- Height and weight
- Dietary preference
- Medical conditions
- Allergies
- Cuisine preference
- Activity level
- Weight or fitness goal
- Available cooking time
- Weekly budget
- Portion requirements
- Medications

### 4. Run the Prompt

Ask the model to:

- Calculate an estimated calorie range
- Create a complete 7-day plan
- Include meal-level macro estimates
- Add a grocery list
- Add meal-preparation instructions
- Add relevant medical disclaimers

### 5. Review the Result

Validate:

- Calorie estimates
- Nutrient totals
- Food safety
- Medical restrictions
- Medication interactions
- Sodium and potassium limits
- Ingredient availability
- Portion sizes
- Hidden allergens

---

## Usage Examples

### Example: Diabetes, Hypertension, and Vegetarian Diet

```text
Create a 7-day lacto-ovo vegetarian meal plan for:

- Age: 42
- Gender: Female
- Condition: Type 2 diabetes
- Additional condition: Mild hypertension
- Goal: Weight loss and blood glucose stability
- Lactose intolerance
- No mushrooms
- Moderate activity
- North/South Indian fusion cuisine
- Preference for home-cooked meals
```

### Example: NAFLD and Hypertension

```text
Create a 7-day Mediterranean/DASH-inspired plan for:

- Age: 50
- Stage 1 hypertension
- NAFLD
- Preference for low-sodium food
- No alcohol
- High-fibre requirement
- Beginner-level cooking skills
```

### Example: Athlete with IBS

```text
Create a 7-day low-FODMAP, lactose-free, vegetarian meal plan for:

- Age: 29
- 1.6 g/kg protein target
- Irritable bowel syndrome
- Lactose intolerance
- Workout at 6:30 PM
- 15-minute breakfast limit
- Packed-lunch requirement
```

---

## Example Core Prompt

```markdown
### ROLE
You are a Board-Certified Clinical Dietitian and Sports Nutritionist
with more than 15 years of meal-planning experience.

### TASK
Create a safe, balanced, personalized 7-day meal plan tailored to the
user's medical profile, cultural preferences, goals, and limitations.

### CONTEXT
- Age: 42
- Gender: Female
- Diet: Lacto-ovo vegetarian
- Medical conditions: Type 2 diabetes and mild hypertension
- Goal: Weight loss and blood glucose stabilization
- Allergen: Lactose intolerance
- Disliked food: Mushrooms
- Activity: 30-minute brisk walk daily
- Cuisine: North/South Indian fusion
- Cooking preference: Accessible home-cooked meals

### FEW-SHOT EXAMPLE
Input: 28-year-old male, non-vegetarian, high cholesterol, muscle gain.
Output: Grilled salmon with quinoa and broccoli.

### RESPONSE FORMAT
Provide:

1. Executive nutritional strategy
2. Calorie and macro targets
3. Seven days of meals
4. Calories and macros per meal
5. Therapeutic rationale
6. Categorized grocery list
7. Meal-preparation guide
8. Medical disclaimer and monitoring advice
```

---

## Customization Guide

Before using a template, customize the following sections:

### User Profile

- Age
- Gender
- Height
- Weight
- Medical history
- Allergies
- Food intolerances
- Medicines
- Current diet
- Activity level
- Work schedule

### Nutrition Requirements

- Calorie range
- Protein range
- Fibre target
- Carbohydrate distribution
- Fat distribution
- Sodium limit
- Potassium limit
- Phosphorus limit
- Fluid restriction

### Practical Constraints

- Cooking time
- Budget
- Family size
- Leftover preferences
- Ingredient availability
- Regional cuisine
- Batch-cooking availability
- Food-storage capacity
- Kitchen equipment

### Output Constraints

- Markdown table
- Meal names
- Portion sizes
- Calories
- Protein
- Carbohydrates
- Fat
- Fibre
- Shopping quantities
- Preparation time
- Storage guidance
- Substitution options

---

## Safety and Medical Disclaimer

These prompts are designed for educational and planning purposes. They do not provide medical diagnosis or replace advice from a qualified clinician.

AI-generated nutrition advice may contain:

- Incorrect calorie estimates
- Unsafe nutrient restrictions
- Ingredient or allergen errors
- Drug–food interactions
- Incorrect assumptions about body composition
- Culturally inappropriate substitutions
- Unverified nutrition claims

Consult a registered dietitian or licensed healthcare professional when planning meals for:

- Diabetes
- Kidney disease
- Heart disease
- Liver disease
- Pregnancy
- Eating disorders
- Gout
- Severe hypertension
- Food allergies
- Gastrointestinal conditions
- Children or older adults
- Medication-controlled dietary requirements

Never make significant dietary or medication changes based only on an AI-generated plan.

---

## Contributing

Contributions are welcome.

You can contribute by:

- Adding new prompt frameworks
- Improving existing RTCFR templates
- Adding safer few-shot examples
- Supporting additional medical profiles
- Improving grocery-list logic
- Adding regional cuisine examples
- Adding table-formatted variants
- Correcting nutritional assumptions
- Improving Markdown formatting
- Fixing typos and broken links
- Adding tests or prompt evaluations

Before submitting a medical prompt, include:

- The target condition
- Applicable restrictions
- Source or clinical reference
- Required disclaimers
- Example input
- Expected response format
- Safety limitations

---

## License

No license file is currently included in this repository.

Until a license is added, users should assume that no reuse, modification, or redistribution rights are explicitly granted. For permitted use or licensing inquiries, contact the repository owner:

- **Owner:** [Karthickbalakrishnan](https://github.com/Karthickbalakrishnan)
- **Repository:** [7-day-meal-plan](https://github.com/Karthickbalakrishnan/7-day-meal-plan)

---

## Repository Status

- **Visibility:** Public
- **Default branch:** `main`
- **Primary format:** Markdown
- **Repository size:** Approximately 48 KB
- **Stars:** 0
- **Forks:** 0
- **Open issues:** 0
- **Declared license:** None
- **Primary purpose:** Prompt engineering for nutritional planning
