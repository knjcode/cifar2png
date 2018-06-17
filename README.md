cifar2png
=========

Convert CIFAR-10 or CIFAR-100 dataset into PNG images.


# Install

```bash
$ pip install cifar2png
```


# Usage

`$ cifar2png <dataset> <output_dir>`

- `dataset`: Specify `cifar10` or `cifar100`
- `output_dir`: Path to save PNG converted dataset (The directory will be created automatically).

Automatically download `cifar-10-python.tar.gz` or `cifar-100-python.tar.gz` to the current directory from [CIFAR-10 and CIFAR-100 datasets] when you run this tool.


# Example


## CIFAR-10

`$ cifar2png cifar10 path/to/cifar10png`


## CIFAR-100

`$ cifar2png cifar100 path/to/cifar100png`


# Structure of output directory

PNG images of CIFAR-10 are saved in 10 subdirectories of each label under the `test` and `train` directories as below.  
(CIFAR-100 are saved in the same way with 100 subdirectories)

```bash
$ tree -d path/to/cifar10png
path/to/cifar10png
├── test
│   ├── airplane
│   ├── automobile
│   ├── bird
│   ├── cat
│   ├── deer
│   ├── dog
│   ├── frog
│   ├── horse
│   ├── ship
│   └── truck
└── train
    ├── airplane
    ├── automobile
    ├── bird
    ├── cat
    ├── deer
    ├── dog
    ├── frog
    ├── horse
    ├── ship
    └── truck
```

```bash
$ tree -d path/to/cifar10png/test/airplane
path/to/cifar10png/test/airplane
├── 0001.png
├── 0002.png
├── 0003.png
(..snip..)
├── 0998.png
├── 0999.png
└── 1000.png
```


[CIFAR-10 and CIFAR-100 datasets]: https://www.cs.toronto.edu/~kriz/cifar.html
