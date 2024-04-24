---
author: "Yiyi"
date: 2024-04-23
title: "MacOS: brew, pip, conda"
tags: [
 
]
categories: [notes
]
---
# Some error I met when running python file in python environment
* Can‘t find model ‘en_core_web_sm‘. 
python -m spacy download en_core_web_sm

* AttributeError: module ‘numpy‘ has no attribute ‘int‘
pip3 install numpy

# For brew, pip, conda
The same thing is that they are all the package manager.
The difference is that homebrew is a general package manager, so you can install many packages using it.

Pip, on the other hand, installs packages related to the python environment and provides a virtual python environment similar to virtualenv.

Conda is a packaging tool and installer that aims to do more than what pip does; handle library dependencies outside of the Python packages as well as the Python packages themselves. Conda also creates a virtual environment, like virtualenv does. As such, Conda should be compared to Buildout perhaps, another tool that lets you handle both Python and non-Python installation tasks. Because Conda introduces a new packaging format, you cannot use pip and Conda interchangeably;  pip cannot install the Conda package format. You can use the two tools side by side but they do not interoperate either.

