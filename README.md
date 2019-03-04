# PythonAndOpencv
手把手教你python、opencv的安装以及环境调试  
# 一.python的安装：  
python可以在不同的平台运行，以下是各个平台安装包的下载地址：  
https://www.python.org  

这里我们举例安装在windows 10系统下的64位处理器机器上：  
打开 WEB 浏览器访问https://www.python.org/downloads/windows  

![image](http://www.runoob.com/wp-content/uploads/2013/11/721E917D-CCA5-4F37-8FD6-486315EC8CF8.png)   
这里我们选择最新的稳定版本3.7.2，链接https://www.python.org/downloads/release/python-372/  
根据自己的机器型号选择相应的版本：  
![image](http://www.runoob.com/wp-content/uploads/2013/11/20180711-160607.png)  
按照指示点击下一步即可。  
  
  
特别需要注意的是，安装过程中请勾选“ADD PYTHON TO PATH”！  
![image](https://ss0.baidu.com/6ONWsjip0QIZ8tyhnq/it/u=961199589,1814899440&fm=173&app=25&f=JPEG?w=640&h=394&s=7992AF1B1D5C5CCC02D9C5DE0200D0B2)  
这一步是用来自动调试系统环境变量，免去了之后手动调试的工作。  

python安装好之后，我们要检测一下是否安装成功，用系统管理员打开命令行工具cmd，输入“python -V”,然后敲回车，如果出现如下界面，则表示我们安装成功了；  
![image](https://github.com/Nocami/PythonAndOpencv/blob/master/gabbage/QQ%E6%88%AA%E5%9B%BE20190304122730.jpg)  
# 二.OpenCV：Python下OpenCV安装  
有两种方法进行对应版本opencv安装。  
①第一种：  
打开命令提示符，输入 pip install opencv-python  ，开始自动安装。  
②第二种：  
先去官网https://www.lfd.uci.edu/~gohlke/pythonlibs/#opencv ，下载相应Python版本的OpenCV的whl文件，如本人下载的opencv_python‑4.0.1‑cp37‑cp37m‑win_amd64.whl，然后在whl文件所在目录下，
命令 pip install opencv_python‑4.0.1‑cp37‑cp37m‑win_amd64.whl 进行安装即可  
安装成功如图：  
![image](https://github.com/Nocami/PythonAndOpencv/blob/master/gabbage/2.jpg)  
接下来我们进行测试，在命令提示行输入“python”  
![image](https://github.com/Nocami/PythonAndOpencv/blob/master/gabbage/3.jpg)  
再输入“import cv2”，出现下图即意味着大功告成啦：  
![image](https://github.com/Nocami/PythonAndOpencv/blob/master/gabbage/4.jpg)  
再测试一下我们的相应代码，打卡库中的test.py,源码如下：  
#导入cv模块  
import cv2 as cv  
#读取图像，支持 bmp、jpg、png、tiff 等常用格式  
img = cv.imread("E:\Study\image_processing\ch2\Fig0228(a).tif")  
#创建窗口并显示图像  
cv.namedWindow("Image")  
cv.imshow("Image",img)  
cv.waitKey(0)  
#释放窗口  
cv2.destroyAllWindows()   
图片打开正常，测试成功。  

![image](https://github.com/Nocami/PythonAndOpencv/blob/master/gabbage/4.jpg)
