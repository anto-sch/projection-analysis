## Part 3: Layout Enrichment for Better Projection Analysis

### What is Layout Enrichment?
To help you better understand what the scatterplot is showing, we present a colored matrix next to it. This matrix provides extra information about the true (original) distances between points, based on the high-dimensional data.

#### How the Matrix and its Color Map Works:
- **Cluster labels:** The colors at the side of each row and column indicate which clusters are being referenced. They correspond to the cluster colors in the scatterplot.
- **Black quadrants in the matrix:** Points in these clusters are close together in both the scatterplot *and* the original space.
- **Red/Yellow/White quadrants in the matrix:** Points in these clusters are further apart in the original space—even if they look close in the scatterplot. The brighter the color, the greater the distance.

<img src="./projection-analysis/assets/tutorial_images/matrix_4_clusters_with_label.png" width="600px" height="auto">

### Examples to Help You Understand:

#### Example 1: Different True Distances Between Clusters
In the scatterplot below there are three visible clusters (yellow, blue, and purple). They appear to be equally spaced apart. However, the matrix on the side shows shows:
- The quadrant comparing the yellow cluster and the blue cluster is bright (yellow)—so, the yellow cluster and the blue cluster are actually farther apart than they seem.
- The quadrant comparing the yellow cluster and the purple cluster is red—so, the yellow cluster and the purple cluster are closer to each other.

<img src="./projection-analysis/assets/tutorial_images/matrix_3_clusters.png" width="600px" height="auto">

#### Example 2: Clusters with Similar 2D Density but Different True Densities
In the scatterplot below the blue cluster and the yellow cluster look equally dense (points equally packed). But the quadrants on the diagonal of the matrix shows us the cluster densities in the original space:
- The quadrant of the yellow cluster is very black—so its density reflects the true density in the original data.
- The quadrant of the blue cluster is red, its points are actually less close together than they seem.
- This tells us that the blue cluster is actually much sparser than the yellow cluster, even though the scatterplot alone would not reveal this.

<img src="./projection-analysis/assets/tutorial_images/matrix_2_clusters.png" width="600px" height="auto">