* **Dataset:** Used the Mall Customer Segmentation dataset.
* **Preprocessing:**

  * Encoded the 'Gender' column numerically.
  * Plotted pairplots using `seaborn` to visually assess the separability of the data.
  * Computed the correlation matrix to understand the relationships between features.
  * Performed Exploratory Data Analysis (EDA) using `ydata-profiling`.
  * Applied `StandardScaler` to normalize the data.
* **Initial Clustering:**

  * Built an initial K-means model with $k = 5$ using the **k-means++** initialization for efficient convergence.
  * Extracted the cluster labels and final centroids.
  * Added the cluster labels to the dataset as a new column named 'cluster'.
  * Visualized the clusters using a color-coded pairplot.
* **Finding the Optimal K:**

  * Applied the **elbow method** by looping $k$ from 2 to 20, recording the inertia at each step, and plotting inertia vs. $k$.
  * Based on the elbow plot, $k = 5$ or $k = 6$ appeared to be potential optimal values.
  * To refine this choice, calculated the **silhouette score** for each $k$ in the same range and plotted the results.
  * Found that the silhouette score peaked at $k = 6$ with a score of approximately **0.454**.
* **Conclusion:**

  * Due to the relatively low silhouette score, the dataset is moderately noisy, indicating some overlap between clusters.
  * Nonetheless, $k = 6$ offers the best efficiency and interpretability for this dataset.
