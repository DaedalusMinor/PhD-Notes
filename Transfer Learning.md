Deep learning model is trained and used in another context. If the model is easily generalizable it transfers well
- **inductive transfer**: model space is narrowed in a beneficial way by using model fit on a different but related task
- Two diff approaches:
	- 1. **Develop Model Approach**: fit model on well known predictive modeling problem. if model fits better than a naive one, and feature learning is confirmed to have happened, use the model fit as the start of a second problem of interest. Uses all or some of the parts learned in the first run.
		- tweaking the model by for adapting or refining input-output pairs
	- 2. **Pre-trained Model Approach**: Same as develop model approach, we just don't do any of the training and take the base model from somewhere else.
### When to use it
- When transfer learning boosts performance start, performance slope, and asymptote, it is successful