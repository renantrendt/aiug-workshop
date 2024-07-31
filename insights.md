- Structure is text in and text out, based on the text out it ingest text in and get inifinite loop
- Pretraining: label tokens to generate a base/foundation model
- Supervised fine tunining: See what they predicted and match the pairs
- Reinforcement Learning from Human Feedback RLHF: rank the outputs rewarding the model what is a safe answer or not
<br>
  
- Tokens: the amount of words
- Embeddings: transform the words in numbers/points/dimensions, example puppy and dog have different amount of tokens, but they have the same meaning so they are near
- Temperature: When you increase it you flatten the probability, low temparature reduce de probability and do not sample others probabilities
- max_tokens: max amout of words inn the answer
- seed: control de variability of the answer. Usually 42 (inspired on the hitckhiker galaxy movie)
- search_kwargs: a quantidade de arquivos q o RAG vai retornar
<br>

- Groq helps increase the speed
- Chain of thought: instead of just providing ask the model to intermediate thinking/reasoning (think before answer) – prompt: think step by step and explain your reasoning
- Few-shot: if ask this answer that. Show a few examples
- ReAct: combine reasoning and action to solve complex tasks (thought -> action -> observation loops)
<br>

- RAG: answer the appropriated information rather then the whole content. Its the context window, it will find the information on the data you provide. For 1 document you can insert the pdf but hundreds of files this is the only way. Indexing: vector database, chop in slices the content to find quickly by similarity search. Retrieval e generation: all the content is preloaded, the user place a question, it search for the content and give to LLM to create the answer. (the less you give, the better perform).
- When split your content, do it un chuncks that is relate to the size of the answer you want to looks like
- The chunck needs to have the representation of the answer, context and meaning. (example: user want to know if they will receive their order automatically or need to go to website. We need to explain that is not automatically, he needs to go on specific website)
- Example of random words cut in papers and the user need to figure out what is there
- Semantic chunking: all the paragraphs contains the same ideas
- Process: come a question, you cna insert and Agentic to create hipothesis before retrieve the database, when generate the prompt you can insert another LLM to be a judge (if have some models that what is needed) before pass to LLM create the final answer.
<br>

- Fine tunning is not to give more information about your database, is to teach on how to behave
