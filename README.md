# SkimLit (Natural Language Processing Project) Medical Literature Abstract Classifier

The purpose of this noebook is to build an NLP model to make reading medical abstracts easier. We will replicate the *PubMed 200k RCT: a Dataset for Sequential Sentence Classification in Medical Abstracts*. 

The model they've used to achieve their best results is [here](https://arxiv.org/pdf/1612.05251.pdf)

There are four models which will be used to do this.

* The first model will be our baseline results from the TF-IDF vectorizer layer in this model with the Multinomial Naive Bayes algorithm which trains very quickly.

* The second model will be a deep sequence Conv1D with token embeddings.
* The third model will be a hybrid model with bidirectional LSTM and Dense layers combining pretrained token embeddings + characters embeddings.

* The fourth and our final result model will be a tribrid model :Transfer Learning with pretrained token embeddings + character embeddings + positional embeddings.

### This final resultant tribrid model will have the following structure

![image](https://user-images.githubusercontent.com/86077149/148389516-fc20445a-8cc0-4391-8245-93f00d6e9504.png)

#### In the end, our tribrid model will have achieved an accuracy of 83.09% which is greater than the baseline accuracy of 72.18% which we wanted to beat by 10.91%

![image](https://user-images.githubusercontent.com/86077149/148389457-002a0027-cd17-4ed2-b9e8-82c5bd18d632.png)

#### Finally our model will be 83.09% capable of receiving an input like 

![image](https://user-images.githubusercontent.com/86077149/148389792-ea4362c4-3585-4376-8c4e-307d922a7ca2.png)

#### and then converting it into an output like this by label classification

![image](https://user-images.githubusercontent.com/86077149/148389899-c4e45d37-ee75-467f-b52c-de0d519defbb.png)


