# SOM-for-clustering-digits

Introduction
In this project, we have used a data set with examples of handwritten digits. There are 1797 examples and each example has 64 pixels as inputs and 1 output (0,1,2,3,... or 9).

Information about the dataset (from https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_digits.html):

Classes: 10
Samples per class: ~180
Samples total: 1797
Dimensionality: 64
Features: integers 0-16

Hyperparameters:

x: x dimension of the SOM
y: y dimension of the SOM
input_len: number of the elements os the vectors in the input
sigma: spread of the neighborhood function (sigma(t) = sigma / (1+t/T))
learning_rate (learning_rate(t)=learning_rate/(1+t/T))
decay_function (function that reduces learning_rate and sigma at each interaction)
neighborhood_function (default=gaussian): function that weights the neighborhood of a position in the map
topology (rectangular (default) or hexagonal)
activation_distance: distance used to active the map (euclidean (default), consine,manhattan, chebyshev)

Definitions

Reference: Evaluating Self-Or aluating Self-Organizing Map Quality Measur ganizing Map Quality Measures as Conv es as Convergence Criteria (from Gregory T. Breard )

Quantization error: is a measure of the average distance between the data points and the map nodes to which they are mapped, with smaller values indicating a better fit.

Topographic error: TE is calculated by finding the best-matching and second-best-matching neuron in the map for each input and then evaluating the positions. If the nodes are next to each other, then we say topology has been preserved for this input. If not, then this is counted as an error. The total number of errors divided by the total number of data points gives the topographic error of the map.
