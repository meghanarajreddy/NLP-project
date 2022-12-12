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
