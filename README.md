# Gaussian-Mixture-Models
This project generates Univariate Gaussian mixtures and then performs clustering to get the approximate Gaussian mixtures. It does this by calculating their Mean, Standard Deviation and mixing ratios.

# Workflow
This code generates Univariate Gaussian Mixtures with the following parameters(number of gaussians, mean-range, sd-range, samples per gaussian). Means & Sd's generated have a spacing of at least 100 and 1 respectively.

Later, incremental K-means is used to find the starting means for each of the Gaussians which are then provided to EM-algorithm to estimate the sd's and mixture ratios for each Gaussian. 

At each cobnvergent exectution of the EM-algorithm, we also calculate the mutual information(MI) of the last Gussian w.r.t. all the previous Gaussians. Finally, if we get a Gaussian with positive MI, we stop.

# References
This project used Warren Weckesser's contribution on Stack Overflow for spaced-random generator(https://stackoverflow.com/questions/53565205/how-to-generate-random-numbers-with-each-random-number-having-a-difference-of-at).

Multiple other papers were referred to implement this project. A list of all the papers is given below:

The global k-means clustering algorithm
https://www.sciencedirect.com/science/article/abs/pii/S0031320302000602

The Estimating Optimal Number of Gaussian Mixtures
Based on Incremental k-means for Speaker Identification
https://pdfs.semanticscholar.org/ce12/8a4580dae6ea04db9ef58a7ba065b07f2c6e.pdf

Modified global k-means algorithm for minimum sum-of-squares clustering problems
https://www.sciencedirect.com/science/article/abs/pii/S0031320308001362

Fast modified global k-means algorithm for incremental cluster construction
https://www.sciencedirect.com/science/article/abs/pii/S0031320310005029

# Future Work
Plan to use fast GMM with kd-tree to speeden incremental k-means algorithm.
