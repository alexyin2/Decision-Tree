# Decision-Tree
This repository helps me to understand the background mathematics of how Decision Tree works.  
The codeing part is based on [lazy_programmer](https://github.com/lazyprogrammer/machine_learning_examples)  

## We will start to introduce some basic theory behind Decision-Tree
***
### Orthogonal:
1. In Decision Tree, it works by cutting the space piece by piece.
2. For example, if we have x1 = height and x2 = weight, our goal is to classify if the person is male or female.
3. We will first want to choose a split that maximizes reduction in uncertainty.(It's about the theory: __*Information Entropy*__. We will explain it later.)
4. Suppose we find out that if height is over or under 160cm maximized reduction in uncertainty, then we will make a split in 160cm.
5. Then we will have two groups, one for height below 160cm and one for height upon 160cm.
6. For each group we still have to choose a splot that maximizes reduction.

### Entropy Information
1. Entropy can be origined by physics, which defined that entropy means the uncertainty of our world.
2. This definition is used in decision tree when we have to split the data by categorical variables or numerical variables.
3. Lets suppose our target is 0 or 1, and we have numerous variables, the algorithm will first split the data depend on the variables that maximizes reduction in uncertainty.
4. We can also use a image to show that how the formula looks like when we only have two targets.
