# Cross_encoder
How Cross encoder models work?
While I was working on a project related to search relevancy in which the goal is to find the best matching topics related to the query, I happened to read across cross-encoder model.  It is an interesting feature to use for finding the closest topics according to the query topic. Traditional popular approach to find the best list of searches is to compute the cosine similarity between word embeddings of the query and all the topics. This is a simple and intutive technique to find the best macthes. However, once we get the top 100 matches based on cosine similarity, there is another way to find the best match. It is like getting job opportunities in data science first and then finding the best one which fits your skills and background.

Once we have list of 100 topics by computing word embeddings and cosine similarity, we take these 100 topics and then take each topic and the query as a pair. We pass these two into a cross-encoder simultaneously which then finds the association between the query and topic as the pair. This happens for all the pair of topics and query. Then the pairs are reranked based on the similarity score. This finds a better relation than finding cosine similarity between the query and all documents as in first method because the transformation happens simultaneously and relation is found at the same time. The pairs of topics are then ranked which is called reranking because it happens again, first while computing cosine similarity and secondly in this method. 

Cross encoder works best when the list of topics are small in number say 50 or 100 because words of topics and query are together so computation will be heavy if number of topics are large. 
