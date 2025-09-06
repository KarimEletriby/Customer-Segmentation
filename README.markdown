# Customer Segmentation

## Project Overview
This project performs customer segmentation using unsupervised Machine Learning (KMeans clustering) on mall customer data. It explores the dataset, preprocesses features, determines the optimal number of clusters using the Elbow Method, applies KMeans clustering based on annual income and spending score, and visualizes the results.

## Dataset
The dataset is the **Mall Customers** dataset (`Mall_Customers.csv`), available from [Kaggle](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python). It includes:
- `CustomerID`: Unique customer identifier
- `Gender`: Gender (Male/Female)
- `Age`: Age of the customer
- `Annual Income (k$)`: Annual income in thousands of dollars
- `Spending Score (1-100)`: Score assigned by the mall based on customer behavior and spending nature

Note: The dataset file is not included in the repository. Download it from Kaggle and place it in the project directory (or update the path in the notebook).

## Project Structure
- `Project 3 (Customer Segmentation).ipynb`: The main Jupyter notebook containing data exploration, preprocessing, clustering, and visualizations.
- `README.md`: This file.
- (Optional) `requirements.txt`: List of dependencies.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/customer-segmentation.git
   cd customer-segmentation
   ```

2. Set up a virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
   Or manually:
   ```bash
   pip install pandas matplotlib numpy seaborn scikit-learn
   ```

## Data Preprocessing
- Check for missing values and duplicates (none found).
- Explore data: Summary statistics, histograms for age, income, and spending score; scatter plot of income vs. spending score; countplot for gender.
- Encode categorical variable `Gender` using `LabelEncoder`.
- Select features for clustering: `Annual Income (k$)` and `Spending Score (1-100)`.

## Clustering
- Use the Elbow Method to determine the optimal number of clusters (found to be 5).
- Apply KMeans clustering with 5 clusters.
- Add a `Cluster` column to the dataset.
- Visualize clusters using a scatter plot colored by cluster labels.

## Usage
1. Download `Mall_Customers.csv` and place it in the project root (or update the path in the notebook).
2. Open and run the Jupyter notebook:
   ```bash
   jupyter notebook "Project 3 (Customer Segmentation).ipynb"
   ```
3. The notebook will:
   - Load and explore the data.
   - Preprocess features.
   - Determine optimal clusters and apply KMeans.
   - Visualize results, including cluster means and distributions.

## Results
- Optimal clusters: 5.
- Cluster analysis includes mean values for age, annual income, and spending score per cluster.
- Visualizations: Histograms, scatter plots, and countplots to interpret customer segments (e.g., high-income low-spenders, low-income high-spenders).

## Future Improvements
- Incorporate more features (e.g., age or gender) into clustering for multi-dimensional segmentation.
- Use other clustering algorithms like DBSCAN or Hierarchical Clustering for comparison.
- Evaluate clusters using silhouette score or other metrics.
- Deploy as a web app for interactive segmentation.
- Handle larger datasets with dimensionality reduction (e.g., PCA).

## Contributing
Feel free to fork the repository and submit pull requests for improvements.

## License
This project is licensed under the MIT License.

## Contact
For questions, open an issue on GitHub.