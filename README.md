# Visualizing Classification Structure of Large-scale Classifiers

## Example Notebook
Explore the classification structure in [MIT Places365](http://places2.csail.mit.edu/), classified using ResNet-18 as implemented in PyTorch.
<br/>
[View Jupyter Notebook](Places365_example.ipynb)

## Example of Classification Structure
Below are similarity matrix of two large-scale classification problems.

### AudioSet Class Similarity Matrix
Each row / column is one of 527 classes (audio events) from [Google's AudioSet](https://research.google.com/audioset/).
The dataset is multi-labeled with high class imbalance.
The major similarity groups exposed by visualizing the matrix are music, inside, organism, and outside.
This suggests that the CNN develops shared features that characterize each of these groups. 

<p align="center">
<img src="/AudioSet_Class_Similarity.png" alt="drawing" width="700"/>
</p>

### VGGFace Class Similarity Matrix
Each row / column is one of 2622 classes (celebrities) from [Oxford's VGGFace Dataset](https://www.robots.ox.ac.uk/~vgg/data/vgg_face/).
Male vs. female celebrities define the major two blocks in the matrix.
Prominent subgroups in these blocks are based on wrinkles and hair / skin color.
Chromaticity defines two of these sub-groups (split marked in red), and indicates that the CNN uses unreliable features to recognize the corresponding celebrities.


<p align="center">
<img src="/VGGFace_SImilarities.png" alt="drawing" width="900"/>
</p>

