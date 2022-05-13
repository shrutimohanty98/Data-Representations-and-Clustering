# Data Representations and Clustering

Machine learning algorithms are applied to a wide variety of data, including text and images.
Before applying these algorithms, one needs to convert the raw data into feature representations
that are suitable for downstream algorithms. In the previous project, we studied feature extraction
from text data, and the downstream task of classification. We also learned that reducing the
dimension of the extracted features often helps with a downstream task.

In this project, we explore the concepts of feature extraction and clustering together. In an
ideal world, all we need are data points – encoded using certain features– and AI should be
able to find what is important to learn, or more specifically, determine what are the underlying
modes or categories in the dataset. This is the ultimate goal of General AI: the machine is
able to bootstrap a knowledge base, acting as its own teacher and interacting with the outside
world to explore to be able to operate autonomously in an environment.

We first explore this field of unsupervised learning using textual data, which is a continuation
of concepts learned in Project 1. We ask if a combination of feature engineering and clustering
techniques can automatically separate a document set into groups that match known labels.

Next we focus on a new type of data, i.e. images. Specifically, we first explore how to
use “deep learning” or “deep neural networks (DNNs)” to obtain image features. Large neural
networks have been trained on huge labeled image datasets to recognize objects of different
types from images. For example, networks trained on the Imagenet dataset can classify more
than one thousand different categories of objects. Such networks can be viewed as comprising
two parts: the first part maps a given RGB image into a feature vector using convolutional
filters, and the second part then classifies this feature vector into an appropriate category, using
a fully-connected multi-layered neural network (we will study such NNs in a later lecture). Such
pre-trained networks could be considered as experienced agents that have learned to discover
features that are salient for image understanding. 

Can one use the experience of such pretrained agents in understanding new images that the machine has never seen before? It is akin
to asking a human expert on forensics to explore a new crime scene. One would expect such
an expert to be able to transfer their domain knowledge into a new scenario. In a similar
vein, can a pre-trained network for image understanding be used for transfer learning? One
could use the output of the network in the last few layers as expert features. Then, given a
multi-modal dataset –consisting of images from categories that the DNN was not trained for–
one can use feature engineering (such as dimensionality reduction) and clustering algorithms
to automatically extract unlabeled categories from such expert features.

For both the text and image data, one can use a common set of multiple evaluation metrics
to compare the groups extracted by the unsupervised learning algorithms to the corresponding
ground truth human labels.
