# Android P support 28.0.0-alpha1 Design 库预览
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

![](https://user-gold-cdn.xitu.io/2018/4/3/1628aad880119b7d?w=350&h=618&f=png&s=29266)
开发过程中需要做的调整
```
    compileSdkVersion 'android-P'
    implementation"com.android.support:appcompat-v7:$support_version"
    implementation"com.android.support:design:$support_version"
（ext.support_version = '28.0.0-alpha1'）
```

* `BottomAppBar` (官方说法是说`BottomAppBar` 像是`FloatingActionButton`的摇篮（翻译的有点怪不过看效果好像有那么点意思）)
    Bottom App bar 是`Toolbar`一种拓展，配合`FloatingActionButton`使用，`FloatingActionButton` 设置关联
到`BottomAppBar`,当然需要用到`CoordinatorLayout`作为它们的父级元素。
    * 要更改背景，您应该调用`app:backgroundTint`而不是`android:background`
    * `setTitle`，`setSubTitle`被覆盖不再起作用
* `Chip` `ChipGroup` 标签和标签组
`Chip` 通过设置 
    *  `style="@style/Widget.MaterialComponents.Chip.Filter"`
    *  `style="@style/Widget.MaterialComponents.Chip.Action"`
    *  `style="@style/Widget.MaterialComponents.Chip.Choice"`
来决定`Chip`类型，`ChipGroup` 可以设置为标签组为单选标签 `app:singleSelection="true"`
* `MaterialCardView` 
添加了添加了`strokeColor` ,`strokeWidth`属性
* `MaterialButton`
  * 本身圆角按钮 `app:cornerRadius`
  * 图标按钮 `app:icon` 可以控制图标位置和颜色
  * 要更改背景，您应该调用`app:backgroundTint`而不是`android:background`
