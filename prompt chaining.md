Prompt Chaining Technique

Objective: Break down the complex meal generation process into a multi-step sequential workflow for maximum detail, accuracy, and safety.

Chain Overview

Step 1: User Profile Assessment & Nutritional Requirement Calculations.

Step 2: Meal Plan Generation (Days 1 to 7).

Step 3: Grocery List & Prep Plan Generation.

Step 1: User Profile & Medical Assessment

### ROLE: Senior Clinical Dietitian
### TASK: Analyze user metrics and produce a Clinical Nutrition Strategy.
### CONTEXT:
- Age: 35 | Gender: Male
- Diet: Non-Vegetarian
- Medical Impact: Fatty Liver (NAFLD Stage 1), Uric Acid / Gout risk
- Goal: Reverse NAFLD, manage uric acid
- Preferences: Easy-to-cook recipes, Mediterranean diet influence

### RESPONSE FORMAT:
1. Daily Caloric Needs (BMR & TDEE calculation).
2. Recommended Macro Split (% Carbs, Protein, Fat).
3. Foods to Explicitly Include (Therapeutic).
4. Foods to Strictly Avoid (Purine-rich/Trans fats).
5. Specific Meal Timing & Hydration Rules.


Step 2: 7-Day Meal Plan Blueprint (Input Output from Step 1)

### ROLE: Master Culinary Nutritionist
### TASK: Using the Nutrition Strategy generated below, create a complete 7-Day Meal Plan.
### CONTEXT: 
[PASTE OUTPUT FROM STEP 1 HERE]

### FEW-SHOT EXAMPLE:
Day 1 Lunch: Lemon Garlic Baked Chicken Breast (120g) + Steamed Asparagus + Brown Rice (1/2 cup). *Target: Low purine, low refined sugar, high antioxidants.*

### RESPONSE FORMAT:
- Days 1 through 7 breakdown:
  - Breakfast, Lunch, Snack, Dinner.
  - Estimated Calories & Macros per meal.
  - Therapeutic justification per day.


Step 3: Grocery & Meal Prep Optimization (Input Output from Step 2)

### ROLE: Meal Prep Specialist & Grocery Optimizer
### TASK: Convert the approved 7-Day Meal Plan into an actionable shopping and meal prep guide.
### CONTEXT:
[PASTE OUTPUT FROM STEP 2 HERE]

### RESPONSE FORMAT:
1. Categorized Grocery List with estimated quantities (Vegetables, Proteins, Grains, Pantry).
2. Step-by-Step Weekend Prep Plan (tasks that take under 2 hours).
3. Substitution Options (e.g., if chicken is unavailable, replace with...).
