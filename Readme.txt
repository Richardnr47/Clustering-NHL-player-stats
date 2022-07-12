Question to answer:
Is it possible to cluster and get some insights about NHL hockey players by using statistics from games and information as height/weight?

The dataset contains multiple csv-files, which become to large to upload, but it is possible to download it here:
https://www.kaggle.com/datasets/martinellis/nhl-game-data

I have choosen to use the K-means algorithm to find clusters in the data.

K-means need a predefined number of clusters (k) input as parameter, that k defines how many clusters you want to split your data into, in my case four clusters.

In the next step the algorithm puts these numbers(k) in to so called centroids on randomized datapoints.
There after K-means measure the distance between every datapoint and every centroid so every datapoint can be connected to closest centroid.
Last step is to measure the mean of every cluster.
This will be repeated until the algorithm can not find any more alteration from previous iteration.

How I choose number of clusters:
I have chosen to use the function funktionen KElbowVisualizer, this function is based of the 'Elbow-method', it will show an indication of what could be an optimal number of clusters.
KElbowVisualizer works fine with K-means because you can define what kind of clustering-model you will use (in this case 'KKmeans') and also a range of number of clusters that will be tested.
(I have chosen 1-10).
KElbowVisualizer then displays a graph where the optimal number of clusters is indicated where the value of the calculation clearly breaking the downspeed and planes out.
There is also a line that indicates the time for the algorithm to make its predictions.
