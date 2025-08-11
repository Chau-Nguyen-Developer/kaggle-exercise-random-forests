# What makes a random forest different than a decision tree  
### Q: What is a random forest?
Answer: Random forest is a collection of many decision trees. Each tree is trained slightly differently  

### Q: How the difference between each tree is achieved?  
Multiple trees were created, and each uses:  
1. Random subsets of data (bootstrapping)
2. Random subsets of featues at each split

### Q: How the prediction is reach?  
1. Classification? -> use majority votes among all trees
2. Regression? -> average the predicted number among trees
   
### Q: Why use random forest instead of just a decision tree?  
1. Random forest helps reduce overfitting.  
2. This is the dilemma of using just use a decision tree: it is hard to _balance_ between overfitting and underfitting.  
3. If a tree very deep with a lot of leaves -> will overfit because each decision comes only from a few data points at its leaves.  
4. If a tree is shallow with just a few leaves --> will perform poorly because it has not captured enough the distinctions in raw data.  

### Q: What is bootstrapping?  
1. Bootstrapping means randomly sampling with replacement from original data to create new datasets. "With replacement" means after picking a data point, we put it back into the dataset before picking the next one, giving old data point a second chance to be picked. This means some points will appear multiple times, and some points do not show up any time.

2. Purpose? --> Create multiple training datasets, so each model sees a slightly different view of the data.

### Q: I want to see the code. 
Please [click here](exercise-random-forests.ipynb) or check out the .ipynb file above. 
