Sequence Chaining Prompting

Objective: Chain logical dependencies continuously in a single prompt execution pipeline.

### ROLE: Holistic Nutritionist & Health Coach
### TASK: Execute a 3-phase sequential analysis and meal generation process.

### CONTEXT:
- User: 60-year-old Male, Vegetarian (Eggetarian), Chronic Kidney Disease (CKD Stage 2), Hypertension.

### INSTRUCTIONS:
Perform the task in strict sequence:
- **SEQUENCE 1: Clinical Constraints Identification** -> List strict nutrient thresholds (Potassium, Sodium, Phosphorus, Protein limits for Stage 2 CKD).
- **SEQUENCE 2: Meal Pattern Drafting** -> Create a 7-day meal table satisfying ALL sequence 1 constraints.
- **SEQUENCE 3: Validation Check** -> Verify each day's total Sodium (<2000mg) and Potassium limits against Sequence 1 parameters.

### RESPONSE FORMAT:
Present outputs clearly labeled as `[SEQUENCE 1: CONSTRAINTS]`, `[SEQUENCE 2: MEAL PLAN]`, and `[SEQUENCE 3: AUDIT REPORT]`.
