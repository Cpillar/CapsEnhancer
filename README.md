# CapsEnhencer

**A model for enhanced classification and feature extraction**



## Abstract

Enhancers are a class of non-coding DNA, serving as crucial regulatory elements in governing gene expression by binding to transcription factors. The identification of enhancers holds paramount importance in the field of biology. However, traditional experimental methods for enhancer identification demand substantial human and material resources. Consequently, there is a growing interest in employing computational methods for enhancer prediction. In this study, we propose a two-stage framework based on deep learning, termed CapsEnhancer, for the identification of enhancers and their strengths. CapsEnhancer utilizes chaos game representation to encode DNA sequences into unique images and employs a capsule network to extract local and global features from sequence ”images”. Experimental results demonstrate that CapsEnhancer achieves state-of-the-art performance in both stages. In the first and second stages, the accuracy surpasses the previous best methods by 8% and 3.5%, reaching accuracies of 94.5% and 95%, respectively. Notably, this research represents the pioneering application of computer vision methods to enhancer identification tasks. We believe that this study not only contributes novel insights to enhancer identification but also provides a fresh perspective for other biological sequence analysis tasks.



### Model

![WechatIMG1555](model_picture.jpg)

## 1.Train

```shell
python3 train.py
```

**please make sure that cuda is avaliable**



## 2.Evaluate

```
python3 evaluate.py
```

**please make sure that cuda is avaliable again**



## 3. train dataset

```
vi train.py
```

**please edit below sentences**

```
...
fig = pd.read_csv("data/stage1/Train.txt")
...
fig_test = pd.read_csv("data/stage1/Test.txt")
```

 **If you want to use our model to train other DNA-related data, please use the data processing code (CGR Encoding) we provide to ensure that the shape of the data matches our model** 



## CGR Encoding

**This instruction can encode DNA sequences into 2D images.**

**Instruction format:**

```shell
Rscript generate_cgr.R {file name} DNA {resolution}
file name: CSV file path, please note that it does not include ". csv".
resolution: The resolution of the generated image.
output: The output is a. txt format file that describes the generated DNA "image".
```



**For example:**

```shell
 Rscript generate_cgr.R dataset/stage1/Test DNA 64
```

