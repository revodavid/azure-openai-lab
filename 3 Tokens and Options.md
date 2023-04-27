## Understanding tokens

The OpenAI natual language models don't operate on words or characters as units of text, but on something in-between: tokens. A token may be a single character, or a fraction of a word, or an entire word. Many common words are represented by a single token, less common words are represented by multiple tokens.

When you enter text in the prompt box or generate a completion, a counter appears below that counts the total number of tokens in the box. (Note takes a second or so to update if you're actively typing.)

How many tokens are in the following words?

    "apple"

    "hamburger"

    "McDonald"

Tip: OpenAI provides a useful tool for visualizing the tokens in text phrases. Try it out here: [OpenAI Tokenizer](https://platform.openai.com/tokenizer).

The natural language models generate completions one token at a time. In fact, they don't generate a single token at all, but a weighted list of all possible tokens. The API samples one token from this list, with heavily-weighted tokens more likely to be selected than the others. 

![Diagram](https://bea.stollnitz.com/images/how-gpt-works/1-ntokens.png)

Then it adds that token to the prompt and repeats the process until the "Max length (tokens)" limit is met for the completion, or until the model generates a special token called a "stop token", which prevents further tokens from being generated.

This is how the model generates completions of one or multiple words, and why those completions can change from invocation to invocation.

You can observe this proess by modifying the "Max length (tokens)" 