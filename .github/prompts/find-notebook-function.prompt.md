---
description: "Use when you need to locate the existing function or notebook cell for a described task, especially in the CPT Gaussian assignment notebook."
name: "Find Notebook Function"
argument-hint: "Describe the operation or goal"
agent: "agent"
---

Help locate the existing code that best matches the user's described goal in this workspace.

- Start with the task wording and relevant notebook heading, then inspect the nearby code cell.
- Trace existing function definitions and call sites. Distinguish custom functions from imported library functions.
- In `Bivariate_Gaussian_CPT_data.ipynb`, known custom helpers include `findfile`, `calculate_covariance`, and `pearson_correlation`. Parts 3 and 4 mostly perform modeling, probability, and conditional-distribution calculations in notebook cells rather than in dedicated functions; verify the current notebook before recommending a target.
- Report the best match with its notebook part, function name or cell purpose, and a brief reason. If no existing function matches, say so and point to the closest relevant cell instead of inventing one.
- If the goal is too vague to choose, ask one focused clarifying question.
- Do not implement, complete `### YOUR CODE HERE ###` placeholders, or modify files unless the user separately asks for that.
