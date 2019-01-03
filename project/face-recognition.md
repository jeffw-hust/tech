# 人脸识别

### face\_recognition
* [官方源码](https://github.com/ageitgey/face_recognition)
* 安装
  + Requirements
    1. Python 3.3+ or Python 2.7
    2. macOS or Linux (Windows not officially supported, but might work)
  + Installing on Mac or Linux
    1. First, make sure you have dlib already installed with Python bindings:
      * 参考一: [https://www.learnopencv.com/install-dlib-on-macos/](https://www.learnopencv.com/install-dlib-on-macos/)
      * 参考二: [How to install dlib from source on macOS or Ubuntu](https://gist.github.com/ageitgey/629d75c1baac34dfa5ca2a1928a7aeaf)
      * 备注： 如果报CMAKE错误，则brew install cmake
    2. Then, install this module from pypi using `pip3` (or `pip2` for Python 2):
      ```bash
      pip3 install face_recognition    
      ```
