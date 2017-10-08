# 是不是小鸟

刚读完 [Machine Learning is Fun! Part 3: Deep Learning and Convolutional Neural Networks](https://medium.com/@ageitgey/machine-learning-is-fun-part-3-deep-learning-and-convolutional-neural-networks-f40359318721) 并且成功让老驴拉车了。现在记录一下中间遇到的问题和解决方案。

![running](https://github.com/chfw/deep-learning-notes/raw/master/images/bird-1.png)


1. 训练数据并不是从CIFAR-10下载，而是从作者的[AWS下载](https://medium.com/@ageitgey/good-question-a095787c12f1)。数据大小是450MB。
1. 训练脚本不能在PYTHON 3下运行。PYTHON2.7可用。
1. 这些是运行所需的PYTHON库：

```
tflearn==0.3.2
tensorflow==1.3.0
h5py==2.7.1
scipy==0.19.1
```

抓小鸟图测试：

运行[小鸟测试程序](https://gist.github.com/ageitgey/a40dded08e82e59724c70da23786bbf0):

```shell
$ python are_you_a_bird.py deep-learning-notes/images/birds/twitter-32x32.jpg 
That's not a bird!
```

|小鸟|测试结果|
|---|---|
|![bird1](https://github.com/chfw/deep-learning-notes/raw/master/images/birds/bird-32x32.png)| Yes  |
|![bird2](https://github.com/chfw/deep-learning-notes/raw/master/images/birds/bird2-32x32.png)| Yes |
|![big-bird](https://github.com/chfw/deep-learning-notes/raw/master/images/birds/bird.jpg)| yes|
|![big-bird2](https://github.com/chfw/deep-learning-notes/raw/master/images/birds/bird2.jpg)| yes|
|![big-bird3](https://github.com/chfw/deep-learning-notes/raw/master/images/birds/bird3.jpg)| no|
|![big-bird4](https://github.com/chfw/deep-learning-notes/raw/master/images/birds/bird4.jpg)| no|
|![twitter](https://github.com/chfw/deep-learning-notes/raw/master/images/birds/twitter-32x32.jpg)| no|
