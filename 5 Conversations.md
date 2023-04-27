# Conversations

If you've used consumer conversational AI services like OpenAI's ChatGPT service or [Bing Chat](https://bing.com/chat), you may wonder how the AI agent "remembers" context from earlier in the conversation. As we've seen, Generative AI models including ChatGPT (`gpt-35-turbo`) have no capability to learn, so how does information from the conversation persist?

The answer is: it's a trick! The AI model isn't reacting to your most recent prompt in isolation. The user interface for the chat service provides the model with the *entire* chat history at each turn, invisibly to you, the user. Also observe that if you exit the conversation and return later, the model has no memory of your previous interactions, and you will start again from scratch.

In this section, we'll explore conversations using the Chat Playground in Azure OpenAI Service.

## Chat Playgound

Return to the Azure OpenAI Studio, and click **Chat** under **Playground** in the left-hand menu. 

(If you've already tried the Chat Playground, 
make sure that the **Assistant Setup** dropdown is set to "default", 
and click the **Clear chat** button in the **Chat session** panel to reset the conversation.)






