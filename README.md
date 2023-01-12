# Deep Learning for Language [![Profile][title-img]][profile]

[title-img]:https://img.shields.io/badge/-SCIA--PRIME-red
[profile]:https://github.com/bictole

## AUTHORS
Alexandre Lemonnier \<alexandre.lemonnier@epita.fr\>\
Eliott Bouhana \<eliott.bouhana@epita.fr\> \
Sarah Gutierez \<sarah.gutierez@epita.fr\> \
Victor Simonin \<victor.simonin@epita.fr\>

---

The teacher github repository can be found
[here](https://github.com/mvonwyl/epita/tree/master/NLP/2022).

---

## Architecture

Our repository for the project has the following architecture:

```
* 1_Encoder_Decoder : Contains the subject and the notebook for our first lab on the Pytorch tutorial and decoding functions.

* 2_HuggingFace : Contains the subject and the notebook for our second lab on the HuggingFace models.

* 3_Semantic_Search : Contains the subject and the notebook for our third lab.

* 4_Project : Contains the subject and the notebook for our project.

* README.md
```

Each notebook of the labs contains the work done during the lab, with some
comments to  describe our technical choices, and analyse our results.

---

## 1_Encoder_Decoder

In this lab, we had to implement a pretty decent **machine translation model** from German to English. This using the transformer by following a Pytorch tutorial.

To use the transformer, we had to implement some **decoding functions** to decode the output of the transformer.
The tutorial uses a **greedy** approach at decoding. We implemented some variations of this greedy approach, such as **beam search** and **top-k sampling**, with a *temperature* parameter.

The **PyTorch tutorial** helped us a lot to implement the translation model and give a first approach to the transformer. We also learned a lot about the transformer and its architecture.

To compare the decoding function we implemented, we used the **BLEU score**. This score is a metric to evaluate the quality of a translation. The higher the score, the better the translation is. We saw
that the parameters of the decoding function have a big impact on the BLEU score. The top-k sampling with a low temperature and a medium k value (like 3) gave the best results. 

---

## 2_HuggingFace

In this section we had to use the **HuggingFace transformer library** to
fine-tune a model on the IMDB library dataset and then evaluate it on the test
set.

The **HuggingFace transformers course** helped us a lot to go step by step
through the process of fine-tuning a model. First we had to load the **imdb**
dataset, then we had to instantiate a tokenizer to preprocess it, then we had to
create a model and train it with a trainer. 

We used the **distilbert** model as a pre-trained model, as it is light and
fine-tuned fast. We also used the **accuracy** as evaluation instead of the
**loss** (default). We saved our model on HuggingFace model hub. We evaluated
the model in term of accuracy on the test data and we got a **0.92** accuracy.
We also tried to explain why the model could have been wrong for some samples
which have been wrongly classified in the test set. We also compared the
advantages and inconvenient of using this model in production compared to the
naive Bayes we implemented in the first part of the course.

---

## 3_Semantic_Search

In this section we used the **Sentence Transformer library**, the **Faiss library** and
**Beir library** to operate a semantic search on **test set** of the DBPedia
entity dataset. The objective what to compare the performance of the Sentence
Transformer search and the Faiss indexing by computing the MAP@100 and mesuring
the processing time of each query.

We used the **Sentence Transformer library** documentation to understand how to
encode the data and what model to choose for the semantic search to have the
best results. We saw that two models where the best. The first one was using the
cosine-similarity ('msmarco-distilbert-base-v4') and the second one the
dot-product (''msmarco-distilbert-base-tas-b''). For our usage we decided to use
the second one. Our Mean Average Precision @ 100 is about **0.5387**, which not
outstanding but shows us that we probably need to rework how we encode the data
or change (or do our own) model to improve the result. 

The **Faiss library** was used to do an Approximate nearest neighbours (ANN). We
also calculated to MAP@100 with different values of parameters and tried to get
the best result. We ended with something very similar (around **0.5359**) to the
Sentence Transformer model. Then we decided to do some plotting and used the
**Pandas library** to visualize the evolution of the time per query and the
MAP@100 when the parameters *nprobe* and *n_clusters* were changed.
