Principal Component Analysis is one of the most frequently used concept in data science for dimensionality reduction. 

Here is a simple visual explanation of the eigenvalues and eigenvector(first principal component) 

Blue dots: the initial data on a 2D space

Red dots: the projection of the blue dots onto lines, that are centered at the mean of the data. There many, many such lines. Notice how the red dots are dispersed (spread out) on the rotating line in different ways depending on the position of the line (=vector): on some lines the red dots have great dispersion compared to other positions of the line.

First Principal Component - Eigenvector: That particular position of the rotating line (=vector)-shown in purple-where the red dots (projection of the original blue data) have the biggest dispersion (have the biggest spread out) than any other line i.e. have the greatest variance on the rotating line.

Eigenvalue: the actual variance of the red dots on that line.

Let's say the eigenvalue(explained_variance_ in sklearn) is 80%. It means that if you project all your data to that line, you will be able to reconstruct the points with 80% of accuracy with using only one dimension.
Source: bit.ly/2nd1XeP
