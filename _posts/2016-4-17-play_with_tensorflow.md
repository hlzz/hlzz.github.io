---
layout: post
title: Play with TensorFlow - Part I (初始Tensorflow - 谷歌深度学习框架)
---

I once developed intense interests in neural networks when I was an undergraduate. Though currently working on 3D reconstruction, 
I am still amazed and inspired by the rapid advancements in the field of deep learning (think about DeepMind and Alphago). 
As Google recently open-sourced their deep learning framework [TensorFlow](https://www.tensorflow.org), which is under the active iterative development, I think it is a good time to pick up this old hobby. 
One particular reason that propels me to look at this library at this very moment is perhaps the release of version 0.8, which has involved a great deal since its first release, and the additional support of distributed computing .
In this post (and hopefully a series of following posts...), I will document my experience with this renowned library.

## Installation
One thing I like frameworks and libraried provided by big companies is that the deployment and support work is nicely done. 
The installation process didn't take me too much efforts thanks to the detailed tutorial, only that I am using a Macbook and currently GPU support can't be enabled for OSX. 
But hopefully it might be supported soon by them.

## First Try
To test the installation, I just run the 'python convolutional.py' in 'tensorflow/models/image/mnist' folder

```
Tianweis-Macbook:mnist STW$ python convolutional.py 
Successfully downloaded train-images-idx3-ubyte.gz 9912422 bytes.
Successfully downloaded train-labels-idx1-ubyte.gz 28881 bytes.
Successfully downloaded t10k-images-idx3-ubyte.gz 1648877 bytes.
Successfully downloaded t10k-labels-idx1-ubyte.gz 4542 bytes.
Extracting data/train-images-idx3-ubyte.gz
Extracting data/train-labels-idx1-ubyte.gz
Extracting data/t10k-images-idx3-ubyte.gz
Extracting data/t10k-labels-idx1-ubyte.gz
Initialized!
Step 0 (epoch 0.00), 3.7 ms
Minibatch loss: 12.054, learning rate: 0.010000
Minibatch error: 90.6%
Validation error: 84.6%
Step 100 (epoch 0.12), 209.4 ms
Minibatch loss: 3.269, learning rate: 0.010000
Minibatch error: 6.2%
Validation error: 6.9%
Step 200 (epoch 0.23), 227.5 ms
Minibatch loss: 3.474, learning rate: 0.010000
Minibatch error: 12.5%
Validation error: 3.6%
Step 300 (epoch 0.35), 219.9 ms
Minibatch loss: 3.215, learning rate: 0.010000
Minibatch error: 7.8%
Validation error: 3.4%
...
# *Steps are omitted in this output*
...
Step 8500 (epoch 9.89), 238.9 ms
Minibatch loss: 1.614, learning rate: 0.006302
Minibatch error: 3.1%
Validation error: 0.8%
Test error: 0.8%
```

After 8500 epochs, it returns a CNN model with 0.8 validation and test error, cool!

## System Highlights
After spending some time reading the initial whitepaper [1], I summarize some of the system highlights:

* The TensorFlow computation is decribed by a directed graph, which is composed of a set of nodes.

* node: values that flow along normal edges

* control dependencies: enforce orderings, controlling the peak memory usage

* operations and kernels: An operation has a name and represents an abstract computation, A kernel is a particular implementation of an operation that can be run on a particular type of device (e.g., CPU or GPU).

* Client-master model: use Session interface to communicate with the master, and one or more worker processes. (TensorFlow didn't release a native distributed computing solution until version 0.8.)

* Fault tolerance: is achieved by Variable nodes that each is connected to a Save node and Restore node.

* Gradient computation: it first finds the path in the computation graph from I to C. Then it backtracks from C to I, and for each operation on the backward path it adds a node to the TensorFlow graph 

* Many of our kernel implementations are relatively thin wrappers around such optimized libraries (e.g., cuBLAS, cuDNN).

* Performance evaluation: they haven't provided such a benchmark comparison with other ML systems such as Caffe and Theano at this moment. But according to some external benchmark tests [2 - 4], it is claimed to have bad performance compared to other popular libraries. We cannot say too definitively on the performance issue since it is involving rapidly thanks to the huge community.

## A Brief Exploration of the Code
TensorFlow uses [bazel](http://bazel.io) as the building tool, which is internally used by Google. It has several dependencies, e.g., [protobuf](https://github.com/google/protobuf) for data serializing, [grpc](https://github.com/grpc/grpc) for message passing in distributed computing, [Eigen3](http://eigen.tuxfamily.org) for matrix manipulation, the list goes on. The core lib directory is both giant and neat, containing the client interface distributed runtime, graph definitions, kernel-related (device) code, etc. I looked up the tensorflow website and found dozens of examples, but no roadmap or code structures for contributing. So in the future I might delve deeper into the code and find more details about the implementation. Stay tuned!

## Reference
[1] TensorFlow whitepaper: Abadi, Martın, et al. "TensorFlow: Large-Scale Machine Learning on Heterogeneous Distributed Systems." arXiv preprint arXiv:1603.04467 (2016)

[2] https://en.wikipedia.org/wiki/Comparison_of_deep_learning_software

[3] Bahrampour, Soheil, et al. "Comparative Study of Deep Learning Software Frameworks." arXiv preprint arXiv:1511.06435 (2015).

[4] https://github.com/soumith/convnet-benchmarks