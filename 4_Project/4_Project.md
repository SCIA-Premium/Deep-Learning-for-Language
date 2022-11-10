# Theoritical questions

## **What is the purpose of subword tokenization used by transformer models?**

The purpose of the subword tokenization used by transformer models is to to split words into subwords in order to better represent them. The words that are rarely used are changed to their subwords because the probability of their subwords showing is greater than the base word itself. So this can help the model to better learn the relationships between words, improve its ability to generalize to out-of-vocabulary words, and to allow it to better handle inflected forms of words.

### - What is the effect on the vocabulary size?

It reduces the vocabulary size by replacing words with subwords. This can be beneficial if the dataset is large and the number of unique words is large. It can also be helpful if the data set contains a lot of rare words.

### - How does it impact out-of-vocabulary words (words which are not in the training data, but appear in the test data, or production environment)?

Because the rarest words and composed words are broken into different subwords, you have less chances of facing out-of-vocabulary words. Which means that the model will be more effective and have less difficulties analyzing the input.

## **When building an encoder-decoder model using an RNN, what is the purpose of adding attention?**

Adding attention allows the model to focus on specific parts of the input when predicting a certain part of the output sequence, enabling easier learning and of higher quality.

### - What problem are we trying to solve?



### - How does attention solve the problem?

## (2 point) **In a transformer model what is the multihead attention used for?**

### - What are we trying to achieve with self-attention?

### - Why do we use muliple head instead of one?

## (2 point) **In a transformer model, what is the purpose of positional embedding?**

### - What would be the problem if we didn't use it?

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
