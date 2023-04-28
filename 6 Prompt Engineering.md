# Prompt Engineering

As we've seen, natural language Generative AI models can produce unexpected or unwanted responses to prompts. This can be caused by any number of factors, including:

* Insufficient information in the training data
* Insufficient context in the prompt
* Lack of capability of the model itself
* Hostile intent by the user providing the prompt ("jailbreaking")

Prompt Engineering is the process of adding additional context to the prompt to provide "grounding" to the AI model and make it more likely to produce the desired response and less likely to produce undesirable outputs. For example, in a chatbot application, the system would inject additional instructions and data into the prompt before the user's actual input, to provide context to the model. 

In the prior Conversations section, the System message, the one-shot examples, and the conversation history all provide grounding to the model via the prompt. If you're building an application that is based on a natural language generative AI model, your application will need to construct the prompt itself.

For more background, read [Introduction to prompt engineering on Microsoft Learn](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/concepts/prompt-engineering). 

## Fine Tuning

Another technique you can use to improve the quality of responses is a process called "[fine-tuning](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/how-to/fine-tuning)", which retrains the underlying model with example prompts and responses that you provide. We don't cover fine-tuning in this workshop, primarily because prompt engineering generally produces better results, faster and more easily.

## Prompt Engineering Techniques

Prompt Engineering is a complex and rapidly-evolving practice. The article [Prompt engineering techniques]() on Microsoft Learn.


This article explains some advanced techniques for designing prompts for Azure OpenAI GPT models. It covers the differences between the Chat Completion and Completion APIs, and how to use system messages, few-shot learning, and other strategies to improve the model outputs.

System message
This section describes how to use the system message to prime the model with context, instructions, or other information relevant to the use case. It shows an example of a system message and the resulting model response.

Few-shot learning
This section explains how to use few-shot learning to adapt language models to new tasks by providing a set of training examples as part of the prompt. It shows how to use examples to prime the model to respond in a certain way, emulate particular behaviors, and seed answers to common questions.

Non chat scenarios
This section shows how to use the Chat Completion API for non chat scenarios, such as sentiment analysis or entity extraction. It shows an example of a prompt and the resulting model response for a sentiment analysis scenario.

Start with clear instructions
This section suggests that telling the model the task you want it to do at the beginning of the prompt, before sharing additional contextual information or examples, can help produce higher-quality outputs. It shows an example of a prompt and the resulting model response with and without clear instructions.

Repeat instructions at the end
This section explains how models can be susceptible to recency bias, which means that information at the end of the prompt might have more significant influence over the output than information at the beginning of the prompt. It suggests experimenting with repeating the instructions at the end of the prompt and evaluating the impact on the generated response.

Prime the output
This section describes how to use a few words or phrases at the end of the prompt to obtain a model response that follows the desired form. It shows an example of a prompt and the resulting model response with and without priming.

Add clear syntax
This section recommends using clear syntax for your prompt, such as punctuation, headings, and section markers, to communicate intent and make outputs easier to parse. It shows an example of a prompt and the resulting model response with and without clear syntax.

Break the task down
This section advises that large language models often perform better if the task is broken down into smaller steps. It shows an example of a prompt and the resulting model response with and without breaking down the task.

Use of affordances
This section explains how to use affordances, such as search, instead of relying on the model’s own parameters for information and answers. It shows an example of a prompt and the resulting model response with and without using affordances.

Chain of thought prompting
This section introduces a variation on breaking down the task technique, where instead of splitting a task into smaller steps, in this approach, you instructs model response to proceed step-by-step and present all steps involved. It shows an example of a prompt and resulting model response with chain-of-thought prompting.

Specifying output structure
This section demonstrates how specifying output structure can have significant impact on nature and quality of results. It shows an example of a prompt and resulting model response with specified output structure.

Temperature and Top_p parameters
This section describes how changing temperature parameter changes output of model. The temperature parameter can be set between 0 and 2. A higher value will make output more random while lower value will make output more focused. Top_probability is another parameter that controls randomness but in different way.

Provide grounding context
This section emphasizes importance of providing reliable data for model to draw responses from (grounding data). It shows an example where system is provided recent blog describing launch of GPT-4 in Azure OpenAI Service, asked name some early customers.

Next steps
This section provides links to learn more about Azure OpenAI, get started with ChatGPT model, check out Azure OpenAI Samples GitHub repository.


More details: https://learn.microsoft.com/en-us/azure/cognitive-services/openai/concepts/advanced-prompt-engineering?pivots=programming-language-chat-completions#specifying-the-output-structure

## Next steps

Once you've finished experimenting with prompt engineering, proceed to [7 Using the API.md](7%20Using%20the%20API.md).

