####	git组件代码：[displayPartText](https://github.com/xushankun/displayPartText)
####	需求
1.文本很多时【收起来，保留指定3行】
![partText1](https://shankun-1257055090.cos.ap-chengdu.myqcloud.com/blog/displayPartText/partText1.png)

2.展开后【变为收起来的按钮】
![partText2](https://shankun-1257055090.cos.ap-chengdu.myqcloud.com/blog/displayPartText/partText2.png)

3.又或者我们还有这样的情况，当文字小于等于3行的时候【不显示按钮】
![partText3](https://shankun-1257055090.cos.ap-chengdu.myqcloud.com/blog/displayPartText/partText3.png)

####	组件属性
1.	textLineHeight【文本行高：number类型默认值52，单位rpx】
2.	lineNumber【显示行数：number类型默认值2,】
3.	showBtnText【显示按钮文本，string类型默认值‘更多内容’】
4.	hideBtnText【隐藏按钮文本，string类型默认值‘收起来’】
5.	btnShowPosition【按钮显示位置，string类型默认值‘bottom’，可选值rightBottom显示为右下角显示如下图】
![partText4](https://shankun-1257055090.cos.ap-chengdu.myqcloud.com/blog/displayPartText/partText4.png)

####	组件方法
actionHandle隐藏显示时的回调

返回值为true时是show的回调，false时是hide的回调

####	组件使用
第一步index.json里引用
```javascript
{
  "usingComponents": {
    "displayPartText": "../components/display-part-text/display-part-text"
  }
}
```
第二步index.html
```javascript
<displayPartText lineNumber="3" textLineHeight="52" bind:actionHandle="actionHandle">雨静悄悄地下着，只有一点细细的淅沥沥的声音。桔红色的房屋，像披着鲜艳的袈裟的老僧，垂头合目，受着雨底洗礼。那潮湿的红砖，发出有刺激性的猪血的颜色和墙下绿油油的桂叶成为强烈的对照。灰色的癞蛤蟆，在湿烂发霉的泥地里跳跃着；在秋雨的沉闷的网底，只有它是唯一的充满愉快的生气的东西。它背上灰黄斑驳的花纹，跟沉闷的天空遥遥相应，造成和谐的色调。它噗通噗通地跳着，从草窠里，跳到泥里，溅出深绿的水花。</displayPartText>
```
第三步index.js
```javascript
 actionHandle(e){
    if (e.detail){
      console.log('show')	// 显示回调
    } else {
      console.log('hide')	// 收起回调
    }
  },
```