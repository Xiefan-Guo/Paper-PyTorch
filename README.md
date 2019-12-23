
## Table of Contents

* [CNN](#cnn)
    * [AlexNet](#alexnet)
    * [LeNet](#lenet)
* [GAN](#gan)
    * [DCGAN](#dcgan)
    * [GAN](#gan)
    * [Wasserstein GAN](#wasserstein-gan)
* [Image Inpainting](#image-inpainting)
    * [Context Encoders](#context-encoders)
    * [Semantic Image Inpainting with DC Models ](#semantic-image-inpainting-with-dc-models)
 
## CNN

### ALexNet
_ImageNet Classification with Deep Convolutional Neural Networks_

#### Authors
Alex Krizhevsky, Ilya Sutskever, Geoffrey E. Hinton

#### Abstract
We trained a large, deep convolutional neural network to classify the 1.2 million high-resolution images in the ImageNet LSVRC-2010 contest into the 1000 different classes. On the test data, we achieved top-1 and top-5 error rates of 37.5% and 17.0% which is considerably better than the previous state-of-the-art. The neural network, which has 60 million parameters and 650,000 neurons, consists of five convolutional layers, some of which are followed by max-pooling layers, and three fully-connected layers with a final 1000-way softmax. To make training faster, we used non-saturating neurons and a very efficient GPU implementation of the convolution operation. To reduce overfitting in the fully-connected layers we employed a recently-developed regularization method called “dropout” that proved to be very effective. We also entered a variant of this model in the ILSVRC-2012 competition and achieved a winning top-5 test error rate of 15.3%, compared to 26.2% achieved by the second-best entry.

[[Paper]](http://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf)[[Code]](https://github.com/gsolvit/Paper-PyTorch/tree/master/CNN/AlexNet)

#### Run Example
```
$ python3 alexnet.py
```

### LeNet
_Gradient-Based Learning Applied to Document Recognition_
 
#### Authors
Yann LeCun，Leon Botton， Yoshua Bengio，and Patrick Haffner

#### Abstract
Multilayer neural networks trained with the back-propagation algorithm constitute the best example of a successful gradient based learning technique. Given an appropriate network architecture, gradient-based learning algorithms can be used to synthesize a complex decision surface that can classify high-dimensional patterns, such as handwritten characters, with minimal preprocessing. This paper reviews various methods applied to handwritten character recognition and compares them on a standard handwritten digit recognition task. Convolutional neural networks, which are specifically designed to deal with the variability of 2D shapes, are shown to outperform all other techniques. Real-life document recognition systems are composed of multiple modules including field extraction, segmentation recognition, and language modeling. A new learning paradigm, called graph transformer networks (GTN), allows such multimodule systems to be trained globally using gradient-based methods so as to minimize an overall performance measure. Two systems for online handwriting recognition are described. Experiments demonstrate the advantage of global training, and the flexibility of graph transformer networks. A graph transformer network for reading a bank cheque is also described. It uses convolutional neural network character recognizers combined with global training techniques to provide record accuracy on business and personal cheques. It is deployed commercially and reads several million cheques per day.

[[Paper]](https://www.researchgate.net/publication/2985446_Gradient-Based_Learning_Applied_to_Document_Recognition)[[Code]](https://github.com/gsolvit/Paper-PyTorch/tree/master/CNN/LeNet)

#### Run Example
```
$ python3 lenet.py
```
    
### Vgg
_Very Deep Convolutional Networks for Large-Scale Image Recognition_

#### Authors
Karen Simonyan, Andrew Zisserman

#### Abstract
In this work we investigate the effect of the convolutional network depth on its accuracy in the large-scale image recognition setting. Our main contribution is a thorough evaluation of networks of increasing depth using an architecture with very small (3x3) convolution filters, which shows that a significant improvement on the prior-art configurations can be achieved by pushing the depth to 16-19 weight layers. These findings were the basis of our ImageNet Challenge 2014 submission, where our team secured the first and the second places in the localisation and classification tracks respectively. We also show that our representations generalise well to other datasets, where they achieve state-of-the-art results. We have made our two best-performing ConvNet models publicly available to facilitate further research on the use of deep visual representations in computer vision.

[[Paper]](https://arxiv.org/abs/1409.1556)[[Code]](https://github.com/gsolvit/Paper-PyTorch/tree/master/CNN/Vgg)

#### Run Example
```
$ python3 vgg.py
```

## GAN

### DCGAN
_Unsupervised Representation Learning with Deep Convolutional Generative Adversarial Networks_ (ICLR 2016)

#### Authors
Alec Radford, Luke Metz, Soumith Chintala

#### Abstract
In recent years, supervised learning with convolutional networks (CNNs) has seen huge adoption in computer vision applications. Comparatively, unsupervised learning with CNNs has received less attention. In this work we hope to help bridge the gap between the success of CNNs for supervised learning and unsupervised learning. We introduce a class of CNNs called deep convolutional generative adversarial networks (DCGANs), that have certain architectural constraints, and demonstrate that they are a strong candidate for unsupervised learning. Training on various image datasets, we show convincing evidence that our deep convolutional adversarial pair learns a hierarchy of representations from object parts to scenes in both the generator and discriminator. Additionally, we use the learned features for novel tasks - demonstrating their applicability as general image representations.

[[Paper]](https://arxiv.org/abs/1511.06434)[[Code]](https://github.com/gsolvit/Paper-PyTorch/blob/master/GAN/DCGAN/dcgan.py)

#### Run Example
```
$ python3 dcgan.py
```

### GAN
_Generative Adversarial Networks_

#### Authors
Ian J. Goodfellow, Jean Pouget-Abadie, Mehdi Mirza, Bing Xu, David Warde-Farley, Sherjil Ozair, Aaron Courville, Yoshua Bengio

#### Abstract
We propose a new framework for estimating generative models via an adversarial process, in which we simultaneously train two models: a generative model G that captures the data distribution, and a discriminative model D that estimates the probability that a sample came from the training data rather than G. The training procedure for G is to maximize the probability of D making a mistake. This framework corresponds to a minimax two-player game. In the space of arbitrary functions G and D, a unique solution exists, with G recovering the training data distribution and D equal to 1/2 everywhere. In the case where G and D are defined by multilayer perceptrons, the entire system can be trained with backpropagation. There is no need for any Markov chains or unrolled approximate inference networks during either training or generation of samples. Experiments demonstrate the potential of the framework through qualitative and quantitative evaluation of the generated samples.

[[Paper]](https://arxiv.org/abs/1406.2661)[[Code]](https://github.com/gsolvit/Paper-PyTorch/blob/master/GAN/GAN/gan.py)

#### Run Example
```
$ python3 gan.py
```

### Wasserstein GAN
_Wasserstein GAN_

#### Authors
Martin Arjovsky, Soumith Chintala, Léon Bottou

#### Abstract
We introduce a new algorithm named WGAN, an alternative to traditional GAN training. In this new model, we show that we can improve the stability of learning, get rid of problems like mode collapse, and provide meaningful learning curves useful for debugging and hyperparameter searches. Furthermore, we show that the corresponding optimization problem is sound, and provide extensive theoretical work highlighting the deep connections to other distances between distributions.

[[Paper]](https://arxiv.org/abs/1701.07875)[[Code]](https://github.com/gsolvit/Paper-PyTorch/tree/master/GAN/WGAN)

#### Run Example
```
$ python3 wgan.py
```

## Image Inpainting

### Context Encoders
_Context Encoders: Feature Learning by Inpainting_ (CVPR 2016) 

#### Authors
Deepak Pathak, Philipp Krahenbuhl, Jeff Donahue, Trevor Darrell, Alexei A. Efros

#### Abstract
We present an unsupervised visual feature learning algorithm driven by context-based pixel prediction. By analogy with auto-encoders, we propose Context Encoders -- a convolutional neural network trained to generate the contents of an arbitrary image region conditioned on its surroundings. In order to succeed at this task, context encoders need to both understand the content of the entire image, as well as produce a plausible hypothesis for the missing part(s). When training context encoders, we have experimented with both a standard pixel-wise reconstruction loss, as well as a reconstruction plus an adversarial loss. The latter produces much sharper results because it can better handle multiple modes in the output. We found that a context encoder learns a representation that captures not just appearance but also the semantics of visual structures. We quantitatively demonstrate the effectiveness of our learned features for CNN pre-training on classification, detection, and segmentation tasks. Furthermore, context encoders can be used for semantic inpainting tasks, either stand-alone or as initialization for non-parametric methods.

[[Paper]](https://arxiv.org/abs/1604.07379)[[Code]](https://github.com/gsolvit/Paper-PyTorch/tree/master/Image-Inpainting/context-encoder)

#### Run Example
```
$ python3 train.py
```

### Semantic Image Inpainting with DC Models 
_Semantic Image Inpainting with Deep Generative Models_ (CVPR 2017)

#### Authors
Raymond A. Yeh, Chen Chen, Teck Yian Lim, Alexander G. Schwing, Mark Hasegawa-Johnson, Minh N. Do

#### Abstract
Semantic image inpainting is a challenging task where large missing regions have to be filled based on the available visual data. Existing methods which extract information from only a single image generally produce unsatisfactory results due to the lack of high level context. In this paper, we propose a novel method for semantic image inpainting, which generates the missing content by conditioning on the available data. Given a trained generative model, we search for the closest encoding of the corrupted image in the latent image manifold using our context and prior losses. This encoding is then passed through the generative model to infer the missing content. In our method, inference is possible irrespective of how the missing content is structured, while the state-of-the-art learning based method requires specific information about the holes in the training phase. Experiments on three datasets show that our method successfully predicts information in large missing regions and achieves pixel-level photorealism, significantly outperforming the state-of-the-art methods.

[[Paper]](https://arxiv.org/abs/1607.07539)[[Code]](https://github.com/gsolvit/Paper-PyTorch/tree/master/Image-Inpainting/Semantic-Inpainting-DC-Models)

#### Run Example
```
$ python3 train.py
$ python3 inpainting.py
```