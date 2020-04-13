To exemplify classification, we used  a Breast Cancer Dataset, which is a dataset donated to the University of California, Irvine (UCI) collection from the University of Wisconsin-Madison. UCI has a large Machine Learning Repository(https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Original%29).

K-Nearest Neighbors
The k-nearest neighbors (KNN) algorithm is a simple, easy-to-implement supervised machine learning algorithm that can be used to solve classification problem
The KNN Algorithm

1.	Load the data
Here, we load in the data, replace the question mark, drop the id column, and then convert the data to a list of lists. Note that we're explicitly converting the entire dataframe to float. For some reason, at least for me, some of the data points were numbers still, but of the string datatype, so that was no good.
2.	Initialize K to your chosen number of neighbors
3. For each example in the data
3.1 Calculate the distance between the query example and the current example from the data.
3.2 Add the distance and the index of the example to an ordered collection
4. Sort the ordered collection of distances and indices from smallest to largest (in ascending order) by the distances
5. Pick the first K entries from the sorted collection
6. Get the labels of the selected K entries

7.  training ,testing and find the ACCURANCY 
we prepare a dictionaries for the training and testing set to be populated. Next, we specify which chunk is the train_data and which is the test_data. We do this by selecting the first 80% as train_data (by doing logic that says to slice the list up to the last 20%), and then we create the test_data by slicing the final 20% of the shuffled data.

we first iterate through the groups (the classes, 2 or 4, also the keys in the dictionary) in the test set, then we go through each datapoint, feeding that datapoint through to our custom k_nearest_neighbors, along with our training data, train_set, and then our choice for k, which is 5
