---
{"dg-publish":true,"permalink":"/other/modbus-tyd/"}
---


## Welcome to [东莞市集思光电科技有限公司 ](https://jisicn.top) ! 

<div align="center"><img src="https://tc.899900.xyz/img/202303301656475.jpg" width="100%" height="50%"></img></div>

---

## MODBUS设定

- 在参数页面信号切换选择“信捷PLC”

<div align="center"><img src="https://tc.899900.xyz/img/202403181748693.png" width="50%" height="50%"></img></div>

### 参数设定
- 先将“切换”设为1
- 与PLC确定IP地址及端口，IP段要一致，如（aaa.bbb.ccc.X）其中aaa.bbb.ccc与PLC同IP段，最后一个X可以随意，但是与PLC已分配的重复。

<div align="center"><img src="https://tc.899900.xyz/img/202403181751496.png" width="50%" height="50%"></img></div>

### 启动端口设定

- 图中参数页“写起始字”设定接收起始地址
	- 如设定“0”表示接收PLC中 M0 开始到M15，即 M0-M15 16个线圈的状态。
	- 如设定“100”表示接收PLC中 M100-M115 16个线圈的状态
- 当前相机取16个线圈中的哪一个线圈作启动，与IO卡的设定一致，“相机参数页面”中启动参数来控制，如设定为“0”表示取16个里面的第一个，如“1”表示取16个里面的每二个……


<div align="center">
<figure class="half">
<img src="https://tc.899900.xyz/img/202403181756837.png" width="40%" height="50%"> 
<img src="https://tc.899900.xyz/img/202403181803267.png" width="40%" height="50%"> 
</figure></div>


### 发送端口设定

- "address1"表示设定发送数据的起始端口，与上方启动端口类似，实际对应线圈的端口 = address1 + OK/NG端口设定值（相机页面）
- “address2”表示数据中“标签”算法中写数据的地址，如我们要将数据写入到PLC的 "D100"，此时就将“address2”设为 “100”

<div align="center"><img src="https://tc.899900.xyz/img/202403181806839.png" width="50%" height="50%"></img></div>

- 算法：标签
- 数据源：200 表示通过modbus写数据
- 参数配制：设定需发送哪一个数据到PLC
	- 注：此序号之前的数据
- 参数配制1: 获取前数据，并判断正负，>=0时，最终数据=（实际数据+数据源1）x 数据源2（放大倍数）
- 标准值2与正公差2 ：角度显示位置X Y坐标

<div align="center"><img src="https://tc.899900.xyz/img/202403181812333.png" width="50%" height="50%"></img></div>

### ROI设定
- 定位
- 点面积：辅助5为100开启任意形状ROI抓取面积
- 辅助3=200： 开启秦元达定制
- 辅助4=0: 水平旋转，非0时坚直旋转

### IO设定
- M4000-M4015: 启动
	- M4000 启动CCD1
	- M4001 启动CCD2
	- M4002 启动 任务3 （新增）
- M4020-M4035: 输出
	- M4020 正反OK
	- M4021 正反NG
	- M4022 有产品
	- M4023 无产品
	- M4024 第二次拍照测试完成
	- M4025 任务3_OK（新增）
	- M4026 任务3_NG（新增）
- D2000: 写角度数据

### 流程
第一次测试，识别正反
第二次测试，计算角度
第三次测试，通过第二次计算机构旋转将产品摆正，再拍第三次，进一下确认角度是否OK

---
---


<div align="center">
    <img src="https://tc.899900.xyz/img/JS_YX_022.jpg" width="100%" height="60%"></img>
</div>

<div STYLE="page-break-after: always;"></div>

<div align="center"><img src="https://tc.899900.xyz/img/202304122151817.JPG" width="100%" height="50%"></img></div>


---


<center><a href="Https://www.jisicn.top" target="_blank">东莞集思光电科技有限公司</a></center>
<center><a href="Https://www.jisicn.top" target="_blank">https://www.jisicn.top</a></center>
<center><a href="Https://www.dgjisi.eu.org" target="_blank">https://www.dgjisi.eu.org</a></center>

---

<div align='center' ><font size='50'><b>End Thanks</b></font></div>