## Part 3: Layout Enrichment for Better Projection Analysis

### What is Layout Enrichment?
To help you better understand what the scatterplot is showing, we add a color map (like a choropleth map) as a background. This color map provides extra information about the true (original) distances between points, based on the high-dimensional data.

#### How the Color Map Works:
The color map shows two types of distortions in the scatterplot: areas where points look further apart than they originally are (tears) and areas where points look closer together than in the original space (false neighbors).
- **White areas:** Points here are close together in both the scatterplot *and* the original space.
- **Green areas:** Points are torn apart in the scatterplot. In the original space, they are closer together.
- **Purple areas:** Points are false neighbors in the scatterplot. In the original space, they are further apart.
- **Black areas:** Points here are shuffled in the scatterplot. In these areas both tearing and false neighbors occur.

<img src="./projection-analysis/assets/tutorial_images/checkviz_4_clusters_no_label.png" width="600px" height="auto">

### Examples to Help You Understand:

#### Example 1: Different True Distances Between Clusters
In the scatterplot below there are three visible clusters (yellow, blue, and purple). They appear to be equally spaced apart. However, the color map in the background shows:
- The area between the blue cluster and the purple cluster is mostly purple—so, the blue cluster and the purple cluster are actually farther apart than they seem.
- The area between the yellow cluster and the purple cluster is mostly white—so, the yellow cluster and the purple cluster are closer to each other.

<img src="./projection-analysis/assets/tutorial_images/checkviz_3_clusters.png" width="600px" height="auto">

#### Example 2: Clusters with Similar 2D Density but Different True Densities
In the scatterplot below the blue cluster and the yellow cluster look equally dense (points equally packed). But the color map shows:
- The areas within the blue cluster are mostly purple, its points are actually less close together than they seem.
- The area within the yellow cluster is mostly white and green—so its density reflects the true density in the original data.
- This tells us that the blue cluster is actually much sparser than the yellow cluster, even though the scatterplot alone would not reveal this.

<img src="./projection-analysis/assets/tutorial_images/checkviz_2_clusters.png" width="600px" height="auto">