0. Structure is text in and text out, based on the text out it ingest text in and get inifinite loop
1. Pretraining: label tokens to generate a base/foundation model
2. Supervised fine tunining: See what they predicted and match the pairs
2. Reinforcement Learning from Human Feedback RLHF: rank the outputs rewarding the model what is a safe answer or not
--
- Tokens: the amount of words
- Embeddings: transform the words in numbers/points/dimensions, example puppy and dog have different amount of tokens, but they have the same meaning so they are near
- Temperature: When you increase it you flatten the probability, low temparature reduce de probability and do not sample others probabilities
- max_tokens: max amout of words inn the answer
- seed: control de variability of the answer. Usually 42 (inspired on the hitckhiker galaxy movie)
--
Curiosities:
- groq helps increase the speed
- Chain of thought: instead of just providing ask the model to intermediate thinking/reasoning (think before answer) – prompt: think step by step and explain your reasoning
- Few-shot: if ask this answer that. Show a few examples
---
ReAct: combine reasoning and action to solve complex tasks (thought -> action -> observation loops)
