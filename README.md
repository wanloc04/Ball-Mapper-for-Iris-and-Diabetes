# Ball-Mapper-for-Iris-and-Diabetes
# Ball Mapper Analysis on Iris and Diabetes Datasets

This repository presents an application of the Ball Mapper algorithm, a method from Topological Data Analysis (TDA), to two publicly available datasets: the Iris dataset and the Pima Indians Diabetes dataset. The objective is to explore the topological structure of the data and to investigate whether meaningful patterns or separations between classes can be observed through the Ball Mapper representation.

## Datasets

1. Iris Dataset:
The Iris dataset is a classical dataset in machine learning, containing 150 samples of iris flowers, each described by four features: sepal length, sepal width, petal length, and petal width. The samples are equally distributed among three species: Iris Setosa, Iris Versicolor, and Iris Virginica.

2. Pima Indians Diabetes Dataset:
This dataset originates from a study conducted on Pima Indian women and contains 768 records. Each record includes eight medical attributes (such as glucose concentration, body mass index, and insulin level) and a binary outcome variable indicating the presence or absence of diabetes.

## Ball Mapper Algorithm

The Ball Mapper algorithm constructs a simplicial representation of a high-dimensional dataset by covering the data space with overlapping balls of a fixed radius. A graph is then created, where each node corresponds to a ball and edges are drawn between nodes if their respective balls share any data points. This construction provides a topological summary of the data that is robust to noise and capable of capturing clusters, boundaries, and holes in the dataset.

The algorithm proceeds as follows:
- Choose a radius epsilon and a distance metric (typically Euclidean).
- Select a set of centers that cover the dataset with balls of radius epsilon.
- Assign each data point to the balls it lies within.
- Construct the Ball Mapper graph based on shared data points across balls.

## Methodology

For both datasets, the following steps are performed:
- Data preprocessing: missing values are handled and features are normalized.
- Construction of the Ball Mapper graph using selected features.
- Coloring of the nodes using the class labels (species for the Iris dataset, diabetic outcome for the Diabetes dataset) to highlight the distribution of classes in the topological space.

## Results

In the case of the Iris dataset, the Ball Mapper graph reveals clear separation between the Iris Setosa class and the other two species, which form more intertwined structures. This observation aligns with known linear separability properties of the dataset.

For the Diabetes dataset, the Ball Mapper graph provides insight into regions of the feature space associated with positive or negative diabetes outcomes. Certain regions contain a high density of diabetic patients, suggesting potential subpopulations or risk profiles.

## Applications and Future Work

The use of Ball Mapper provides a complementary perspective to classical dimensionality reduction and clustering methods. Future work may include:
- Multi-scale Ball Mapper analysis by varying the radius parameter.
- Integration with Rough Set or Fuzzy Set theory for enhanced interpretability.
- Application to larger or more complex biomedical datasets.

## Repository Structure

- `data/`: Contains the raw CSV files for the Iris and Diabetes datasets.
- `ball_mapper/`: Python scripts for constructing Ball Mapper graphs for each dataset.
- `utils/`: Helper functions for preprocessing and visualization.
- `images/`: Optional directory for saving generated figures.
- `README.md`: This documentation file.
- `requirements.txt`: List of required Python libraries.

## Requirements

This project requires Python 3.8 or later and the following Python packages:
- pandas
- numpy
- matplotlib
- scikit-learn
- ballmapper (if not available on PyPI, a local implementation should be provided)

All dependencies can be installed via:

