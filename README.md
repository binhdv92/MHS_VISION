# MHS_VISION

# Installation
1. Install Anaconda
2. update conda
```
(base) C:\>conda upgrade conda
```

3. Create a python virtual environmnet named "tf1.15" that included packages are pip and python 3.7
```
(base) C:\>conda create -n tf1.15 pip python=3.7
```

4. Activate tf1.15 env
```
(base) c:\>conda activate tf1.15
(tf1.15) C:\>

(tf1.15) c:\>python --version
Python 3.7.7

(tf1.15) c:\>pip --version
pip 20.0.2 from C:\ProgramData\Anaconda3\envs\tf1.15\lib\site-packages\pip (python 3.7)
```

5. Installation and validation tensorflow 1.15
- Installation:
```
(tf1.15) C:\>pip install --upgrade tensorflow==1.15
```
- Validation:
```
(tf1.15) c:\>python
Python 3.7.7 (default, May  6 2020, 11:45:54) [MSC v.1916 64 bit (AMD64)] :: Anaconda, Inc. on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> import tensorflow as tf
2020-05-29 09:53:26.262800: W tensorflow/stream_executor/platform/default/dso_loader.cc:55] Could not load dynamic library 'cudart64_100.dll'; dlerror: cudart64_100.dll not found
2020-05-29 09:53:26.266267: I tensorflow/stream_executor/cuda/cudart_stub.cc:29] Ignore above cudart dlerror if you do not have a GPU set up on your machine.
>>> print(tf.__version__)
1.15.0
>>>
```
6. Installation dependences
```
(tf1.15) c:\>conda install -c anaconda protobuf
(tf1.15) c:\>pip install pillow lxml Cython contextlib2 jupyter matplotlib pandas opencv-python
(tf1.15) c:\>pip install tf_slim
(tf1.15) c:\>pip install git+https://github.com/philferriere/cocoapi.git#subdirectory=PythonAPI

```

7. Configure PYTHONPATH environment variable
```
(tf1.15) c:\>set PYTHONPATH=C:\tensorflow1\models;C:\tensorflow1\models\research;C:\tensorflow1\models\research\slim
(tf1.15) c:\>echo %PYTHONPATH%
C:\tensorflow1\models;C:\tensorflow1\models\research;C:\tensorflow1\models\research\slim
```
-

8. Compile Protobufs and run setup.py
```
(base) C:\WINDOWS\system32>conda activate tf1.15

(tf1.15) C:\WINDOWS\system32>cd C:\tensorflow1\models\research

(tf1.15) C:\tensorflow1\models\research>protoc  --python_out=. object_detection/protos/*.proto
object_detection/protos/input_reader.proto:5:1: warning: Import object_detection/protos/image_resizer.proto is unused.

(tf1.15) C:\tensorflow1\models\research>
```

9. 
```
(tf1.15) C:\tensorflow1\models\research>cd C:\tensorflow1\models\research\object_detection
(tf1.15) C:\tensorflow1\models\research\object_detection>jupyter notebook object_detection_tutorial.ipynb
```

```
cd c:/tensorflow1/models/research/

python C:\tensorflow1\models\research\object_detection\builders\model_builder_tf1_test.py
```
