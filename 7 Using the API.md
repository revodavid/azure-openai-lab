# Using the Azure OpenAI Service API

Note, this section assumes familiarity with developer tools including the Azure Cloud Shell, shell scripts, and environment variables. If you are not familiar with these tools, you may want to skip ahead to the next section.

The Completions Playground and the Chat Playground in the Azure OpenAI Studio are handy tools for experimenting with the OpenAI natural language models. To add the power of these models to your applications, however, you will use the Azure OpenAI Service API.

## The Completion and Conversation APIs

The Azure OpenAI Service API provides two APIs: the Completions API and the Conversation API. The Completion API takes a single prompt as input, and is used to generate text completions. The Conversation API takes a conversation history as input, and generates the next AI response to the conversation. The Conversation API is particularly suitable for chatbot applications, but can be used for other applications as well.

You can find a more complete list at [aka.ms/oai/models](https://aka.ms/oai/models).

| Model | Model ID | API Type |
| ----| --------------- | --------------- |
| GPT-3.5 | `text-davinci-003` | Completions | 
| ChatGPT | `gpt-35-turbo` | Conversation |
| GPT-4 | `gpt-4` | Conversation |

In this workshop, we will try out GPT-3.5 and ChatGPT. GPT-4 is currently in preview, and existing Azure OpenAI customers can apply by [filling out this form](https://aka.ms/oai/get-gpt4).

## Finding your API key

Regardless of which API you use, you will need your unique API key to successfully complete any call. You can find your API key in the [Azure Portal](https://portal.azure.com) as follows:

1. Navigate to your `openai-lab-build` resource
2. Click "Keys and Endpoint" in the left-hand menu
3. Copy the Key 1 value and keep it handy (say, in a Notepad window). You'll be needing it soon.

## The Completion API with GPT-3.5

Return to the Completions Playground in the Azure OpenAI Studio.

## TODO

* Generate a completion to "a long and unusual cat name is " from the UI
* View code, save the curl command to a file
* Edit the file, provide the key
* Run the curl command from the Azure shell

### optional

* Python example (tricky to do in the shell because of package dependencies)
* A more self-contained shell command, with options?

Proceed to [8 Learnings and Resources.md](8%20Learnings%20and%20Resources.md).
