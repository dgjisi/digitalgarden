---
{"dg-publish":true,"permalink":"/Algorithm/"}
---


---

**返回主页 [[JISI\|JISI]]**

---

## 算法
#### 1.  X算法
	1. 数据源默认，计算水平方向两点X距离 
	2. 数据源为200，计算任意两点间距离
#### 2. Y算法
	1. 数据源默认，计算竖直方向两点Y距离 
	2. 数据源为-10，当参数配制0与1计算NG时，再次计算参数配制0与2的值
#### 3. 点到线
	1. DistanceY
		1. 默认0，没抓到点时为无穷大，此时数据显示NaN
		2. -1，进入作弊模式，让数据在区间内跳动
		3. -5，没抓到点时将标准值传入
#### 4. 自启动循环：
- 第一个点面积ROI
	- 辅助3=100，连续测试
	- 辅助3≠100，当面积为TRUE时拍一次，FALSE到TRUE拍一次
#### 5. 数据_发送IO
数据源：
	0 ：IO卡
	1 ：MODBUS
	2 ：机械手 JSON数据

MODBUS通讯时数据源 1 :
	0 ：发送单个数据值到PLC寄存器
		参数配置 ：起始值「指向PLC地址」
		参数配置1 ：数据索引「指向CCD中数据序号」
	1 ：发送多个数据值「同时发送两个数据值，格式 ==符号+数据+符号+数据== 其中符号0为+，2为-」
		参数配置 ：起始值
		参数配置1 ：数据索引
		参数配置2 ：数据索引
	2 ：发送坐标数据「直接引用ROI序号」
		参数配置 ：起始值
		参数配置1 ：ROI索引「通常配合匹配模式」
	3 ：写线圈「改变PLC指定线圈的状态，ON或OFF」
		参数配置 ：PLC线圈地址「类似OK端口」
		参数配置1 ：PLC线圈地址「NG端口」
#### 6. 找圆
+ 辅助3 ：
	+ 默认 ：找圆心
	+ 2 ：扫描圆或圆弧缺口
+  辅助5 ：设定缺口不良距离值，默认设为4

#### 7.数据_角度
数据源1 ：当测试角度大于设定值，自动减去360，从而转换成负角度「如测试结果为359度，转换后为-1度」

#### 8. 三点抓圆心
扫描方向 ： 前两点
Average ：点的数量，最小为3，三点确定圆心
辅助4 ：=100，显示圆心坐标








---
## 直接通过ROI像素计算共面度（不计算数据）
- 数据项中增加数据，算法选"共面度"
- "数据源"设定500开启
- "参数配置0"设为ROI中的组号
此时设定完成，计算的数据为ROI组的最大与最小像素坐标的落差