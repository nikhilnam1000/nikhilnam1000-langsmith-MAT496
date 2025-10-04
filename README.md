This is my first commit. Hours of work have went into figuring out how IDE's work, how things are done as I have had minimal exposure to technicalities as a math major. Thank you for reading!

# Module 1
## Lesson 1
### What I learnt
Learnt basic tracing concepts in lesson 1 with the overview of project, traces and runs. 'Decorated' functions with traceabela and tracked individual runs in langchain. Added new metadata statically and also at runtime

### What I tweaked
I changed up the prompt of the RAG slightly and also the questions asked (I tried to be funny)
(See tracing_basics.ipynb)

## Lesson 2
### What I Learnt
Learnt about the different types of runs, compared a default chain type run with an llm type run on langsmith. Added metadata fields to the llm run and customly rendered the llm runs for tool calling, streaming and retriever runs.

### What I tweaked
I slightly tweaked the inputs, didn't find much to tweak in the code elsewhere.
(See types_of_runs.ipynb)

## Lesson 3
### What I learnt
Learnt to use Langgraph, trace(), wrapopenai() and how it helps in tracking performance.

### What I tweaked
Tweaked the inputs
(See alternative_tracing_methods.ipynb)

## Lesson 4
### What I learnt
Used the conversational thread view that openai offers, greatly improving readability for looking at the structure and improving performance.

### What I tweaked
Tweaked the two questions
(See conversational_threads.ipynb )
Note that I will run the openai api key in line to run the program then remove it before saving to avoid problems pushing onto git

# Module 2
## Lesson 1
### What I Learnt
Created an empty dataset and added examples from the ipynb file as 'golden examples' for the llm to refer to. Custom added an LLM generated question to the dataset and modified schemas.

### What I tweaked
Tweaked the input questions and added more examples to the dataset on the langchain platform.
(See dataset_upload.ipynb)

## Lesson 2
### What I Learnt
Used evaluators to compare dataset example against the output run from app, using a function to give a score from 1 to 10 on how similar the run is to the example and opened the auto-evaluator, custom edited in langchain.

### What I tweaked
Tweaked the run output to change the semantics score.
(See evaluators.ipynb)

## Lesson 3
### What I learnt
Used evaluators to run experiments with different openai models, over datasets and specific examples, ran into problems cause I was unable to index datasets properly

### What I Tweaked
Used specific examples and tried my best to find out the dataset labelling problem.