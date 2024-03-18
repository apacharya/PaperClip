MiniLLM Experiment to read / learn scientific paper and answer questions based on it. Also evaluated LLM based on it context retrieval performance.

## Introducing PaperClip: A Personal Learning Assistant that learns and answers questions about scientific paper of interest from arxiv, in a readable, short and digestable format. 
I am building it using LangChain and OpenAI model (gpt-3.5-turbo)

#### Inputs: 
- Input a arxiv paper ID as input (ex: 1706.03762)
- user question (input)


##### Output:
smart answer - a simple summary of scientific paper of interest

##### Concepts I am demostrating are below:
- Role prompting to mimic learning assistant role 
- Vector database to store the data source and support semantic search to retrieve relevant context
- Personalized response 

# Evaluation, 
my aim is to generate responses from PaperClip generating answers to signle questions : " What is the title of the paper?"".I am manually generating the ground truth of 11 papers that are stored in the folder ;  "PaperDB". 
Output -  I am generating a dataframe with question, answer of LLM ( paper name), relevant retrived context. I compliment that with groundtruth

# Evaluation Technique 1: RAGAS: Automated Evaluation of Retrieval Augmented Generation

 I'm taking responses from Step 2: Model with basic instruction prompt and evaluating the LLM model using the [ragas](https://github.com/explodinggradients/ragas) evaluation tool. Uses `gpt-3.5` ad default model for evaluation.

# Evaluation Technique 2: # Evaluation Technique 2: RAG using Phoenix 
https://docs.arize.com/phoenix/evaluation/running-pre-tested-evals/retrieval-rag-relevance


