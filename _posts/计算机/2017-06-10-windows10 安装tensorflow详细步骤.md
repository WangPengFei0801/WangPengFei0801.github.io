---
layout: post
title:前端工程———基础篇
category: 计算机(IT)
keywords:  机器学习 tensorflow
description: 前端基础篇介绍[借鉴于](https://github.com/fouber/blog/issues/10)
---




## 预备工作     
1.  (xxxxxxx) python工具包利器： Anaconda3(因为win下只出了python3.5版本的)， [清华大学conda源](https://mirror.tuna.tsinghua.edu.cn/help/anaconda/) , [清华大学pipy源](https://mirror.tuna.tsinghua.edu.cn/help/pypi/) , [Pypi官方源](https://pypi.python.org/packages) ，[Conda官方源(其中一个发布源)](https://anaconda.org/menpo/) ，最重要的就是Google了。
2.   当我们下载好了Anaconda后，你懂的，直接安装，最好是写入系统的path中（注意提示，不要直接一路回车过去）。 在Linux中更是如此，不要使用sudo权限，否则会写入sudo 的路径中，以后使用的时候诸多麻烦的。安装好anaconda后，你应该有了virtualenv这个工具了，这个工具是用来创建虚拟环境的（一个系统往往有很多人在用，大家对系统的要求都不一样，你需要opencv2.8，他可能需要opencv3.1...为了解决这个问题，python虚拟环境应运而生，具体请google）。如果没有，请这样子： pip install  virtualenv  -i http://pypi.douban.com/simple,  请注意看，我这里使用的是豆瓣的pypi源头，换成清华源当然也是可以的了。 **反正无论如何，你都要装上这个virtualenv这个工具**，如果中途提示你升级 pip之类的，听话就行了。           
        
## 安装虚拟环境       

2.    下载好的opencv应该是win-64/opencv3-3.1.0-py35_0.tar.bz2。 conda install XXX.tar.bz2就行了。或者你下的是whl的，那就pip install XXX.whl 也行。  然后pip install numpy_XXX_XXX.whl。这样opencv和numpy就安装好了。                
##  安装tensorflow
1  在github的tensorflow主页安装指南这里，你应该会看到这么一副图：        
  
```bash
# Ubuntu/Linux 64-bit, CPU only, Python 2.7
$ export TF_BINARY_URL=https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-0.12.1-cp27-none-linux_x86_64.whl

# Ubuntu/Linux 64-bit, GPU enabled, Python 2.7
# Requires CUDA toolkit 8.0 and CuDNN v5. For other versions, see "Installing from sources" below.
$ export TF_BINARY_URL=https://storage.googleapis.com/tensorflow/linux/gpu/tensorflow_gpu-0.12.1-cp27-none-linux_x86_64.whl


# Ubuntu/Linux 64-bit, CPU only, Python 3.4
$ export TF_BINARY_URL=https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-0.12.1-cp34-cp34m-linux_x86_64.whl

# Ubuntu/Linux 64-bit, GPU enabled, Python 3.4
# Requires CUDA toolkit 8.0 and CuDNN v5. For other versions, see "Installing from sources" below.
$ export TF_BINARY_URL=https://storage.googleapis.com/tensorflow/linux/gpu/tensorflow_gpu-0.12.1-cp34-cp34m-linux_x86_64.whl

# Ubuntu/Linux 64-bit, CPU only, Python 3.5
$ export TF_BINARY_URL=https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-0.12.1-cp35-cp35m-linux_x86_64.whl

# Ubuntu/Linux 64-bit, GPU enabled, Python 3.5
# Requires CUDA toolkit 8.0 and CuDNN v5. For other versions, see "Installing from sources" below.
$ export TF_BINARY_URL=https://storage.googleapis.com/tensorflow/linux/gpu/tensorflow_gpu-0.12.1-cp35-cp35m-linux_x86_64.whl
```          

看的我头大，我们需要哪个的话，就直接把URL放到迅雷里面，然后直接下载就好了，速度相当快。  我们看到            

```bash
C:\> pip install --upgrade https://storage.googleapis.com/tensorflow/windows/cpu/tensorflow-0.12.1-cp35-cp35m-win_amd64.whl    
```               

下载它（CPU版），在虚拟环境中执行 pip install tensor_XXX_XXX.whl就可以了。在这一步中它会检查必要的包，然后自动给你安装上（所以上一步我说如果网速好，可以跳过安装numpy这一步）。    

tensorflow安装好了，进入tensorflow_ocr\Script\这个目录，执行activate.bat就会激活这个虚拟环境（仅仅相当于各种包以及python解释器是单独引入的），或者deactivate.bat来退出这个虚拟环境。