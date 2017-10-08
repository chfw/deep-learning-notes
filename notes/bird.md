# 是不是小鸟

刚读完[机器学习原来这么有趣！第三章:图像识别【鸟or飞机】？深度学习与卷积神经网络](https://zhuanlan.zhihu.com/p/24524583)并且成功让老驴拉车了。现在记录一下中间遇到的问题和解决方案。

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


## 观察

### 训练过程

没有GPU加速，8内核CPU的老驴拉了6个半小时才结束训练。训练程序中产生一堆中间文件

```
...
-rw-r--r--. 1 25860168 Oct  6 00:53 bird-classifier.tfl.ckpt-7696.data-00000-of-00001
-rw-r--r--. 1     1508 Oct  6 00:53 bird-classifier.tfl.ckpt-7696.index
-rw-r--r--. 1   211246 Oct  6 00:53 bird-classifier.tfl.ckpt-7696.meta
...
```

### 判断

判断时间不长，得结论比训练快。



英文原版：[Machine Learning is Fun! Part 3: Deep Learning and Convolutional Neural Networks](https://medium.com/@ageitgey/machine-learning-is-fun-part-3-deep-learning-and-convolutional-neural-networks-f40359318721)