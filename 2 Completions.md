# Completions

In this section, you will experiment with creating completions with OpenAI natural langage models.

## What is a completion?

A natural language model like OpenAI's `text-davinci-003` has a simple purpose: Given a fragment of text (the "prompt"), generate additional text that is likely to follow the prompt. This is called a "completion".

The definition of "likely" is more complex, but for now, you can think of it as "text similar to text in the training data that often follows text like the prompt". Models like `text-davinci-003` are trained on very large volumes of text data from the internet, and this data influences the model's predictions.

You can learn more details about how OpenAI's models work at Microsoft Learn: [Understand OpenAI's natural language capabilities](https://learn.microsoft.com/en-us/training/modules/explore-azure-openai/5-understand-openai-natural-language).

## Launch the Completions Playground

In the left navigation of the Azure OpenAI Studio, click "Completions" under the "Playground" heading.

In the drop-downs under "Completions playground" make sure the following options are selected:

1. Deployments: `text-davinci-003`
2. Examples: `Load an example` (do not change this option)

## Basic Prompting

In the prompt box (where you see the text "Start typing here"), you can enter any text you like, and then use one of your deployed models to generate a completion. Let's try a few examples.

Enter the following in the prompt box: "I climbed the apple tree and picked an". Now click the "Generate" button below the prompt box.

The generated text will appear in green in the prompt box, following the prompt you entered. It probably now reads: "I climbed the apple tree and picked an apple."

## Completions are non-deterministic

Clear the contents of the prompt box. (Control-A and then Delete should do the trick, or you can reload the page in your browser.) Now enter: "I climbed the tree and picked a" (note: don't specify a kind of tree this time), and click "Generate" again.

Once again, your completion will appear in green. It might read "an apple", "a pear", or something else entirely. The completion is non-deterministic: The model is not guaranteed to generate the same completion for the same prompt every time. 

Click the "Undo" button to delete the provided completion, and then click "Generate" again. What do you observe?

Try it a few more times. Tip: you can click the "Regenerate" button to generate a new completion without deleting the previous one.

## Generating novel content

Even though completions are generated based on frequencies of similar content in the training data, generative AI models are capable of generating novel content that has never existed before. 



## Completions are not facts

Clear the contents of the prompt box again. Enter the following text, then click Generate.

"What is the capital of France?"





















