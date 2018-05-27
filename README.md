# Decision-Tree
This repository helps me to understand the background mathematics of how Decision Tree works.  
The codeing part is based on [lazy_programmer](https://github.com/lazyprogrammer/machine_learning_examples)  
***
## We will start to introduce some basic theory behind Decision-Tree

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
![image](https://github.com/alexyin2/Decision-Tree/blob/master/Image/EntropyInformation.png)
5. When the probability of the targets are 0.5 and 0.5, the entropy is 1, which means that its totally uncertain and there's no help for us to predict or guess the target.
6. As one of the targets probability gets lower, the entropy also gets lower, which means that the uncertainty has reduced.

***
## Next we will introduce different ways to split our data

### ID3(Interactive Dichotomiser 3)
1. First, it sets all the attributes as S = {a(1), a(2), ...a(D)).
2. Next, It will find the attributes that best splits data based on having maximum information gain.
3. Notice that is quite important that when using ID3, _**it can split more than once at a time**_, which means that each node can have more than two children.
4. Also remember that this algorithm will remove the attribute after we've used to split the data. In other words, _**each attributes will only be used for one time**_.

### C4.5
1. The main idea of this algorithm is the same as above, which tries to split data based on having maximum information gain.
2. But there are some parts different from ID3.
3. First, this algoirthm __*does not require that an attribute can only be split once*__, which makes it performs better on donut data(data that have different labels in each circle).
4. Second, This algorithm __*restricts that each tree node can only have 0(leaf) or 2 children*__.
***

## Detail steps of running the algorithms
1. First, sort X's for current column in order, sort Y in the corresponding way.
2. Second, find all the boundaries points where Y changes from one value to another.
3. Third, calculate information gain when spliting at each boundaries.
4. Last Keep the split which gives the maximum of information gain.
