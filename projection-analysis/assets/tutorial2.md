## Part 2: Understanding Dimensionality Reduction Techniques

### Why Do We Use Dimensionality Reduction?
In real-world data, there are often more than just two features or dimensions—sometimes dozens or even hundreds! Dimensionality reduction is a technique used to simplify this high-dimensional data into two dimensions (for visualization), so we can see it in a scatterplot.

**Main Goal:** To show patterns and groupings (clusters) in the data, even when it has many dimensions.

### Limitations and Important Points
**Possible Distortions:** Reducing the number of dimensions sometimes distorts the distances between points and the density of clusters. This means:
  - Points that look close in the scatterplot may not be truly close in the original (high-dimensional) data.
  - Points that were neighbors before may not appear together in the 2D scatterplot.

**Always use caution:** Some relationships you see in the scatterplot may not reflect the real situation in the original data.

**[Placeholder: Animated example showing high-dimensional points, then their 2D projection, with lines/indicators for misleading neighbor relationships]**

<img src="./projection-analysis/assets/DR_explanation.png" width="800px" height="auto">