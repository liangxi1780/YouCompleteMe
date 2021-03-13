# fastText
[fastText](http://u.720life.cn/g/efa41906c3cda0d464111f5be441a9d674d79c8d34906f2ea38b844585b8b3e2)  is a library for efficient learning of word representations and sentence classification.

[![CircleCI](https://circleci.com/gh/facebookresearch/fastText/tree/master.svg?style=svg)](https://circleci.com/gh/facebookresearch/fastText/tree/master)

## Table of contents

* [Resources](#resources)
   * [Models](#models)
   * [Supplementary data](#supplementary-data)
   * [FAQ](#faq)
   * [Cheatsheet](#cheatsheet)
* [Requirements](#requirements)
* [Building fastText](#building-fasttext)
   * [Getting the source code](#getting-the-source-code)
   * [Building fastText using make (preferred)](#building-fasttext-using-make-preferred)
   * [Building fastText using cmake](#building-fasttext-using-cmake)
   * [Building fastText for Python](#building-fasttext-for-python)
* [Example use cases](#example-use-cases)
   * [Word representation learning](#word-representation-learning)
   * [Obtaining word vectors for out-of-vocabulary words](#obtaining-word-vectors-for-out-of-vocabulary-words)
   * [Text classification](#text-classification)
* [Full documentation](#full-documentation)
* [References](#references)
   * [Enriching Word Vectors with Subword Information](#enriching-word-vectors-with-subword-information)
   * [Bag of Tricks for Efficient Text Classification](#bag-of-tricks-for-efficient-text-classification)
   * [FastText.zip: Compressing text classification models](#fasttextzip-compressing-text-classification-models)
* [Join the fastText community](#join-the-fasttext-community)
* [License](#license)

## Resources

### Models
- Recent state-of-the-art [English word vectors](http://u.720life.cn/g/efa41906c3cda0d464111f5be441a9d65859f9dae5d83ecda7daa230e33d4c5abf9eae1aa5a43f68227370d60812d7d59707b60c46e32a42dc3e8448a4301d3c 
- Word vectors for [157 languages trained on Wikipedia and Crawl](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304697d9ece9d0ba791376c04b68e0cd9a5bf657534e08247a47318c99862003b6dc9e22d9a4eb14f2e3a83590027f5800b740ae7355477dadb20ea834482e0b153a 
- Models for [language identification](http://u.720life.cn/g/efa41906c3cda0d464111f5be441a9d6d4cedf527ca7dfb6b0a36db641253a568e64180b5f319d4b78bc763c8cd39b64e194f3d33b32c6c433609e19dc83bb3f)  and [various supervised tasks](http://u.720life.cn/g/efa41906c3cda0d464111f5be441a9d60b7fcd4d5ad0edd68d598ab9d761d6fec21d1bd6e6469c0dcdf3233f5b6676eeae56bd061622c5f45f34a22fedf91a65 

### Supplementary data
- The preprocessed [YFCC100M data](http://u.720life.cn/g/efa41906c3cda0d464111f5be441a9d6ed2e431416868bdd034eb56d5746b50318e4c665845a00ce6bac392a1c42516b)  used in [2].

### FAQ

You can find [answers to frequently asked questions](http://u.720life.cn/g/efa41906c3cda0d464111f5be441a9d6b197ca8c2551bd524d233dff5b5480e5c9c77f7a34e420bc9147da8d3ad98ab1)  on our [website](http://u.720life.cn/g/efa41906c3cda0d464111f5be441a9d69c9ec8b052d3463c4bbd133e978bc0d5 

### Cheatsheet

We also provide a [cheatsheet](http://u.720life.cn/g/efa41906c3cda0d464111f5be441a9d6b0439810b117883332f69bd8440701df5dcea4d7765523cbba4452ac68c677d5a57fd2c02f613704161c93078c7df8b1)  full of useful one-liners.

## Requirements

We are continuously building and testing our library, CLI and Python bindings under various docker images using [circleci](http://u.720life.cn/g/898666cdcb1d135b6c1e75c8d72bb956a2a6ca81c78a85cf14aa17d42521ba9e 

Generally, **fastText** builds on modern Mac OS and Linux distributions.
Since it uses some C++11 features, it requires a compiler with good C++11 support.
These include :

* (g++-4.7.2 or newer) or (clang-3.3 or newer)

Compilation is carried out using a Makefile, so you will need to have a working **make**.
If you want to use **cmake** you need at least version 2.8.9.

One of the oldest distributions we successfully built and tested the CLI under is [Debian jessie](http://u.720life.cn/g/ccf0a694c1840e89256e936c17a9434d7d662a51b5af65a115c8c1dd494b5779ccb171414dbac1ad7918bc36c899dc90 

For the word-similarity evaluation script you will need:

* Python 2.6 or newer
* NumPy & SciPy

For the python bindings (see the subdirectory python) you will need:

* Python version 2.7 or >=3.4
* NumPy & SciPy
* [pybind11](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a471de8bb155c2e1a8ba25c86b6903f87d64c252a31b66f58383fd81c1084108) 

One of the oldest distributions we successfully built and tested the Python bindings under is [Debian jessie](http://u.720life.cn/g/ccf0a694c1840e89256e936c17a9434d7d662a51b5af65a115c8c1dd494b5779ccb171414dbac1ad7918bc36c899dc90 

If these requirements make it impossible for you to use fastText, please open an issue and we will try to accommodate you.

## Building fastText

We discuss building the latest stable version of fastText.

### Getting the source code

You can find our [latest stable release](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304697d9ece9d0ba791376c04b68e0cd9a5be4f28fdbb37625920290aa8cdd16e7ec7b0d0bd1a327351f93bf2d0b269cc696)  in the usual place.

There is also the master branch that contains all of our most recent work, but comes along with all the usual caveats of an unstable branch. You might want to use this if you are a developer or power-user.

### Building fastText using make (preferred)

```
$ wget https://github.com/facebookresearch/fastText/archive/v0.9.2.zip
$ unzip v0.9.2.zip
$ cd fastText-0.9.2
$ make
```

This will produce object files for all the classes as well as the main binary `fasttext`.
If you do not plan on using the default system-wide compiler, update the two macros defined at the beginning of the Makefile (CC and INCLUDES).

### Building fastText using cmake

For now this is not part of a release, so you will need to clone the master branch.

```
$ git clone https://github.com/facebookresearch/fastText.git
$ cd fastText
$ mkdir build && cd build && cmake ..
$ make && make install
```

This will create the fasttext binary and also all relevant libraries (shared, static, PIC).

### Building fastText for Python

For now this is not part of a release, so you will need to clone the master branch.

```
$ git clone https://github.com/facebookresearch/fastText.git
$ cd fastText
$ pip install .
```

For further information and introduction see python/README.md

## Example use cases

This library has two main use cases: word representation learning and text classification.
These were described in the two papers [1](#enriching-word-vectors-with-subword-information) and [2](#bag-of-tricks-for-efficient-text-classification).

### Word representation learning

In order to learn word vectors, as described in [1](#enriching-word-vectors-with-subword-information), do:

```
$ ./fasttext skipgram -input data.txt -output model
```

where `data.txt` is a training file containing `UTF-8` encoded text.
By default the word vectors will take into account character n-grams from 3 to 6 characters.
At the end of optimization the program will save two files: `model.bin` and `model.vec`.
`model.vec` is a text file containing the word vectors, one per line.
`model.bin` is a binary file containing the parameters of the model along with the dictionary and all hyper parameters.
The binary file can be used later to compute word vectors or to restart the optimization.

### Obtaining word vectors for out-of-vocabulary words

The previously trained model can be used to compute word vectors for out-of-vocabulary words.
Provided you have a text file `queries.txt` containing words for which you want to compute vectors, use the following command:

```
$ ./fasttext print-word-vectors model.bin < queries.txt
```

This will output word vectors to the standard output, one vector per line.
This can also be used with pipes:

```
$ cat queries.txt | ./fasttext print-word-vectors model.bin
```

See the provided scripts for an example. For instance, running:

```
$ ./word-vector-example.sh
```

will compile the code, download data, compute word vectors and evaluate them on the rare words similarity dataset RW [Thang et al. 2013].

### Text classification

This library can also be used to train supervised text classifiers, for instance for sentiment analysis.
In order to train a text classifier using the method described in [2](#bag-of-tricks-for-efficient-text-classification), use:

```
$ ./fasttext supervised -input train.txt -output model
```

where `train.txt` is a text file containing a training sentence per line along with the labels.
By default, we assume that labels are words that are prefixed by the string `__label__`.
This will output two files: `model.bin` and `model.vec`.
Once the model was trained, you can evaluate it by computing the precision and recall at k (P@k and R@k) on a test set using:

```
$ ./fasttext test model.bin test.txt k
```

The argument `k` is optional, and is equal to `1` by default.

In order to obtain the k most likely labels for a piece of text, use:

```
$ ./fasttext predict model.bin test.txt k
```

or use `predict-prob` to also get the probability for each label

```
$ ./fasttext predict-prob model.bin test.txt k
```

where `test.txt` contains a piece of text to classify per line.
Doing so will print to the standard output the k most likely labels for each line.
The argument `k` is optional, and equal to `1` by default.
See `classification-example.sh` for an example use case.
In order to reproduce results from the paper [2](#bag-of-tricks-for-efficient-text-classification), run `classification-results.sh`, this will download all the datasets and reproduce the results from Table 1.

If you want to compute vector representations of sentences or paragraphs, please use:

```
$ ./fasttext print-sentence-vectors model.bin < text.txt
```

This assumes that the `text.txt` file contains the paragraphs that you want to get vectors for.
The program will output one vector representation per line in the file.

You can also quantize a supervised model to reduce its memory usage with the following command:

```
$ ./fasttext quantize -output model
```
This will create a `.ftz` file with a smaller memory footprint. All the standard functionality, like `test` or `predict` work the same way on the quantized models:
```
$ ./fasttext test model.ftz test.txt
```
The quantization procedure follows the steps described in [3](#fasttextzip-compressing-text-classification-models). You can
run the script `quantization-example.sh` for an example.


## Full documentation

Invoke a command without arguments to list available arguments and their default values:

```
$ ./fasttext supervised
Empty input or output path.

The following arguments are mandatory:
  -input              training file path
  -output             output file path

The following arguments are optional:
  -verbose            verbosity level [2]

The following arguments for the dictionary are optional:
  -minCount           minimal number of word occurrences [1]
  -minCountLabel      minimal number of label occurrences [0]
  -wordNgrams         max length of word ngram [1]
  -bucket             number of buckets [2000000]
  -minn               min length of char ngram [0]
  -maxn               max length of char ngram [0]
  -t                  sampling threshold [0.0001]
  -label              labels prefix [__label__]

The following arguments for training are optional:
  -lr                 learning rate [0.1]
  -lrUpdateRate       change the rate of updates for the learning rate [100]
  -dim                size of word vectors [100]
  -ws                 size of the context window [5]
  -epoch              number of epochs [5]
  -neg                number of negatives sampled [5]
  -loss               loss function {ns, hs, softmax} [softmax]
  -thread             number of threads [12]
  -pretrainedVectors  pretrained word vectors for supervised learning []
  -saveOutput         whether output params should be saved [0]

The following arguments for quantization are optional:
  -cutoff             number of words and ngrams to retain [0]
  -retrain            finetune embeddings if a cutoff is applied [0]
  -qnorm              quantizing the norm separately [0]
  -qout               quantizing the classifier [0]
  -dsub               size of each sub-vector [2]
```

Defaults may vary by mode. (Word-representation modes `skipgram` and `cbow` use a default `-minCount` of 5.)

## References

Please cite [1](#enriching-word-vectors-with-subword-information) if using this code for learning word representations or [2](#bag-of-tricks-for-efficient-text-classification) if using for text classification.

### Enriching Word Vectors with Subword Information

[1] P. Bojanowski\*, E. Grave\*, A. Joulin, T. Mikolov, [*Enriching Word Vectors with Subword Information*](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754d2ab61c84a1dbcb3df75a967834b699e) 

```
@article{bojanowski2017enriching,
  title={Enriching Word Vectors with Subword Information},
  author={Bojanowski, Piotr and Grave, Edouard and Joulin, Armand and Mikolov, Tomas},
  journal={Transactions of the Association for Computational Linguistics},
  volume={5},
  year={2017},
  issn={2307-387X},
  pages={135--146}
}
```

### Bag of Tricks for Efficient Text Classification

[2] A. Joulin, E. Grave, P. Bojanowski, T. Mikolov, [*Bag of Tricks for Efficient Text Classification*](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754f48cbdcb19bf2141845154bcd0c6ee17) 

```
@InProceedings{joulin2017bag,
  title={Bag of Tricks for Efficient Text Classification},
  author={Joulin, Armand and Grave, Edouard and Bojanowski, Piotr and Mikolov, Tomas},
  booktitle={Proceedings of the 15th Conference of the European Chapter of the Association for Computational Linguistics: Volume 2, Short Papers},
  month={April},
  year={2017},
  publisher={Association for Computational Linguistics},
  pages={427--431},
}
```

### FastText.zip: Compressing text classification models

[3] A. Joulin, E. Grave, P. Bojanowski, M. Douze, H. Jégou, T. Mikolov, [*FastText.zip: Compressing text classification models*](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754356aab74fd0375f1945116228242ff49) 

```
@article{joulin2016fasttext,
  title={FastText.zip: Compressing text classification models},
  author={Joulin, Armand and Grave, Edouard and Bojanowski, Piotr and Douze, Matthijs and J{\'e}gou, H{\'e}rve and Mikolov, Tomas},
  journal={arXiv preprint arXiv:1612.03651},
  year={2016}
}
```

(\* These authors contributed equally.)


## Join the fastText community

* Facebook page: https://www.facebook.com/groups/1174547215919768
* Google group: https://groups.google.com/forum/#!forum/fasttext-library
* Contact: [egrave@fb.com](mailto:egrave@fb.com), [bojanowski@fb.com](mailto:bojanowski@fb.com), [ajoulin@fb.com](mailto:ajoulin@fb.com), [tmikolov@fb.com](mailto:tmikolov@fb.com)

See the CONTRIBUTING file for information about how to help out.

## License

fastText is MIT-licensed.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)