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
(See experiments.ipynb)
##Lesson 4
### What I learnt
How to analyze experiments, seeing trends, diving deep into an experiment and running multiple experiments side by side to see evaluator metrics.

### What I tweaked
Nothing to tweak, no notebook

# Module 3
## Lesson 1: Playground
~~*(Changing my video by video descriptions to correct for sparse explanations as per  instructor feedback).*~~

Got introduced to and familiarized myself with the **Playground** on the langchain environment which is used for iterating on and testing prompts, which are supposed to serve as a benchmark for a wide variety of interactions.

1. Hooked up OpenAI's API key and went on to converse with the LLM, and learning how to follow up on a question with context.  
2. Learnt to compare different model providers against the same prompt side by side.
3. Ran the same prompt multiple times simultaneously, which would help in tracking performances for complex prompts.  
4. Added an output schema and a tool separately to guide the output in a certain direction.
5. Finally we ran the associated notebook (**see playground_experiments.ipynb**), where a  simple new sample dataset was created (modified by me) with inputs and outputs and the inputs were re-run on playground to gauge performance and modify prompts to be able to match the LLM's output with the desired sample output.

## Lesson 2: Prompt Templates

Got introduced to and familiarized myself with the Prompt section and prompt hub in Langchain.
1. Created a new chat-style prompt (which then takes us to the Playground section).  
2. Prompted the system message to be a *christian missionary from the dark ages* (my diversion from the official demonstration, changing the nature of the prompt), setting the language as a variable and then added an output schema to track whatever the output is.
3. Saved this custom prompt to the prompt hub and used it in the referred ipynb file (**see prompt_hub.ipynb**), model seemed to invoke prompt appropriately.  
A lot of different custom prompts can be made according to use cases.
4. Edited prompt (Christian missionary from the year 2400), committed the change, and ran the updated prompt.
5. Next a prompt was added to the prompt hub (with an agenda modified by me) programmatically from the ipynb file, and then the same prompt was pushed to the prompt hub as a runnable sequence which allows us to change model providers, models and other details; and this was viewed and checked in the prompt hub.

## Lesson 3: Prompt Engineering Lifecycle
Opened the associated ipynb file (**see prompt_engineering_lifecycle.ipynb**), imported a rag application, ran it (with @traceable) and then opened langchain to look at the trace. Then I proceeded to:
1. Open the trace in Playground, added a new dataset through the ipynb file and made a custom prompt (I made the prompt to use a lot of medical metaphors) for the RAG application.
2. Removed the hard coded prompt from the ipynb file and replaced it with our new prompt context.
3. Removed the manually formatted messages and used the prompt instead.

Now everytime changes are to be made, the prompt can be updated accordingly and committed, which will automatically update it in our code, eliminating the need to change the code
