Egret Engine 3.0 包含了白鹭时代研发的遵循HTML5标准的2D引擎及全新打造的3D引擎，它解决了HTML5性能问题及碎片化问题，灵活地满足开发者开发2D或3D游戏的需求，并有着极强的跨平台运行能力。

下面介绍 Egret Engine 3.0.4 到 Egret Engine 3.0.5 之间的更新详情。

### Egret Engine 2D 

在 Egret Engine 2D 的 本次更新中，我们吸收开发者提供的反馈和建议，进一步稳定引擎并重构底层部分功能模块，使引擎更加高效稳定。下面列出的是 3.0.4 到 3.0.5 的更新详情。

#### 重构矢量绘图模块

在本次更新中我们重构了引擎底层的矢量绘图模块，优化矢量绘图的渲染结构，简化底层对 Canvas API 的调用。使用更为有效的方式构建底层渲染结构，使在绘制复杂矢量图形尤其是在生成 Native 项目时的稳定性大大提高。 

#### 重构显示列表渲染

在本次更新中我们重构了显示列表渲染方式，不再直接使用 Canvas 的 Context 2D 直接进行渲染，而是使用统一的渲染节点进行管理。渲染节点将统一管理显示对象的所有属性，当需要的时候统一进行渲染。当我们操作显示对象时实际在操作其渲染节点中保存的属性。可以在一定程度上提升渲染性能。

本次底层重构中不会修改任何 API，只是底层提供更稳定的架构并提升部分性能。需要注意的是如果原有依赖底层渲染方式或矢量绘图的第三方库或者功能是需要参照新的引擎底层手动进行修改的。

#### 修复问题

* 修复编译 Map 或者 WeakMap 报错问题。
* 修复编译第三方库可能会编译出重复内容问题。
* 修复 Native 下图片宽度为 0 显示异常问题。
* 修复 native_require.js 可能会被清空问题。
* 修复某些情况下输入文本不自动换行问题。
* 修复 eui.ItemRenderer 某些情况 stage 为空报错问题。（感谢开发者 丶守望灬稻田）
* 修复多个输入框在pc端浏览器来回切换焦点会出现报错问题。（感谢开发者 feng zhi hao）
* 修复 eui.Scroller 嵌套使用时，底层的 Scroller 不能滚动问题。（感谢开发者 缺氧）

### Egret Engine 3D

在 Egret Engine 3D 的 本次更新中，我们吸收开发者提供的反馈和建议，修复了一些问题。

#### 修复问题

* 修复切换模型贴图的问题。
* 修复骨骼动画法线没有计算的问题。
   
#### 联系我们

[获取 Egret Engine 3D 的源码](https://github.com/egret-labs/egret-3d)。

[Egret Engine 3D API](http://edn.egret.com/cn/apidoc/index/name/egret3D.AnimaNodeCollection)。

更多关于 Egret Engine 3D 的教程欢迎关注 EDN [Egret Engine 3D 分类](http://edn.egret.com/cn/docs/page/775)。

在体验的过程中如果遇到任何问题希望您能留下宝贵意见，更欢迎大家在 Egret Engine 3D 论坛交流:[Egret3D 交流贴](http://bbs.egret.com/forum.php?mod=viewthread&tid=15653)。

Egret Engine 3D 官方交流群: 180593985 。

Egret Engine 2D 最新官方交流群: 343030940 。

### 获取 Egret Engine

Windows 安装包下载地址：[点击这里](http://tool.egret-labs.org/EgretEngine/EgretEngine-v3.0.5.exe)
Mac 安装包下载地址：     [点击这里](http://tool.egret-labs.org/EgretEngine/EgretEngine-v3.0.5.dmg)
Egret Engine 2D 源码地址：[点击这里](https://github.com/egret-labs/egret-core/tree/v3.0.5)
Egret Engine 3D 源码地址：[点击这里](https://github.com/egret-labs/egret-3d)
