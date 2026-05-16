# Self-Correct-via-RL-SCoRe---RL-Project

This project consist of 2 Experiments

# 1. Score Algorithm
Here, we implemented the whole SCoRe algorithm. We used distillgpt-2 for and 300 steps for stage 1 and stage 2 each implementing this. The dataset we used for this is GSM8K (We took 300 problems from this dataset), which is a math QnA dataset. This experiment consist of a binary (0 or 1) reward function, both stage 1 and 2 and charts.
# Results:
Since we used only 600 steps (in total) and a very light weight model for this, therefore, we only got a small self correction score i.e., 0.010.

# 2. Our Experiment:
Here, we took 2 models, 1st is generator model (Qwen/Qwen2.5-1.5B-Instruct). Its function is to generate an answer and self correct it using a pre defined prompt and the second model is the critic model (). Its function is ti critisize the 1st model's original response and provide a better one. Then we compared both models and checked if the responses got better.
# Results:
Here the critic model improved the results of the generator model. Out of 50 answers by the generator, critic produced 47 responses better than the generator while the generator only produced 3 responses better than the critic. This result shows that the critic won with a high margin: Critic Win Rate: 94%
