# NLP Deep [![Profile][title-img]][profile]

[title-img]:https://img.shields.io/badge/-SCIA--PRIME-red
[profile]:https://github.com/bictole

## AUTHORS
Alexandre Lemonnier \<alexandre.lemonnier@epita.fr\>\
Eliott Bouhana \<eliott.bouhana@epita.fr\> \
Sarah Gutierez \<sarah.gutierez@epita.fr\> \
Victor Simonin \<victor.simonin@epita.fr\>

---

The teacher github repository can be found [here](https://github.com/mvonwyl/epita/tree/master/NLP/2022).

---

## 1_Encoder_Decoder

## 2_HuggingFace

In this section we had touUse the **HuggingFace transformer library** to fine-tune a model on the IMDB library dataset and then evaluate it on the test set.

The **HuggingFace transformers course** helped us a lot to go step by step through the process of fine-tuning a model. First we had to load the **imdb** dataset, then we had to instantiate a tokenizer to preprocess it, then we had to create a model and train it with a trainer. 

We used the **distilbert** model as a pre-trained model, as it is light and fine-tuned fast. We also used the **accuracy** as evaluation instead of the **loss** (default). We saved our model on HuggingFace model hub. We evaluated the model in term of accuracy on the test data and we got a **0.92** accuracy. We also tried to explain why the model could have been wrong for some samples which have been wrongly classified in the test set. We also compared the advantages and inconvenient of using this model in production compared to the naive Bayes we implemented in the first part of the course.

## 3_Sematic_Search