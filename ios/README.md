
# About

罗列一些 iOS 开发相关的网址或者内容

## 参考书

- [objccn](https://objccn.io/issues/): ObjC 中国

## 语言细节

- [+load() 及 +initialize()](https://www.jianshu.com/p/af36edff5d4e): +load() 类加载时候触发，每个 category 的实现都会调用；+initialize() 被使用的时候调用，编译顺序最后的 initialize 会覆盖所有
- [MRC 与 ARC](https://www.jianshu.com/p/5eac83471b23): 栈区、堆区、全局区、常量区、代码区、 自由存储区；MRC 手动引用计数，ARC 自动引用计数，编译器在合适地方插入 release 消息
- [Runtime](https://www.jianshu.com/p/2414d5db0852): 获取类名、方法、类实例变量、父类接口
- [Category 与 Extension](https://www.jianshu.com/p/cafb774ab81f): 一个类可有多个 Category，装饰者模式，部分类函数加载顺序、次数跟编译顺序相关；Extension 是匿名分类，可以加载属性，仅有一个
- [GCD 多线程](https://www.jianshu.com/p/bdb39ff9d095): main、hight、low、default、background global queue，cocurrent、serial queue，dispatch_once，dispatch group，source
- [NSOperation](https://www.jianshu.com/p/9382e8409bc7): NSTread、GCD、NSOperation 多线程，系统提供的抽象程度最高，最为细粒度控制的方式
- [KVO 用法及原理](https://www.jianshu.com/p/bcaf178a4b23): C 接口注册回调函数并监听，dealloc 前反注册，原理是在 runtime 动态插入了一个桩 class，转发相关属性的读取

## UI 相关

- [CALayer 的 mask](https://www.jianshu.com/p/2c91564546c7): mask layer 中 backgroundColor 的 alpha 控制 layer 的显示区域透明程度，opacity 控制是否显示
- [状态栏的控制](https://www.jianshu.com/p/7c969c075fbb): iPhoneX 及之后，状态栏高度 44，iOS11 及以上，增加了 SafeArea 判断状态栏高度；导航栏高度 44
- [UITableView 性能优化](https://www.jianshu.com/p/0014f736b130): 重用 cell、预计算高度、移步加载图片、优化渲染
- [离屏渲染](https://github.com/seedante/iOS-Note/wiki/Mastering-Offscreen-Render): 根据 iPad1 上测试得到的数据，相比大路货推荐的创建纯色覆盖板、裁剪图片，使用混合图层的效果较好
- [MVVM](https://objccn.io/issue-13-1/): 减少 ViewController 的复杂性，ViewModel 跟 view 的数据绑定，比如使用 ReactCocoa