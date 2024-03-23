---
{"dg-publish":true,"permalink":"/CCD/LON/"}
---


## 如何让CCD程序接入光源

实现效果，CCD拍照前自动打开光源，完成则自动关闭光源。


<div align="center"><img src="https://tc.899900.xyz/img/202311072337047.png" width="30%" height="50%"></img></div>

如上图：
> 参数位置：右侧栏--任务--相机--"拍照完成"

説明：
- 拍照完成端口设定值≥100开启
- 关联IO端口「为设定值减去100，如图中设定值为100，此时100-100=0，即对应IO输出端口0」（将光源接入IO卡0号端口）

接线：
- 光源所在电源的输出端（输入220V输出24V），将24V的COM线（0V）与机器的COM点短接，光源的0V接到IO端口。

注意：
- 光源通电后由暗到这虽是线性，但是还是建议加50-100ms左右的延时，确保光源最亮状态

 <div align="center"><img src="https://tc.899900.xyz/img/202311072358971.png" width="30%" height="50%"></img></div>

- 此外，"IO发送延时"不可太短，如果出现光源亮了，但是还没正常取图就关闭了，通常就是"IO发送延时"太短，适当加长便可
---
---
<center><a href="https://www.jisicn.top" target="_blank">东莞集思光电科技有限公司</a></center>
<center><a href="https://www.jisicn.top" target="_blank">https://www.jisicn.top</a></center>
<center><a href="Https://www.dgjisi.eu.org" target="_blank">https://www.dgjisi.eu.org</a></center>

---
**如何获取最新CCD程序**

关注公众号，并发送 **“CCD”** 获取

<div align="center">
    <img src="https://cloud.jisi.cf/api/v3/file/source/1124/JISI%20%E5%85%AC%E4%BC%97%E5%8F%B7.jpg?sign=vxeGqA0B2Y-Yger8pV5Rxvdh6ZeBWi4fVG1Wm98bXNo%3D%3A0" width="40%" height="40%"></img>
</div>


------

<div align='center' ><font size='50'><b>End Thanks</b></font></div>