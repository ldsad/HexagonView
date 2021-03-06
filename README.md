# HexagonView
六边形带圆角的自定义View，支持图文混排，点击区域，水平垂直方向切换，圆角大小等各种属性

### 联系方式
 * 邮箱地址： liaojeason@126.com
 * QQ群： 489873144 （建议使用QQ群，邮箱使用较少，可能看的不及时）
 * 本群刚建立，旨在为使用我的github项目的人提供方便，如果遇到问题欢迎在群里提问。个人能力也有限，希望一起学习一起进步。


## 演示
 ![image](http://7xss53.com2.z0.glb.clouddn.com/hexagonview/demo0.png)![image](http://7xss53.com2.z0.glb.clouddn.com/hexagonview/demo2.gif)![image](http://7xss53.com2.z0.glb.clouddn.com/hexagonview/demo1.gif)

## 1.用法

该项目和我github上其他的view相关的项目已经一起打包上传到jCenter仓库中（源码地址 [https://github.com/jeasonlzy0216/ViewCore](https://github.com/jeasonlzy0216/ViewCore) ），使用的时候可以直接使用compile依赖，用法如下
```java
	compile 'com.lzy.widget:view-core:0.1.9'
```
或者使用
```java
    compile project(':hexagonview')
```

## 2.注意
由于该控件不是矩形，所以想要点击事件只在六边形区域有效，需要设置`OnHexagonViewClickListener`，代码如下：
```java
 hexagon.setOnHexagonClickListener(new HexagonView.OnHexagonViewClickListener() {
	@Override
	public void onClick(View view) {
	    Toast.makeText(HexagonActivity.this, "点击六边形了！", Toast.LENGTH_SHORT).show();
	}
});
```

## 3.参数含义

<table>
  <tdead>
    <tr>
      <th align="center">自定义属性名字</th>
      <th align="center">参数含义</th>
    </tr>
  </tdead>
  <tbody>
    <tr>
      <td align="center">hexagonText</td>
      <td align="center">文字内容</td>
    </tr>
    <tr>
      <td align="center">hexagonTextSize</td>
      <td align="center">文字大小</td>
    </tr>
    <tr>
      <td align="center">hexagonTextColor</td>
      <td align="center">文字颜色</td>
    </tr>
    <tr>
      <td align="center">hexagonBorderWidtd</td>
      <td align="center">边框宽度</td>
    </tr>
    <tr>
      <td align="center">hexagonBorderColor</td>
      <td align="center">边框颜色</td>
    </tr>
    <tr>
      <td align="center">hexagonFillColor</td>
      <td align="center">背景填充色</td>
    </tr>
    <tr>
      <td align="center">hexagonCorner</td>
      <td align="center">圆角大小</td>
    </tr>
    <tr>
      <td align="center">hexagonBreakLineCount</td>
      <td align="center">换行字节数，一个中文代表两个字节</td>
    </tr>
    <tr>
      <td align="center">hexagonMaxLine</td>
      <td align="center">允许的最大行数，超过显示...</td>
    </tr>
    <tr>
      <td align="center">hexagonTextSpacing</td>
      <td align="center">每行文本的间距</td>
    </tr>
    <tr>
      <td align="center">hexagonBorderOverlay</td>
      <td align="center">边框是否覆盖在背景之上</td>
    </tr>
    <tr>
      <td align="center">hexagonOrientation</td>
      <td align="center">六边的的方向，横向和</td>
    </tr>
  </tbody>
</table>
