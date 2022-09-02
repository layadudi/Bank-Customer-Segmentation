# Bank-Customer-Segmentation



# EDA 
 # Introduction
  
  It is done to find Dataset has 7 variables and 210 instances. It is evident that no null values are present in the data. 

   Using the describe() function in Python, a summary of all the parameters can be obtained.
   Using the .duplicated() function, it is found that the given dataset has no duplicate values.
   
   Univariate analysis can be done using dist plot
   Multivariate analysis can be done using a heat map
   -The heatmap shows quite a few strong positive correlations between the fields like spending and advance payments, advance payments & current balance, credit limit 
     & spending, spending & current balance, credit limit & advance payments, Max_spent_in_single_shopping & current balance

  Pairplot is used to find a correlation between all variables in the dataset

  Scaling is a method that converts all the variables from various scales of measurement to a single scale of measurement. The columns Spending and Advance Payments had 
        varied values and now the scaled data makes the whole dataset proportionate.
 
###     Hierarchical clustering performed using the following methods:
#           1. Ward’s method 
#           2. Average method
            
         The first dendrogram created using the ward method shows all the points grouped into different clusters. 
         To arrive at an optimal number of clusters, the truncate_mode function is used. 
         The data points are clustered into the 3 clusters using the fcluster function and the maxclust criterion. 
         The cluster frequency, as well as the cluster profile, has also been depicted.
         
        -   Using the average method of clustering, and distance criterion, it can be noticed that 4 clusters are formed.
 
        Both methods showed similar results with minor variations in the means. 
        Cluster grouping can be 3 or 4 based on the criterion picked but 3 clusters is a better option in my opinion.
        And three group cluster solution gives a pattern based on high/medium/low spending with max_spent_in_single_shopping (high-value item) 
        and probability_of_full_payment (payment made)
        
####   K MEANS

       Randomly select 3 clusters and look at the distribution of the clusters according to n_clusters. 
       We then apply K-Means on scaled data, after which the clear cluster output is obtained for each observation in the dataset.
       
       To find the optimal number of clusters, the K-elbow curve method can be used. Initially, WSS is calculated and then the K-elbow curve is plotted.

       A cluster loop from 1 to 11 is created to check for the right inertia value. 
       The drop in value declined after the third cluster and hence the third cluster is taken into consideration. The curve plotted also depicts the same

   Using the K- Mean’s method we can conclude that 3 clusters are optimal since there is no huge drop in inertia values.
       The elbow curve seems to show similar results. The silhouette score of the K means is also very less value that indicates all the data points are properly clustered to          the cluster.  There is no mismatch in the data points with regards to clustering.

##### CONCLUSION : 

Cluster profiles have been plotted alongside every type of clustering above. According to the K-means clustering profile:
Cluster 0 = Medium Spending group
Cluster 1 = Low Spending group 
Cluster 2 = High Spending group


## Cluster group 0: Medium Spending Group – These customers are customers who are paying bills and purchasing items while maintaining comparatively good credit scores. So,                                                  increasing the credit limit or lowering the interest rate could be a good motivation. Promoting premium cards would also increase                                                transactions. The chances of increasing the spending habits could be achieved by giving offers and discounts on premium e-commerce                                               sites, travel portals, travel airlines/hotels, as this might encourage them to spend more.
 
 
## Cluster group 1: Low Spending Group – These customers should be given constant reminders for payments and offers should be available upon early payments to improve the                                                 payment rates as well as credit score. Increasing their spending habits by tying up with grocery stores, utilities (electricity, phone,                                          gas, others) could be another way to attract such customer groups since the frequency of this group is highest.

## Cluster group 2: High Spending Group – Giving any reward points might increase their purchases. Maximum max_spent_in_single_shopping is high for this group, so they can be                                             offer a discount/offer on the next transactions upon full payment. Increase their credit limit and this might increase spending habits.                                           Give loan against the credit card, as they are customers with good repayment records. Tie up with luxury brands, which will drive more                                           one_time_maximun spending.



