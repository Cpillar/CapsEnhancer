# CapsEnhencer

**A model for enhanced classification and feature extraction**

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
fig = pd.read_csv("data/stage1/Test.txt")
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


# CapsEnhancer
