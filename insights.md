- LLM Structure is: text in and text out, based on the text out it ingest text in and get inifinite loop
- Pretraining: labeling tokens to generate a base/foundation model
- Supervised fine tunining: See what they predicted and match the pairs by labeling again
- Reinforcement Learning from Human Feedback RLHF: rank the outputs rewarding the model what is a safe answer or not
<br>
  
- Tokens: the amount of words
- Embeddings: transform the words in numbers/points/dimensions, example puppy and dog have different amount of tokens, but they have the same meaning so they are near
- Temperature: When you increase it you flatten the probability many diferents word have the same chance to be choosen, low temparature reduce the probability and do not sample others probabilities.
- max_tokens: max amout of words in the answer
- seed: control de variability of the answer. Usually 42 (randomly inspired on the hitckhiker galaxy movie)
- search_kwargs: a quantidade de arquivos q o RAG vai retornar
<br>

- Groq app: helps increase the speed
- Chain of thought: instead of just providing ask the model to intermediate thinking/reasoning (think before answer) – prompt: think step by step and explain your reasoning
- Few-shot: if ask this then answer that. Give a few examples to LLM follow
- ReAct: combine reasoning and action to solve complex tasks (thought -> action -> observation loops)
<br>

- RAG: answer the appropriated information rather then the whole content. Its the context window, it will find the information on the data you provide. For 1 document you can insert the pdf but hundreds of files this is the only way. Indexing: vector database, chop in slices the content to find quickly by similarity search. Retrieval e generation: all the content is preloaded, the user place a question, it search for the content and give to LLM to create the answer. (the less content you feed, the better perform).
- When split your content, do it in chuncks that relate to the size of the answer you want to looks like.
- - Semantic chunking: all the paragraphs contains the same ideas. The chunck needs to have the representation of the answer, context and meaning. (example: user want to know if they will receive their order automatically or need to go to website use its credits. Then in the chunck for both variables (when ask just how to use credits or previous ask) We need to explain that is not automatically, he needs to go on specific link and use its credits)
- Example of why we need RAGS with the right amount of chunks: Imagine random paper words cutout from a magazine all over a table and you need to try to figure out what this means. If you give not words but phrases it will context better.
- Agentic: user place a question, you can insert an Agentic to create hipothesis before send to the database retrieval, then after the retrieval its the step of generate the prompt then after it you can place another Agentic to be a judge before pass to LLM create the final answer or return to improve.
<br>

- Fine tunning is not to give more information about your database, is to teach on how to behave. Change the behavior from a general model to a specialized model on domain specific data set. If you are looking to add new knowledge to LLM then RAG is the right path.
- Quantization: compress very precise numbers into broader numbers: from 0.1 to 1; from 0.2 to 2. Its good to reduce the size of the LLM and increase performance, but loose quality
- Ratio: % that are quantized
