# Jupyter内核配置：Python+Stata+R 😎

Python、Stata和R是数据科学常用的编程工具。通过Jupyter，可以将这三种工具集成在一起，协同完成数据分析任务，让数据分析更加省时高效。🚀

## 第一步：安装基础软件 📦

1. 下载并安装Anaconda（自带JupyterLab）。
   - [Anaconda下载链接](https://www.anaconda.com/download) 🐍

2. 安装R（支持各个版本），并找到程序启动目录。
   - 例如："D:/R-4.3.2/bin/x64/R"
   - [R下载链接](https://mirrors.tuna.tsinghua.edu.cn/CRAN/) 📈

3. 安装Stata（支持各个版本），并找到程序启动目录。
   - 例如："D:/stata17/StataMP-64.exe" 📊

## 第二步：配置R内核 🔧

1. 启动R。
2. 在R中安装`IRkernel`包，并将其注册到Jupyter。
   ```R
   install.packages('IRkernel')
   IRkernel::installspec(user = FALSE)
   ```

## 第三步：配置Stata内核 🔨

1. 启动Jupyter或者Anaconda Prompt。
2. 在命令行界面中安装`stata_kernel`。
   ```bash
   pip install stata_kernel
   ```
3. 安装`stata_kernel`包后，运行配置命令。
   ```bash
   python -m stata_kernel.install
   ```

## 第四步：检查配置结果 🕵️‍♂️

1. 运行命令，查看内核配置文件的位置。
   ```bash
   jupyter kernelspec list
   ```
2. 输出示例：
   ```
   Available kernels:
     python3    D:\anaconda3new\envs\deep_learning\share\jupyter\kernels\python3
     ir431      C:\Users\Administrator\AppData\Roaming\jupyter\kernels\ir431
     stata      C:\Users\Administrator\AppData\Roaming\jupyter\kernels\stata
   ```
3. 打开目录下的`kernel.json`，可以修改内核信息。
   - 将R的名称增加上版本信息，`"display_name": "R 4.3.2"` 📘
   - Stata的名称增加上版本信息，`"display_name": "Stata17MP"` 📙
4. 重启Jupyter，新建文件时可以看到有Python、R 4.3.2和Stata17MP三个内核可选。 🔄

<p align="center">
  <img src="result.png" width="50%"/>
</p>

