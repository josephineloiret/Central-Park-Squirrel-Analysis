# Central Park Squirrel Census Analysis

This project analyzes the 2018 Central Park Squirrel Census data to predict squirrel energy expenditure based on geographical location using K-Nearest Neighbors (KNN) regression. The analysis includes comprehensive data preprocessing, feature engineering, exploratory visualizations, and geographical mapping of squirrel behavior patterns across Central Park in New York City. The project demonstrates machine learning techniques for spatial regression and provides insights into how squirrel activity levels vary by location within the park.

## How to Run

### Prerequisites

Install the required Python packages:

```bash
pip install pandas matplotlib seaborn plotly folium scikit-learn numpy scipy geojsoncontour gdown jupyter
```

### Setup

1. Clone or download this repository
2. The data file (`2018_Central_Park_Squirrel_Census_-_Squirrel_Data.csv`) will be automatically downloaded when you run the notebooks, or you can manually download it using:
   ```bash
   gdown 13atAjRD7sIt0pv2Y__ytYvVWCKo4RPn_ -O archive.zip
   unzip archive.zip
   ```

### Running the Notebooks

Open and run each notebook in order using Jupyter:

```bash
jupyter notebook
```

Or execute all notebooks programmatically:

```bash
jupyter nbconvert --to notebook --execute "CSCI183_FinalProject_DataProcessing (1).ipynb"
jupyter nbconvert --to notebook --execute "CSCI183_FinalProject_FeatureVisualization (1).ipynb"
jupyter nbconvert --to notebook --execute "CSCI183_FinalProject_GeographicalMapVisualizations.ipynb"
jupyter nbconvert --to notebook --execute "CSCI183_FinalProject_KNNRegressionImplementation.ipynb"
```

**Note:** The notebooks should be run in order as they build upon each other. Some notebooks contain interactive visualizations (Plotly/Folium maps) that work best when opened in Jupyter Notebook or JupyterLab.

## File Descriptions

### `CSCI183_FinalProject_DataProcessing (1).ipynb`
This notebook handles the initial data preprocessing and feature engineering. It downloads the squirrel census dataset, removes insignificant columns, and creates a target variable called `Energy_expenditure` that quantifies squirrel activity levels. The energy expenditure metric assigns values based on activity types: Chasing (6), Running (5), Climbing (3), Foraging (2), and Eating (1), with special handling for activities listed in the "Other Activities" column.

### `CSCI183_FinalProject_FeatureVisualization (1).ipynb`
This notebook creates exploratory data visualizations to understand the distribution of features in the dataset. It generates bar charts showing the value counts for different activity categories (Running, Chasing, Climbing, Eating, Foraging), primary fur colors, and age groups. It also includes scatter plots to visualize the spatial distribution of activities across Central Park.

### `CSCI183_FinalProject_GeographicalMapVisualizations.ipynb`
This notebook creates interactive geographical visualizations using Plotly and Folium. It generates a scatter map showing the distribution of squirrel fur colors across Central Park and a density heatmap visualizing energy expenditure patterns. The notebook also includes preprocessing steps to create the energy expenditure feature and prepares the data for machine learning modeling.

### `CSCI183_FinalProject_KNNRegressionImplementation.ipynb`
This notebook implements the K-Nearest Neighbors regression model to predict squirrel energy expenditure based on geographical coordinates (X and Y). It includes hyperparameter tuning to find the optimal number of neighbors (k=15), evaluates model performance using mean squared error, checks for overfitting by comparing train and test errors, and visualizes the decision boundaries on both static plots and interactive Folium maps. The model achieves a training MSE of approximately 5.25 and test MSE of 6.37.

### `2018_Central_Park_Squirrel_Census_-_Squirrel_Data.csv`
The raw dataset containing observations of squirrels in Central Park, including their locations, activities, physical characteristics, and behaviors recorded during the 2018 census.


