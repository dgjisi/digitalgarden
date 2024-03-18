---
{"dg-publish":true,"permalink":"/other/modbus/"}
---


# Welcome to [东莞市集思光电科技有限公司 ](https://jisicn.top) ! 

![Rsa7uSlt_0602-04.jpg](https://tc.899900.xyz/img/202303301656475.jpg)

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

<div align="center"><img src="https://tc.899900.xyz/img/202403181812333.png" width="50%" height="50%"></img></div>


---
---


<div align="center">
    <img src="https://tc.899900.xyz/img/JS_YX_022.jpg" width="80%" height="60%"></img>
</div>

<div STYLE="page-break-after: always;"></div>

![水印产品图.JPG](https://tc.899900.xyz/img/202304122151817.JPG)


---


<center><a href="Https://www.jisicn.top" target="_blank">东莞集思光电科技有限公司</a></center>
<center><a href="Https://www.jisicn.top" target="_blank">https://www.jisicn.top</a></center>
<center><a href="Https://www.dgjisi.eu.org" target="_blank">https://www.dgjisi.eu.org</a></center>

---

<div align='center' ><font size='50'><b>End Thanks</b></font></div>