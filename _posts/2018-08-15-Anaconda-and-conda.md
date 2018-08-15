---
layout: article
title: Anaconda-and-conda
key: 100000
tags: Python学习
category: blog
date: 2018-08-15 01:00:00 +08:00
modify_date: 2018-08-15 13:00:00 +08:00
---

## 1.Package Manager

to install `numpy`

```
conda install package_name 
eg:conda install numpy
```
<!--more-->

install multiple packages

```
eg:conda install numpy scipy pandas
```

specify which version of a package you want

```
conda install numpy=1.10
```

Conda also automatically installs dependencies for you. 
For example `scipy` depends on `numpy`, it uses and requires `numpy`. If you install just `scipy` (`conda install scipy`), Conda will also install numpy if it isn't already installed.

To uninstall

```
conda remove package_name
```

To update

```
conda update package_name
```
update all packages
```
conda update --all
```
list installed packages
```
conda list
```
don't know the exact name of the package, searching with
```
conda search search_term
```
For example, I know I want to install `Beautiful Soup`, but I'm not sure of the exact package name. So, I try `conda search beautifulsoup`.

## 2.Managing environments

to create an environment named `my_env` and install `numpy` in it
```
conda create -n my_env numpy
```
to remove env
```
conda env remove -n env_name
```
to list all environments
```
conda info --envs or conda env list
```
entering an environment
```
source activate my_env（Windows环境下不需要source）
```
```
source deactivate my_env（Windows环境下不需要source）
```
when it comes to env migration, we'd better use pip
```
pip freeze > requirements.txt pip install -r requirements.txt
```


> 参考链接：
>
> [anaconda 常用指令](https://blog.csdn.net/andylei777/article/details/79008348)
>
> [Anaconda使用入门](https://www.cnblogs.com/baiyangcao/p/anaconda_basic.html)

