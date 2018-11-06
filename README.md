####	git组件代码：[displayPartText](https://github.com/xushankun/displayPartText)
####	一、需求
1.文本很多时【收起来，保留指定3行】
![partText1](https://shankun-1257055090.cos.ap-chengdu.myqcloud.com/blog/displayPartText/partText1.png)

2.展开后【变为收起来的按钮】
![partText2](https://shankun-1257055090.cos.ap-chengdu.myqcloud.com/blog/displayPartText/partText2.png)

3.又或者我们还有这样的情况，当文字小于等于3行的时候【不显示按钮】
![partText3](https://shankun-1257055090.cos.ap-chengdu.myqcloud.com/blog/displayPartText/partText3.png)

####	二、组件属性
1.	textLineHeight【文本行高：number类型默认值52，单位rpx】
2.	lineNumber【显示行数：number类型默认值2,】
3.	showBtnText【显示按钮文本，string类型默认值‘更多内容’】
4.	hideBtnText【隐藏按钮文本，string类型默认值‘收起来’】
5.	btnShowPosition【按钮显示位置，string类型默认值‘bottom’，可选值rightBottom显示为右下角显示如下图】
![partText4](https://shankun-1257055090.cos.ap-chengdu.myqcloud.com/blog/displayPartText/partText4.png)
