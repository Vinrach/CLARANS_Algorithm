# CLARANS: A Method for Clustering Objects for Spatial Data Mining
Raymond T. Ng and Jiawei Han, Member, IEEE Computer Society

# Abstract: 
Spatial data mining is the discovery of interesting relationships and characteristics that may exist implicitly in spatial
databases. To this end, this paper has three main contributions. First, we propose a new clustering method called CLARANS, whose
aim is to identify spatial structures that may be present in the data. Experimental results indicate that, when compared with existing
clustering methods, CLARANS is very efficient and effective. Second, we investigate how CLARANS can handle not only points
objects, but also polygon objects efficiently. One of the methods considered, called the IR-approximation, is very efficient in clustering
convex and nonconvex polygon objects. Third, building on top of CLARANS, we develop two spatial data mining algorithms that aim to
discover relationships between spatial and nonspatial attributes. Both algorithms can discover knowledge that is difficult to find with
existing spatial data mining algorithms.

# Description: 
Re-implemented the CLARANS clustering algorithm in Python for spatial data analysis, using Matplotlib for visualization.
Demonstrated strong analytical and programming skills in machine learning model training and data mining.

# Problem Statement:
In the context of university admissions, it is essential for institutions to understand the patterns and relationships between the number of students applying, the number of acceptance letters issued, and the actual enrollment figure. This can help universities optimize their admission strategies, manage resources, and predict future enrollment trends.

The problem involves clustering universities based on two primary factors:
1. Number of applications accepted by each university.
2. Number of students who enrolled after receiving acceptance letters.

The goal is to group universities into clusters that exhibit similar behavior in terms of these two variables, helping identify patterns such as which universities have higher conversion rates and which ones struggle with enrollment despite a high number of acceptance letters.

# Code Explanation:
1. Data Preprocessing: The data is cleaned by dropping unnecessary columns and any missing values are checked. We create a scatter plot to visualize the relationship between the number of accepted applications and the number of students enrolled
2. Clarans Algorithm:
-> Initialization: Randomly select a set of initial medoids (central points).
-> Cluster Assignment: For each medoid, assign data points to the nearest medoid, calculating the Euclidean distance between the points and the medoids.
-> Cost Calculation: Calculate the total cost (sum of distances between points and their closest medoid) for the current clustering configuration.
-> Randomized Neighbor Search: The algorithm explores random neighboring configurations (by swapping medoids with non-medoids) to see if a better solution (lower cost) can be found. If a better solution is found, it becomes the current solution.
-> Iteration: The process is repeated for a fixed number of neighbors and local minima to ensure that a good solution is reached.
3. Hyperparameter Tuning: A grid search approach is used to identify the best combination of hyperparameters by running the CLARANS algorithm for each combination and comparing the resulting costs.
4. Best Cluster Identification: After tuning the hyperparameters, the best medoids and cluster assignments are identified. A visualization of the clusters is created.
5. Results: The optimal number of clusters is determined to be 6, and the best clustering configuration minimizes the overall cost function to 337,643,399.

# How the Problem Was Solved Using CLARANS:
By applying the CLARANS algorithm to this dataset, the universities were grouped into distinct clusters based on the relationship between applications accepted and students enrolled. This allowed us to identify patterns and group universities with similar admission behaviors, helping address the problem of understanding how effectively universities convert accepted applicants into enrolled students.

The CLARANS algorithm was particularly useful for this problem because:
Randomized Search: It efficiently explored various potential clusters, allowing us to find a solution that minimizes the overall cost (distance between points and their medoids).
Scalability: Since CLARANS is more scalable than traditional k-medoids, it handled the large dataset well and provided optimal results.
Interpretability: The results of the clustering can be easily interpreted by universities to better manage their admissions process and improve their enrollment rates.# 


