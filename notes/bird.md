# 是不是小鸟

刚读完 [Machine Learning is Fun! Part 3: Deep Learning and Convolutional Neural Networks](https://medium.com/@ageitgey/machine-learning-is-fun-part-3-deep-learning-and-convolutional-neural-networks-f40359318721) 并且成功让老驴拉车了。现在记录一下中间遇到的问题和解决方案。

![running](https://github.com/chfw/deep-learning-notes/raw/master/images/bird-1.png)


1. 训练数据并不是从CIFAR-10下载，而是从作者的[AWS下载](https://medium.com/@ageitgey/good-question-a095787c12f1)。数据大小是450MB。
1. 训练脚本不能在PYTHON 3下运行。PYTHON2.7可用。
1. 这些是运行所需的PYTHON库：

```
tflearn
tensorflow
h5py
scipy
```

..静待更新