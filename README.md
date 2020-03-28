# tf_pip_whl
TensorFlow 2.1.0.whl file to install with pip (Ubuntu)

Install TensorFlow 2.1.0 for Ubuntu 19.10 with the following specs:
    - Intel Celeron N3060 1.60GHz 
    - 8GB DDR3L RAM
    - 64-bit OS

Unfortunately, there are a lot of PC´s which have been left behind current TensorFlow versions (In this case, due to AVX instructions added after tf 1.6) this is why I built a pip package made to be installed on PC´s with 'old' processors (Or not powerful like i5-i7 Intel series)

Feel free to use and distribute 'tf_nightly-2.1.0-cp37-cp37m-linux_x86_64.whl' on your laptop/desktop

*The majority of commands are typed in virtualenv (Please note the: (TensorFlow) user@hostname ~$ BEFORE commands)

1. INSTALL PYTHON AND PIP

```
$ sudo apt install python3-dev python3-pip
```

2. DEPENDENCES

```
(TensorFlow) $ pip install pip
```
```
(TensorFlow) $ pip install numpy
```
```(TensorFlow) $ pip install mock```
```
(TensorFlow) $ pip install keras_applications --no-deps
```
```
(TensorFlow) $ pip install keras_preprocessing --no-deps
```

3. GET BAZEL

```
$ sudo apt install curl
```
```
curl https://bazel.build/bazel-release.pub.gpg | sudo apt-key add - echo "deb [arch=amd64] https://storage.googleapis.com/bazel-apt stable jdk1.8" | sudo tee /etc/apt/sources.list.d/bazel.list
```

4. INSTALL AND UPDATE BAZEL

```
$ sudo apt update && sudo apt install bazel
```

5. INSTALL AN SPECIFIC VERSION OF BAZEL

```
$ sup apt install bazel-2.0.0
```

*The are some comments about that Bazel requires an specific version to build the pip package, but I did use Bazel-2.0.0 with no errors / problems

6. DOWNLOAD TENSORFLOW 

```
(TensorFlow) $ git clone https://github.com/tensorflow/tensorflow.git
```

7. GO TO THE DIRECTORY

```
(TensorFlow) $ cd tensorflow
```

8. 

