# Decision-Tree
This repository helps me to understand the background mathematics of how Decision Tree works.  
The codeing part is based on [lazy_programmer](https://github.com/lazyprogrammer/machine_learning_examples)  

## We will start to introduce some basic theory behind Decision-Tree
***
### Orthoganal:
1. In Decision Tree, it works by cutting the space piece by piece.
2. For example, if we have x1 = height and x2 = weight, our goal is to classify if the person is male or female.
3. We will first want to choose a split that maximizes reduction in uncertainty.(It's about the theory: __*Information Entropy*__. We will explain it later.)
4. Suppose we find out that if height is over or under 160cm maximized reduction in uncertainty, then we will make a split in 160cm.
5. Then we will have two groups, one for height below 160cm and one for height upon 160cm.
6. For each group we still have to choose a splot that maximizes reduction.
