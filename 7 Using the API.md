# Using the Azure OpenAI Service API

Note, this section assumes familiarity with developer tools including the Azure Cloud Shell, shell scripts, and environment variables. If you are not familiar with these tools, you may want to skip ahead to the next section.

The Completions Playground and the Chat Playground in the Azure OpenAI Studio are handy tools for experimenting with the OpenAI natural language models. To add the power of these models to your applications, however, you will use the Azure OpenAI Service API.

## The Completion and Conversation APIs

The Azure OpenAI Service API provides two APIs: the Completions API and the Conversation API. The Completion API takes a single prompt as input and is used to generate text completions. The Conversation API takes a conversation history as input and generates the next AI response to the conversation. The Conversation API is particularly suitable for chatbot applications but can be used for other applications as well.

You can find a more complete list at [aka.ms/oai/models](https://aka.ms/oai/models).

| Model | Model ID | API Type |
| ----| --------------- | --------------- |
| GPT-3.5 | `text-davinci-003` | Completions |
| ChatGPT | `gpt-35-turbo` | Conversation |
| GPT-4 | `gpt-4` | Conversation |

In this workshop, we will try out GPT-3.5 and ChatGPT. GPT-4 is currently in preview, and existing Azure OpenAI customers can apply by [filling out this form](https://aka.ms/oai/get-gpt4).

### Finding your API key

Regardless of which API you use, you will need your unique API key to successfully complete any call. You can find your API key in the [Azure Portal](https://portal.azure.com) as follows:

1. Navigate to your `openai-lab-build` resource
2. Click "Keys and Endpoint" in the left-hand menu
3. Copy the Key 1 value and keep it handy (say, in a Notepad window). You'll be needing it soon.

### The Completion API with GPT-3.5

Return to the Completions Playground in the Azure OpenAI Studio.

### Create a new prompt

1. In the "User Message" box in the right pane, enter the following text: `a long and unusual cat name is `
2. Select `View code`, and select `curl` from the dropdown
3. Copy the curl command to the clipboard, and open the text editor of your choice, and paste the curl command into the editor window.
4. Update the curl command with your API key. The command should look something like this:

    ```bash
    curl https://glovebox-openai.openai.azure.com/openai/deployments/text-davinci-003/completions?api-version=2022-12-01 \
    -H "Content-Type: application/json" \
    -H "api-key: 09c999b9999c99cda999de9999b9ca9d" \
    -d '{
    "prompt": "a long and unusual cat name is",
    "max_tokens": 100,
    "temperature": 1,
    "frequency_penalty": 0,
    "presence_penalty": 0,
    "top_p": 0.5,
    "best_of": 1,
    "stop": null
    }'

### Run the CURL command

1. Open to the [Azure Cloud Shell (https://shell.azure.com/)](https://shell.azure.com/)
2. If prompted, select `Bash` from the dropdown menu.
3. Paste the updated curl command that contains your API key into the shell, and press `Enter`.

The curl command will return a JSON object containing the completion. The completion is the text that follows the prompt. The response from the curl command will look similar to this:

```json
{"id":"cmpl-7AARwaMlXDWi2gWSXo7PAmH5J4Hrg","object":"text_completion","created":1682657804,"model":"text-davinci-003","choices":[{"text":" one that’s not just two syllables. This means that you’ll need to come up with a name that’s longer than that. If you have a female cat, you can choose a name that’s three syllables long. If you have a male cat, you can choose a name that’s four syllables long. You can also use names that are three syllables long if you have a male cat.\n\nIf you have a","index":0,"finish_reason":"length","logprobs":null}],"usage":{"completion_tokens":100,"prompt_tokens":6,"total_tokens":106}}
```

## optional

* Python example (tricky to do in the shell because of package dependencies)
* A more self-contained shell command, with options?

Proceed to [8 Learnings and Resources.md](8%20Learnings%20and%20Resources.md).
