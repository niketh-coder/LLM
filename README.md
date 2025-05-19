![download](https://github.com/user-attachments/assets/91228120-c5f1-4d8b-9897-dc4ac1fe27fd)

On May 19 2025


1. Query Preprocessing
Before querying the vector database or LLM, a preprocessing step is applied to the user's input.

This step ensures the query is more semantically rich and context-aware, improving the relevance of retrieved chunks.

2. Iterative Retrieval for Missing Functions
After initial retrieval, the system checks for missing but relevant functions related to the current context.

If certain functional components are referenced but not present, the pipeline iteratively fetches them.

This ensures fine-grained detail and completeness in the retrieved chunks.

3. Enhanced Chunk Ranking Using Cross-Encoder
Instead of relying solely on cosine similarity, the system uses a cross-encoder model (based on BERT) to compute more accurate relevance scores.

The cross-encoder assesses the semantic alignment between the query and each retrieved chunk, leading to better ranking.

| Metric                               | Before | After |
| ------------------------------------ | ------ | ----- |
| **BERT Score (Most Relevant Chunk)** | 0.70   | 0.90  |


Future work:

Test for more complex queries
Find a simplified way to find the metrices for comparision
Add the memory input and the human-in-the-loop for better results
