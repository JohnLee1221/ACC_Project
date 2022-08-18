# ACC_Project
A project of acc function



# 1.算法框图

![image-20220818160154201](C:\Users\lzh\AppData\Roaming\Typora\typora-user-images\image-20220818160154201.png)

------





## 1.1.输入

### 			整车参数

<img src="C:\Users\lzh\AppData\Roaming\Typora\typora-user-images\image-20220818160920548.png" alt="image-20220818160920548" style="zoom:80%;" />

​						a：车长；

​						b：车宽；

​						m：整车质量；

​						Cαf：前轮侧偏刚度；

​						Cαr：后轮侧偏刚度；

​						I：整车惯量；



### 			车辆状态

<img src="C:\Users\lzh\AppData\Roaming\Typora\typora-user-images\image-20220818162232850.png" alt="image-20220818162232850" style="zoom: 80%;" />

<img src="C:\Users\lzh\AppData\Roaming\Typora\typora-user-images\image-20220818162404434.png" alt="image-20220818162404434" style="zoom:80%;" />

​						x：横向坐标；

​						y：纵向坐标；

​						φ：横摆角；

​						vx：横向速度；

​						vy：纵向速度；

​						φ`：横摆角速度；

### 			规划

<img src="C:\Users\lzh\AppData\Roaming\Typora\typora-user-images\image-20220818162327066.png" alt="image-20220818162327066" style="zoom:80%;" />

​						xr：规划轨迹的横坐标；

​						yr：规划轨迹的纵坐标；

​						θr：航向角，规划轨迹速度与x的夹角；

​						kr：规划曲线的曲率；





## 1.2.输出



------



# 2.runtime 步骤



## 2.1.carsim 设置

carsim车辆参数：略。

carsim输入：I/O Channels:export

<img src="C:\Users\lzh\AppData\Roaming\Typora\typora-user-images\image-20220818163237756.png" alt="image-20220818163237756" style="zoom:150%;" />

carsim输出：I/O Channels:import

![image-20220818163528109](C:\Users\lzh\AppData\Roaming\Typora\typora-user-images\image-20220818163528109.png)



 注意事项：

- carsim中的车辆质量：m = Sprung mass（簧上质量）+  Unsprung mass（悬架质量）*  2；
- carsim侧偏刚度，从Touring Tires中查找轮胎的垂向力对应的曲线，求斜率；
- carsim侧偏刚度的单位为：N/度，算法侧偏刚度单位为：N/弧度，单位需要换算；
- 算法侧偏刚度：carsim侧偏刚度*2 （算法为自行车模型）；
- 算法侧偏刚度为负值；
- Vehicle Body中把Aerodynamics选项关闭掉；

## 2.2.




![企业微信截图_16576042833607](https://user-images.githubusercontent.com/91543040/185382167-a3d0de90-fa5b-4ebb-8868-37c27737765d.png)



