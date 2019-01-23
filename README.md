# aaron_camera_calibrate
相机标定，纯属个人从收集的资料中加上自己的理解，如有不准的地方，还请指出。  

相机的标定，其实可以说是三个坐标系下的矩阵变换：图像坐标系，相机坐标系，世界坐标系。  
首先来看图像坐标系与相机坐标系之间的关系  
![image](https://github.com/Aaronswei/aaron_camera_calibrate/blob/master/readme_screenshot/%E5%9B%BE%E5%83%8F%E5%92%8C%E7%9B%B8%E6%9C%BA%E5%9D%90%E6%A0%87%E7%B3%BB%E7%9A%84%E8%BD%AC%E6%8D%A2.png)  
![image](https://github.com/Aaronswei/aaron_camera_calibrate/blob/master/readme_screenshot/%E5%9B%BE%E5%83%8F%E5%9D%90%E6%A0%87%E7%B3%BB%E5%92%8C%E7%9B%B8%E6%9C%BA%E5%9D%90%E6%A0%87%E7%B3%BB%E4%B9%8B%E9%97%B4%E7%9A%84%E5%85%B3%E7%B3%BB.png)  
由图可知XCam=x/dx+x0, YCam=y/dy+y0  
其矩阵可以表示为  
![image](https://github.com/Aaronswei/aaron_camera_calibrate/blob/master/readme_screenshot/%E5%9D%90%E6%A0%87%E8%A1%A8%E7%A4%BA1.png)  
所以  
![image](https://github.com/Aaronswei/aaron_camera_calibrate/blob/master/readme_screenshot/%E5%9D%90%E6%A0%87%E8%A1%A8%E7%A4%BA2.png)  
可以写成  
![image](https://github.com/Aaronswei/aaron_camera_calibrate/blob/master/readme_screenshot/%E5%9D%90%E6%A0%87%E8%A1%A8%E7%A4%BA3.png)  
  
同时对于世界坐标系与相机坐标系的关系如下图  
![image](https://github.com/Aaronswei/aaron_camera_calibrate/blob/master/readme_screenshot/%E4%B8%96%E7%95%8C%E5%9D%90%E6%A0%87%E7%B3%BB%E4%B8%8E%E7%9B%B8%E6%9C%BA%E5%9D%90%E6%A0%87%E7%B3%BB%E5%85%B3%E7%B3%BB.png)  
表示成矩阵可以表示为  
![image](https://github.com/Aaronswei/aaron_camera_calibrate/blob/master/readme_screenshot/w2c%E8%A1%A8%E7%A4%BA1.png)  
那么可以推理出（这里的Xc,Yc,Zc就是所谓x，y，z）  
![image](https://github.com/Aaronswei/aaron_camera_calibrate/blob/master/readme_screenshot/w2c%E8%A1%A8%E7%A4%BA2.png)  
这里令K赋下值，得到的就是相机的内参也就是所谓畸变系数  
![image](https://github.com/Aaronswei/aaron_camera_calibrate/blob/master/readme_screenshot/w2c%E8%A1%A8%E7%A4%BA3.png)  