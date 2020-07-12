# Visualizing Classification Structure of Large-scale Classifiers

## Example Notebook
Explore the classification structure in Places365, classified using resnet18.
<br/>
[Jupyter Notebook](Places365_example.ipynb)

## AudioSet Class Similarity Matrix
Each row / column is one of 527 classes (audio events).
The dataset is multi-labeled with high class imbalance.
The major similarity groups exposed by visualizing the matrix are music, inside, organism, and outside.
This suggests that the CNN develops shared features that characterize each of these groups. 

![AudioSet Class Similarity Matrix](/AudioSet_Class_Similarity.png  =500)

## VGGFace Class Similarity Matrix
![VGGFace Class Similarity Matrix](/VGGFace_SImilarities.png)
Each row / column is one of 2622 classes (celebrities).
Male vs. female celebrities define the major two blocks in the matrix.
Prominent subgroups in these blocks are based on wrinkles and hair / skin color.
Chromaticity defines two of these sub-groups (split marked in red), and indicates that the CNN uses unreliable features to recognize the corresponding celebrities.
