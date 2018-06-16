# RecSys
This is optimized recommender system code from Recommender System Practice. The author of that book is Xiang Liang.(《推荐系统实践--项亮》)
# Environment
A Python 3 virtual environment is required.
# Content
UserCF_acc1.py  user collaborative filter module I based on the original algorithm
UserCF_IIF_acc1.py  user collaborative filter module II based on a revised algorithm
ItemCF_acc1.py  item collaborative filter module I based on the original algorithm
ItemCF_IUF_acc1.py  item collaborative filter module II based on a revised algorithm
LFM_acc1.py latent factor model implemented by gredient descent method
main_acc1.py  main module that imports and executes all the above module, in which transform_random_A method does not consider timestamps and transform_random_B method considers timestamps.
Evaluation.py the same module from the original code.
# Advantage
UserCF_acc1.py is about 2.5 times as fast as the original code with almost the same accuracy 
UserCF_IIF_acc1.py is about 2.5 times as fast as the original code with almost the same accuracy 
ItemCF_acc1.py is about 120 times as fast as the original code with almost the same accuracy 
ItemCF_IUF_acc1.py is about 120 times as fast as the original code with almost the same accuracy 
LFM_acc1.py is about 100 times as fast as the original code, meanwhile its accuracy has been improved by about 16%.
# Example
use user collaborative filter module I based on timestamps with train/test ratio 4.
train, test, user_movie_train, user_movie_test = transform_random_B(ratings, train_size = 0.75)
W = UserCF_acc1.user_similar_matrix(user_movie_train)
result = UserCF_acc1.Recommendation(test.keys(), user_movie_train, W, K=80)
