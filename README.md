# RAGAssignment
There are three fundamental parts which are very important to an llm based solution
1. The Vectors and how efficiently they are indexed
2. the LLMs themselves on how they manage the context and give refined output
3. The infrastructure which hosts the entire system

These three points must be the focal point in determining any system architecture for gen AI based applications or use cases
The infrastrucutre is critical since the models are very huge and this brings distinct operational challenges apart from the application architecture to the overall system.
Please refer the System Architecture diagram in repo for a high level view

Problems Faced during this assignment:
1. Not enough ram to process large models on Colab
2. The specified pdf file did not have EOF character and hence was not readable for the pdf reader, I tried modifying the file but since it didnt work, I chose to use another sample file
3. The question-answer task in the huggingface pipeline gives error when the input is sent to the retrievalQA chain of langchain, the input is required in squadExample, when we pass the input in required format it gives required input 'prompt' missing, I inspected the underlying calls but could not find the exact cause in time
4. I would pursue this and try other chain types to figure the optimal structure
5. I did try another task, texy generation task with the HuggingFace pipeline but that did not produce desired results since the language models were small and my embeddings size were larger
6. I tried some configuration and new models, retreivalQA chaintype='refine' and a openai-community/gpt2 model but as per my observation, it required a partial tuning rather than RAG for better results
7. To showcase the possiblity of RAG training a model I used my AzureOpenAI creds to spin up another notebook and rag train the powerful, gpt-35-turbo-inter02 model, I found the integration is more straight forward than using the external libraries, which now I am keen to explore and master
