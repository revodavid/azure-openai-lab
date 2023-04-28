# Prompt Engineering

As we've seen, natural language Generative AI models can produce unexpected responses to prompts. Prompt Engineering is the process of adding additional context to the prompt to provide "grounding" to the AI model and make it more likely to produce the desired response. 

In the prior Conversations section, the System message, the one-shot examples, and the conversation history all provide grounding to the model. If you're building an application that is based on a natural language generative AI model, your application will need to construct a prompt




(Another technique you can use to improve the quality of responses is a process called "[fine-tuning](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/how-to/fine-tuning)", which retrains the underlying model with example prompts and responses that you provide. We don't cover fine-tuning in this workshop, primarily because prompt engineering generally produces better results, faster and more easily.)

More details: https://learn.microsoft.com/en-us/azure/cognitive-services/openai/concepts/advanced-prompt-engineering?pivots=programming-language-chat-completions#specifying-the-output-structure

Proceed to [7 Using the API.md](7%20Using%20the%20API.md).
