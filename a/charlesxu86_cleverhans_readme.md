# cleverhans (v1.0.0)

 

This repository contains the source code for `cleverhans`, a Python library to
benchmark machine learning systems' vulnerability to
[adversarial examples](http://u.720life.cn/g/e388ee8f1fdc79c4c48d01b7c30cecc9c590412888f4dfd9beb2e770cdbdc60d3d1367cf4436e6ced4517487e0b6f335db53a69fa5ca2074cbc62ced18b56960 

The `cleverhans` library is under continual development, always welcoming
contributions of the latest attacks and defenses.

## Setting up `cleverhans`

### Dependencies

This library uses `TensorFlow` or `Theano` to accelerate graph 
computations performed by many machine learning models. 
Installing these libraries is therefore a pre-requisite. 
You can find instructions 
[here for Tensorflow](http://u.720life.cn/g/de14350178d8232a6828b0e4db6a4d7b0cb576b44c72a97a53b3244cec9c7eda6f51d5b9a94501e035d4dcf980cc8840) 
and [here for Theano](http://u.720life.cn/g/5233a6d7a6d166bb31785e8f1074e38cd205e94df67bd63664dff6ed2c98f78a9d7cffe73290ece07f771d8ca138168d59d8a7850953c06a23faf48c4c30fd91 
For better performance, it is also recommended to install the
backend library of your choice (`TensorFlow` or `Theano`) with GPU support.

Some models used in the tutorials are also defined using `Keras`.
Note that you should **configure Keras to use the backend that matches
the one used by the tutorial**. Indeed, some tutorials use `Tensorflow`
as their backend while others use `Theano`. You
can find instructions for
setting the Keras backend [on this page](http://u.720life.cn/g/0b0d7e8f2a8da4f210f18d7319f0a1692dc8a43ee0c0d016d7ddac16761f6794  

Installing `TensorFlow` or `Theano` will
take care of all other dependencies like `numpy` and `scipy`.

### Cloning the repository 

Once dependencies have been taken care of, you simply need to clone
this repository into a folder of your choice. 

```
git clone https://github.com/openai/cleverhans
```

### Updating the `PYTHONPATH` environment variable

On UNIX machines, it is recommended to add your clone of this repository to the
`PYTHONPATH` variable so as to be able to import `cleverhans` from any folder.

```
export PYTHONPATH="/path/to/cleverhans":$PYTHONPATH
```

You may want to make that change permanent through your shell's profile.

## Tutorials

To help you get started with the functionalities provided by this library, it
comes with the following tutorials:
* **MNIST with FGSM using the TensorFlow backend** ([code](tutorials/mnist_tutorial_tf.py), [tutorial](tutorials/mnist_tutorial_tf.md)): this first
tutorial covers how to train a MNIST model using TensorFlow,
craft adversarial examples using the [fast gradient sign method](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754d2a2c866fddd797fc4ff5263d6158be68721581cf02c61fdac053c64585ae885  
and make the model more robust to adversarial
examples using adversarial training.
* **MNIST with JSMA using the Tensorflow backend** ([code](tutorials/mnist_tutorial_jsma.py), [tutorial](tutorials/mnist_tutorial_jsma.md)): this second
tutorial covers how to train a MNIST model using TensorFlow and
craft adversarial examples using the [Jacobian-based saliency map approach](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa057546d5ddd929b0f892f21ee6f115544c3251aae7218156ca70b517d214d04e3e3c8  
* **MNIST with FGSM using the Theano backend** ([code](tutorials/mnist_tutorial_th.py)): this
tutorial covers how to train a MNIST model using Theano,
craft adversarial examples using the fast gradient sign
method and make the model more robust to
adversarial examples using adversarial training.
Note: this script does not have a tutorial markdown
yet, but the corresponding [tutorial](tutorials/mnist_tutorial_tf.md) in TensorFlow
will prove useful in the meanwhile.
* more to come soon...
 
## Reporting benchmarks

When reporting benchmarks, please:
* Use a versioned release of `cleverhans`. You can find a list of released versions [here](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046eaa9e61ed3500273d226f7fcd9e9a9182f91b1daed77432a559dbe333306af3e 
* Either use the latest version, or, if comparing to an earlier publication, use the same version as the earlier publication.
* Report which attack method was used.
* Report any configuration variables used to determine the behavior of the attack.

For example, you might report "We benchmarked the robustness of our method to
adversarial attack using v1.0.0 of `cleverhans`. On a test set modified by the
`fgsm` with `eps` of 0.3, we obtained a test set accuracy of 71.3%."

## Contributing

Contributions are welcomed! We ask that new efforts and features be coordinated
on the mailing list for `cleverhans` development: [cleverhans-dev@googlegroups.com](http://u.720life.cn/g/941693b557d072bb769494a6a61fcd979ee9fee4d4fd0c2a6b8a30bc68eade2120b0bdeafc4dd16396d5377bed32a77886b053bdda47b30cd6832e960e49a8d9  
Bug fixes can be initiated through Github pull requests.

When making contributions to `cleverhans`, we ask that you follow the 
`PEP8` coding style in your pull requests. 

## About the name

The name `cleverhans` is a reference to a presentation by Bob Sturm titled
“Clever Hans, Clever Algorithms: Are Your Machine Learnings Learning What You
Think?" and the corresponding publication, ["A Simple Method to Determine if a
Music Information Retrieval System is a
'Horse'."](http://u.720life.cn/g/9e82bf4a493e96d7a7f3c02f5e1db3ea9ce877e15b61806e47f568f689d6ef0fb6ba1e098677c0c60525654fc99b7caa)  Clever Hans was a
horse that appeared to have learned to answer arithmetic questions, but had in
fact only learned to read social cues that enabled him to give the correct
answer. In controlled settings where he could not see people's faces or receive
other feedback, he was unable to answer the same questions. The story of Clever
Hans is a metaphor for machine learning systems that may achieve very high
accuracy on a test set drawn from the same distribution as the training data,
but that do not actually understand the underlying task and perform poorly on
other inputs.

## Authors

This library is managed and maintained by Ian Goodfellow (OpenAI),
Nicolas Papernot (Pennsylvania State University), and
Ryan Sheatsley (Pennsylvania State University).

The following authors contributed (ordered according to the GitHub contributors page):
* Nicolas Papernot (Pennsylvania State University)
* Ian Goodfellow (OpenAI)
* Ryan Sheatsley (Pennsylvania State University)
* Reuben Feinman (Symantec)

## Citing this work

If you use `cleverhans` for academic research, you are highly encouraged 
(though not required) to cite the following paper:

```
@article{papernot2016cleverhans,
  title={cleverhans v1.0.0: an adversarial machine learning library},
  author={Papernot, Nicolas and Goodfellow, Ian and Sheatsley, Ryan and Feinman, Reuben and McDaniel, Patrick},
  journal={arXiv preprint arXiv:1610.00768},
  year={2016}
}
```

A new version of the technical report will be uploaded for each major
revision. GitHub contributors will be added to the author list.

## Copyright

Copyright 2016 - OpenAI and Pennsylvania State University.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)