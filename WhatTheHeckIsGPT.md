# GPT -> Generative PreTrained Transformers

*(Fun Fact: GPT-3.5 helped me format plain text to Markdown)*

## 1. What the heck are transformers: History
From predicting data points, we successfully started recognizing image patterns using CNN. However, CNN struggled to understand the patterns in language, the grammatical nuances, gender, plurality, etc. Here Comes RNN, which started processing the tokens/words in the sentence sequentially since the sequence of words in language matters. However, RNNs struggled with large paragraphs, they used to lose context by the time it processed the last sentence of the paragraph. They were also susceptible to vanishing/exploding gradient problem. It was extremely slow since it used to process words sequentially.

Enters Transformers, the primary advantage of transformers over RNN is that they can process data parallelly which means with proper hardware you can do wonders. GPT-3 is trained on 45 TB of text data.

## 2. Core Concepts of Transformers:
   1. **Positional Encodings:**
      RNN used the sequence to understand the semantics of language. Transformers use positional encoding to maintain the sequence. The idea is to take all of the words in your input sequence–an English sentence, in this case–and append each word with a number indicating its order. So, you feed your network a sequence like:
      [("Saurabh", 1), ("says", 2), ("hello", 3), ("world", 4)]

   2. **Attention:**
      Attention is a mechanism that allows a text model to “look at” every single word in the original sentence when making a decision about how to translate words in the output sentence. And how does the model know which words it should be “attending” to at each time step? It’s something that’s learned from training data. By seeing thousands of examples of French and English sentences, the model learns what types of words are interdependent. It learns how to respect gender, plurality, and other rules of grammar.

   3. **Self-Attention:**
      Self-Attention is more advanced than the vanilla attention concept. In general, what makes neural networks powerful and exciting is that they often automatically build up meaningful internal representations of the data they’re trained on. When you inspect the layers of a vision neural network, for example, you’ll find sets of neurons that “recognize” edges, shapes, and even high-level structures like eyes and mouths. A model trained on text data might automatically learn parts of speech, rules of grammar, and whether words are synonymous.
      The better the internal representation of language a neural network learns, the better it will be at any language task. And it turns out that attention can be a very effective way of doing just this, if it’s turned on the input text itself.
      Self-attention helps neural networks disambiguate words, do part-of-speech tagging, entity resolution, learn semantic roles, and a lot more.

## 3. What can transformers do?
   - Text summarization
   - Question answering
   - Classification
   - Named entity resolution
   - Text similarity
   - Offensive message/profanity detection
   - Understanding user queries
   - A whole lot more
