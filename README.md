# Revision 28.0.0 Alpha 1
2018三月，发布了Android p 预览版。想了解具体变化可以查看
<a href="https://developer.android.com/preview/release-notes.html">release notes</a>
这里重点看下MD设计相关的内容
* 加入了新的主题 
```
Theme.MaterialComponents
```
* 新添加Components

```
BottomAppBar
Chip
ChipGroup
MaterialButton
MaterialCardView
```
效果如下
![](https://user-gold-cdn.xitu.io/2018/4/3/1628a89ca64a361d?w=387&h=690&f=png&s=49057)
开发过程中需要做的调整
```
compileSdkVersion 'android-P'
implementation"com.android.support:appcompat-v7:$support_version"
（ext.support_version = '28.0.0-alpha1'）
```
