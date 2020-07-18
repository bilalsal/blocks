# Visualizing Classification Structure of Large-scale Classifiers

This project aims to visualize class similarities in large-scale classifiers such as deep neural networks.
These similarities usually define a hierarchical structure over the classes.
Understanding this structure helps explain the classifier's behaviour and it errors because it largely influences the features the classifier learns.

## Example Notebook
Explore the classification structure in [MIT Places365](http://places2.csail.mit.edu/), classified using ResNet-18 as implemented in PyTorch.
<br/>
[View Jupyter Notebook](Places365_example.ipynb)

## 3-min Talk
[![Spotlight Talk @ICML 2020 WHI Workshop](https://img.youtube.com/vi/yat1Y5Tu8AI/0.jpg)](https://www.youtube.com/watch?v=yat1Y5Tu8AI)


## Example of Classification Structure
Below are class similarity matrices computed for two large-scale classifiers.

### AudioSet Class Similarity Matrix
Each row / column is one of 527 classes (audio events) from [Google's AudioSet](https://research.google.com/audioset/).
The dataset is multi-labeled with high class imbalance.
The major similarity groups exposed by visualizing the matrix are music, inside, organism, and outside.
This suggests that the CNN develops shared features that characterize each of these groups. 

<p align="center">
<img src="/example_images/AudioSet_Class_Similarity.png" alt="drawing" width="700"/>
</p>

### VGGFace Class Similarity Matrix
Each row / column is one of 2622 classes (celebrities) from [Oxford's VGGFace Dataset](https://www.robots.ox.ac.uk/~vgg/data/vgg_face/).
Male vs. female celebrities define the major two blocks in the matrix.
Prominent subgroups in these blocks are based on wrinkles and hair / skin color.
Chromaticity defines two of these sub-groups (split marked in red), and indicates that the CNN uses unreliable features to recognize the corresponding celebrities.


<p align="center">
<img src="/example_images/VGGFace_Class_Similarities.png" alt="drawing" width="900"/>
</p>

## Article and BibTex

[Here](https://arxiv.org/abs/2007.06068) is an article describing how we compute class similarity and how we visualize the class similarity matrix, with examples on five datasets. The article is accepted to the [WHI Workshop @ICML 2020](https://sites.google.com/view/whi2020).

[Here](/poster_XC2020.pdf) is a poster summarizing the work, presented at the [XC Workshop @ICML 2020](http://manikvarma.org/events/XC20).

You can cite the article as follows:
<br/>
```
@inproceedings{whi2020visualizing,
  title={Visualizing Classification Structure of Large-Scale Classifiers},
  author={Bilal Alsallakh and Zhixin Yan and Shabnam Ghaffarzadegan and Zeng Dai and Ren, Liu},
  booktitle={ICML Workshop on Human Interpretability in Machine Learning (WHI)},
  year={2020},
}
```

## Thank You

If you have any suggestions or feedback, we will be happy to hear from you!
