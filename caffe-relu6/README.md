# Caffe-ReLU6
Caffe Implementation of ReLU6 Layer.

## ReLU6 Utilize
1.You should move .c* files to /path/to/caffe/src/caffe/layers/ and .hpp files to /path/to/caffe/include/caffe/layers/

2.Then add these lines to your caffe.proto file:

```
optional ReLU6Parameter relu6_param = 100000;
```
```
message ReLU6Parameter {
  optional float negative_slope = 1 [default = 0];
}
```
3.finally rebuild your caffe
```
$ cd caffe 
$ make pycaffe
$ mkdir build && cd build
$ cmake ..
$ make -j4
$ make install
```

