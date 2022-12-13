# NLP-project-DSCI-6004

While question-answering systems have gained popularity across many industries, the medical field has proven difficult due 
to the wealth of specialized knowledge. As more and more sizable pretrained language models emerge, retrieval-based approaches 
have shown promise. The goal of this project is to develop a retrieval-based medical question answering system. To do this, 
we leverage huge language models and graphs to extend our knowledge. First, we effectively use Elasticsearch to get a large 
yet coarse set of responses. Then, using knowledge graphs and named entity recognition to take advantage of the relationship 
between the entities in the query and answer, we combine semantic matching with pretrained language models to get a 
fine-grained ranking. We offer a thorough study of both this dataset and the medical reading comprehension test in this project. 
Our qualitative research reveals that our QA answers are often insufficient and QA questions can be satisfactorily answered 
without domain knowledge. We compared the model trained on the entire dataset. the performance of our model is close to human 
expert’s performance, and BERT models do not beat the best performing base model. 

#**Method**

This project aim is to develop a question answeting system in medical domain. For the the
implementation of a BERT-based model which returns “an answer”, given a user question and a
passage which includes the answer of the question. For this question answering task, we used three
differents medical domain datasets, MedQuAD, MEDIQA2019, BiQA and Combined them for fine
tuning a model that is trained on SQUAD 2.0. Stanford Question Answering Dataset (SQuAD) is a
reading comprehension dataset, consisting of questions posed by crowdworkers on a set of Wikipedia
articles, where the answer to every question is a segment of text, or span, from the corresponding
reading passage, or the question might be unanswerable. BiQA is a dataset that has data from Biology,
medical scinces, nutrition domains with number of samples, 6681, 3014, 4099 respectively. MedQuAD
– 47k. MEDIQA2019 - 10k BiQA – 13k samples. I started with the BERT-base pretrained model “bertbase-
uncased” and fine-tune it to have a question answering task. For Question Answering we use the
BertForQuestion Answering class from the transformers library. BERT is a Bidirectional Encoder
Representations from Transformers. It is one of the most popular and widely used NLP models. BERT
models can consider the full context of a word by looking at the words that come before and after it,
which is particularly useful for understanding the intent behind the query asked. Because of its
bidirectionality, it has a deeper sense of language context and flow and hence, is used in a lot of NLP
tasks nowadays. This class supports fine-tuning, but for this example we will keep things simpler and
load a BERT model that has already been fine-tuned for the SQuAD benchmark. The transformers
library has a large collection of pre-trained models which we can reference by name and load easily.
Apparently the vocabulary of this model is identicaly to the one in bert-base-uncased. we can load the
tokenizer from bert-base-uncased and that works just as well. After trying various bert architectures,
bert, distilbert, albert, distilroberta and distilroberta_extra_linear, we found distilroberta_extra_linear
gave better performance over the given task in medical domain dataset.

**Our Implementation**

• First Step - Evaluating performance of the SQUAD finetuned BERT-QA model on medicalQA.
• Second Step - SQUAD finetuned BERT-QA model on medicalQA.
• Evaluating model performance on Fine-tuned model with medicalQA dataset
