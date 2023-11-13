# Trochilus

Python 3
---
Python 3: Fundaments、Functional、Iteration、Generation、Dictionaries、Sets、JSON、OOP

# Python 3 Fundamentals

## 一、介绍

### 本课程内容

- Python的基本原理介绍
- 查看第三方Python库，以及如何安装。
- 学习Python中常见的第三方库。
    - 用于数值计算(numerical computations)
    - 用于操作数据集(manipulating data sets)
    - 用于图表数据(charting)

### 课程预览

- 安装和运行Python
- Python中的基本原理
    - 变量（算术运算符、逻辑运算符、布尔运算符）
    - 简单的数据类型（整型、浮点型、布尔类型等）
- Python中的控制流
    - 条件执行(if else)
    - 迭代器（iterables、iterators、loops）
    - 异常处理
- 高级数据类型
    - 序列类型（lists、tuples、strings）
    - 字典和集合
    - 日期与时间
    - 十进制数据类型(decimal)
- 函数式编程
    - 函数
    - 高阶函数
    - 闭包(closures)
    - 装饰器(decorators)
- 面向对象编程(object-oriented programming)
    - 自定义类
    - 方法
    - 属性
- 数据采集
    - 从CSV文件中获取数据
    - 从Web中获取数据(JSON)
- 第三方库
    - pytz - 处理时区和夏令时问题非常有用
    - dateutil - 对日期处理非常有用
    - requests - http请求库，使用它来查询api
    - numpy - 对数值分析很有用，特别是处理数组或矩阵
    - pandas - 对处理数据采集非常有用
    - matplotlib - 一个方便的图表库。

## 二、运行Python

### 1. 介绍

- 什么是Python？
- Python语言之间的区别？
- Python的不同实现？
- 如何安装Python？
- 如何拥有并行版本的Python？
- 虚拟环境(Virtual environments)
- 如何安装第三方库？
- 如何运行Python代码？

### 2. 什么是Python

#### 2.1 Python的历史？

- Python是由 `Guido van Rossum` 在`1989`年当他在荷兰的`CWI`工作时创建的。

#### 2.2 什么是Python？

- Python是一种编程语言，它不是应用程序。
    - Python有很多种实现，例如：`CPython`、`PyPy`。
    - 另外有许多更像是翻译器，在Python与其他语言之间进行代码转换：
        - IronPython 转换为 .NET
        - Jython 转换为 Java
        - Cython 转换为 C/C++
- 官方标准使用的是CPython。

#### 2.3 CPython

- CPython是官方参考(reference)实现。
- CPython是使用最广泛的Python发行版，它是开源的，并且用C语言写的。
- CPython实现还包括一个叫做标准库(standard library)的东西。
- CPython和标准库的这个实现是Python的正式(official)实现。
- 支持跨平台（Linux、Windows、Mac OS、iOS、Android、PlayStation、XBox、...）

### 3. 安装 Python

进入 [Python 官网](https://www.python.org)，点击 `Downloads` 菜单下载最新安装包进行安装。

### 4. 使用 Windows Python Launcher

#### 4.1 查看Python版本

查看Python默认版本：
```bash 
py --version
```

查看所有已安装的Python列表：
```bash
py --list
```

切换默认使用的Python版本：
```bash
py -3.10 --version
```

查看所有Python安装路径列表：
```bash
py --list-paths
```

### 5. 虚拟环境(Virtual Environments)

#### 5.1 创建虚拟环境

```bash
py -m venv test
```

激活虚拟环境
```bash
cd test\Scripts
activate.bat
```

停用虚拟环境
```bash
cd test\Scripts
deactive.bat
```

### 6. 安装第三方库

#### 6.1 pip

`pip`: Package Install for Python 

- pip是Python的包安装程序。
- pip允许我们管理包，很容易安装、更新和删除包。
- pip使用Python包索引 `https://pypi.org`，它是Python的官方第三方存储库。

#### 6.2 使用pip安装第三方包

- 激活虚拟环境
- 使用命令 `pip install <package_name>` 即可安装对应的包。
- 可以安装指定版本的包 `pip install <package_name> == 1.3.2`。
- 可以安装小于等于某个版本的包 `pip install <package_name> <= 1.2`
- 可以安装大于某个版本的包 `pip install <package_name> >= 2.0`

例如安装 `jupyterthemes`
```bash
pip install jupyterthemes
```

#### 6.3 requirements.txt 文件

`requirements.txt` 文件的作用就是与代码一起跟踪所需的包和版本。

requirements.txt
```
numpy==1.18.1
pandas==1.1.4
matplotlib==3.3.3
```

可以安装指定`requirements.txt`文件中的包
```bash
pip install -r requirements.txt
```