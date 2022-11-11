# Theoritical questions

## **What is the purpose of subword tokenization used by transformer models?**

The purpose of the subword tokenization used by transformer models is to to split words into subwords in order to better represent them. The words that are rarely used are changed to their subwords because the probability of their subwords showing is greater than the base word itself. So this can help the model to better learn the relationships between words, improve its ability to generalize to out-of-vocabulary words, and to allow it to better handle inflected forms of words.

### - What is the effect on the vocabulary size?

It reduces the vocabulary size by replacing words with subwords. This can be beneficial if the dataset is large and the number of unique words is large. It can also be helpful if the data set contains a lot of rare words.

### - How does it impact out-of-vocabulary words (words which are not in the training data, but appear in the test data, or production environment)?

Because the rarest words and composed words are broken into different subwords, you have less chances of facing out-of-vocabulary words. Which means that the model will be more effective and have less difficulties analyzing the input.

## **When building an encoder-decoder model using an RNN, what is the purpose of adding attention?**

### - What problem are we trying to solve?

Attention is supposed to fix to the limitation of the Encoder-Decoder model encoding the input sequence to one fixed length vector from which to decode each output time step. In the RNN the limitation is due to the vanishing/exploding gradient problem. It remembers the parts which it just saw. So, the longer the input sentence, the worse the output.

### - How does attention solve the problem?

Adding attention allows the model to focus on specific parts of the input when predicting a certain part of the output sequence, enabling easier learning and of higher quality. Attention itself adds 'weight', relative importance, to words in the context vector being created. This allows the RNN to ignore irrelevant information and focus on the most important information when making predictions.

## **In a transformer model what is the multihead attention used for?**

### - What are we trying to achieve with self-attention?

Self-attention is trying to make sense of the input of the model. The main problem is that when processing a long sequence or multiple sequences the model looses information of relevance of each word. To memorize the whole sequence the self-attention is used.

### - Why do we use multiple head instead of one?

The multihead attention is used to jointly attend to information from different parts of the input. By doing that, we create a more diverse representations which increases the performances of the transformer model.

## **In a transformer model, what is the purpose of positional embedding?**

In a transformer model, positional embedding is used to represent the relative or absolute position of tokens in the sequence. It is impactful because the transformer model is based on self-attention. It allows it to properly learn the relationships between the different positions of words in a sequence.

### - What would be the problem if we didn't use it?

This is necessary because the transformer model does not have an inherent understanding of the order of the inputs and the meaning of it. Without positional embedding, the model would not be able to correctly learn the relationships between the words and would therefore be less accurate.

## (2 point) **What are the are the purpose of benchmarks?**

### - And are they reliable? Why?

## (4 points) **What are the differences between BERT and GPT?**

### - What kind of transformer-based model are they?

### - How are they pretrained?

### - How are they fine-tuned?

## (2 points) **How are zero-shot and few-shots learning different from fine-tuning?**

### - How do fine-tuning, zero-shot, and few-shot learning affect the model's weights?

## (2 point) **In a few paragraphs, explain how the triplet loss is used to train a bi-encoder model for semantic similarity?**

## (2 point) **What is the purpose of using an Approximate Nearest Neighbour method to speed up search?**

### - What does it really reduce?
