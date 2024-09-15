---
{"dg-publish":true,"permalink":"/other/free-agreement/"}
---


## Welcome to [东莞市集思光电科技有限公司 ](https://jisicn.top) ! 

<div align="center"><img src="https://tc.jisicn.top/img/202303301656475.jpg" width="100%" height="50%"></img></div>

---

## 开瓶器__自由协议

### 一、启动CCD

- 在参数页面信号切换选择 **“自由协议”**
- 启动数据为 **01 02 03**

下图为启动CCD的PLC示例，H31 H32 H33为数据，解码后为01 02 03，H75 H7A为CRC校验数据。

![83efcf76b379dbe7fbea818a5e45520.jpg](https://tc.jisicn.top/img/202403201600931.jpg)

![ea76421923c0ebf6b5e738972f60a5c.jpg](https://tc.jisicn.top/img/202403201603916.jpg)

### 二、写数据

- 格式为 **AA%sBB** , AA为帧头，BB为帧尾，%s为数据

### 二、模版设定

- 一、ROI算法
	- 定位，抓圆心定位
	- 点面积：任意形状抓取面积，ROI为圆
		- **辅助5=100** 开启
		- **标签=开瓶器**
- 二、两点一线
	-  **辅助5=1000，MIN=？** 指定前面点面积的ROI，如果成功，图像中会出现黄色参考线
- 三、手动基准线
	- 能过一、二步成功取得参考线，再手动加一条参考线做角度计算
- 四、数据设定
	- 算法角度
		- **数据源1=100** ，写串口数据
- 五、另一种发送数据方式
	- 算法：标签
	- 数据源：300发送自动协议数据(200为modbus数据)
	- 参数配制：指定要发送的数据

![6cc688b6e820933c5a387df76ec2957.jpg](https://tc.jisicn.top/img/202403201624885.jpg)

---
---


<div align="center">
    <img src="https://tc.jisicn.top/img/JS_YX_022.jpg" width="100%" height="60%"></img>
</div>

<div STYLE="page-break-after: always;"></div>

<div align="center"><img src="https://tc.jisicn.top/img/202304122151817.JPG" width="100%" height="50%"></img></div>

---


<center><a href="Https://www.jisicn.top" target="_blank">东莞集思光电科技有限公司</a></center>
<center><a href="Https://www.jisicn.top" target="_blank">https://www.jisicn.top</a></center>
<center><a href="Https://www.dgjisi.eu.org" target="_blank">https://www.dgjisi.eu.org</a></center>

---

<div align='center' ><font size='50'><b>End   Thanks</b></font></div>
<div align='center'><font size='3'><b>联系人：周生  18029199900 「dgjisi@foxmail.com」</b></font></div>

