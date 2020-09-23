torchvision
===========

The torchvision package consists of popular datasets, model architectures, and common image transformations for computer vision.

Installation
============

TorchVision requires PyTorch 1.2 or newer.

Anaconda:

.. code:: bash

    conda install torchvision -c pytorch

pip:

.. code:: bash

    pip install torchvision

From source:

.. code:: bash

    python setup.py install
    # or, for OSX
    # MACOSX_DEPLOYMENT_TARGET=10.9 CC=clang CXX=clang++ python setup.py install

By default, GPU support is built if CUDA is found and ``torch.cuda.is_available()`` is true.
It's possible to force building GPU support by setting ``FORCE_CUDA=1`` environment variable,
which is useful when building a docker image.

Image Backend
=============
Torchvision currently supports the following image backends:

* `Pillow`_ (default)

* `Pillow-SIMD`_ - a **much faster** drop-in replacement for Pillow with SIMD. If installed will be used as the default.

* `accimage`_ - if installed can be activated by calling :code:`torchvision.set_image_backend('accimage')`

.. _Pillow : https://python-pillow.org/
.. _Pillow-SIMD : https://github.com/uploadcare/pillow-simd
.. _accimage: https://github.com/pytorch/accimage

C++ API
=======
TorchVision also offers a C++ API that contains C++ equivalent of python models. 

Installation From source:

.. code:: bash

    mkdir build
    cd build
    cmake ..
    make 
    make install
