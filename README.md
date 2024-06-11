# Cross_encoder
How Cross encoder models work?
While I was working on a project related to search relevancy in which the goal is to find the best matching topics related to the query, I happened to read across cross-encoder model which is an interesting feature to use for finding the closest topics according to the query topic. Traditional popular approach to find the best list of searches is to compute the cosine similarity between word embeddings of the query and all the topics. This is a simple and intutive technique to find the best macthes. However, once we get the top 100 matches based on cosine similarity, there is another way to find the best match. It is like getting job opportunities in data science first and then finding the best one which fits your skills and background.

Once, we have list of 100 topics
