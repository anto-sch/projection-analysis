## Part 3: Layout Enrichment for Better Projection Analysis

### What is Layout Enrichment?
To help you better understand what the scatterplot is showing, we add a color map (like a heatmap) as a background. This color map provides extra information about the true (original) distances between points, based on the high-dimensional data.

#### How the Color Map Works:
- **Black areas:** Points here are close together in both the scatterplot *and* the original space.
- **Red/Yellow/White areas:** Points are further apart in the original space—even if they look close in the scatterplot. The brighter the color, the greater the distance.

<img src="./projection-analysis/assets/tutorial_images/delaunay_4_clusters_no_label.png" width="600px" height="auto">

### Examples to Help You Understand:

#### Example 1: Different True Distances Between Clusters
In the scatterplot below there are three visible clusters (yellow, blue, and purple). They appear to be equally spaced apart. However, the heatmap in the background shows:
- The area between the yellow cluster and the blue cluster is bright (yellow/white)—so, the yellow cluster and the blue cluster are actually farther apart than they seem.
- The area between the yellow cluster and the purple cluster is dark red—so, the yellow cluster and the purple cluster are closer to each other.

<img src="./projection-analysis/assets/tutorial_images/delaunay_3_clusters.png" width="600px" height="auto">

#### Example 2: Clusters with Similar 2D Density but Different True Densities
In the scatterplot below the blue cluster and the yellow cluster look equally dense (points equally packed). But the color map shows:
- Some areas within the blue cluster are not as black—meaning, its points are actually less close together than they seem.
- The area within the yellow cluster is very black—so its density reflects the true density in the original data.
- This tells us that the blue cluster is actually much sparser than the yellow cluster, even though the scatterplot alone would not reveal this.

<img src="./projection-analysis/assets/tutorial_images/delaunay_2_clusters.png" width="600px" height="auto">