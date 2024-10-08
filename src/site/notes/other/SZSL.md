---
{"dg-publish":true,"permalink":"/other/SZSL/"}
---


**返回主页 [[JISI\|JISI]]**

---

# CCD程序更新
更新内容： 
- 名称统一
- 增加显示面面，将原先重复先后拍两次的画面分开显示

---

## **参数设定**
**增加画面**
1. 用户密码先后输入8、9901，然后右侧跳到设置--参数

![image.png](https://tc.jisicn.top/img/202304101854217.png)

2. 将相机数量加1，如现有2个画面增加到3个，将相机数量改为3；若现在3个需要加到4个，相机数量改为4

<div align="center"><img src="https://tc.jisicn.top/img/202304101855974.png" width="30%" height="50%"></img></div>

3. 再次点**用户**并输入密码“9900”，点登录后，右侧便会弹出隐藏的高级参数设定页面。
如图，假设当前是2个画观，需增加3个，按顺序将第三个“CCD3相机类型”改成与上面的一致，此时后面的“相机端口”根据实际需要设定，如想调用原先CCD1的同步画面将端口改为0，若是调用CCD2的同步画面则将端口改为1。

若是按图中设定CCD1与CCD2相机端口都是0，即表示第一个画面与第二个画面调用的是同一个相机；第三个画面为原先的第二个画面（调用另一个相机）

<div align="center"><img src="https://tc.jisicn.top/img/202304101909020.png" width="40%" height="50%"></img></div>


4. 自定义名称：相机备注从10开始为名称自定义，如将三个画面自定义为CCD1-1、CCD1-2、CCD2

    10改为CCD1-1
    11改为CCD1-2
    12改为CCD2

<div align="center"><img src="https://tc.jisicn.top/img/202304101914552.png" width="30%" height="50%"></img></div>


5. 完成后重启CCD程序

6. 将任务指定页面：走完以上步骤，已经实现了画面增加，到此最后可以将任务指向指定画面，如将CCD1-1显示在第一个画面则将图中数据包值改为0，若显示在第二个画面则改为1，放在第三个画面改为2。
图中，

	CCD1-1指向画面1，CCD1-1相机页面“数据包”0
	CCD1-2指向画面2，CCD1-2相机页面“数据包”1
	CCD2指向画面3，CCD2相机页面“数据包”2

<div align="center"><img src="https://tc.jisicn.top/img/202304101920316.png" width="30%" height="50%"></img></div>

6. 设定完成
---
---
**其它注意**
1、产品请尽量剧中调，避免靠单边，原因是你们要求端子要落在槽里，假如偏了，框也偏，容易抓到其它错误位置，如治具、塑胶（缺PIN时）
<div align="center"><img src="https://tc.jisicn.top/img/202304251656816.png" width="50%" height="50%"></img></div>

2、请及时清理治具上的杂物，避免误抓，严重的时候，刚好缺PIN，但是抓到杂物上造成错判。
<div align="center"><img src="https://tc.jisicn.top/img/202304251657496.png" width="50%" height="50%"></img></div>

