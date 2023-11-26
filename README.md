# HaystackQAPipelineExample
A jupyter notebook showing how to create a basic QA-Pipeline in Haystack.

This example uses a retriever in combination with a Haystack PromptNode to generate answers for a given question with the help 
of Text2Text-Transformers from HuggingFace.
The documents for the retriever are gathered from wikipedia articles with the help of the python wikipedia libary.
These documents are then being processed by the Haystack PreProcessor and then fetched by the Retriever to provide the
relevant documents for an answer.
The Context-Window (or Token Limit) of the model in the PromptNode is the main limiting factor of this approach because
of the given prompt, which also includes the retrived documents and the question/query alongside the prompt.
