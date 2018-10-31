2018年10月31日

### Android系统

#### Android系统历史简介
Android 是 Google 公司专门为移动设备开发的平台，其中包括操作系统，中间件和核心应用。Android 最初由Andy Rubin (安卓之父）创办。Google 公司于 2005 年收购了成立约 22 个月的 Android  公司，开始了短信、手机检索、定位等业务，进入了基于 Linux 平台的开发。Google 公司在 2007年 11 月 5 日正式公布了这个平台，之后由开放手机联盟 （Open Handset Alliance）开发。Open Handset Alliance  组织由一群共同致力于构建更好的移动电话的公司组成。这个组织由 Google 领导，包含了移动运营商、手持设备制造商、零部件制造商、软件解决方案和平台提供商以及市场营销公司。

#### Android 平台架构（重点）

![Android 平台架构图](../images/android系统/002wuwKBgy6HLRRhnij33.png)

从图中我们可以清楚的认识到 Android 分为 **`4`** 层架构（ 5 层架构就多了一层硬件抽象层 HAL：hardwork abstract layer），层次分明。  
1. **application层**。application 层位于最顶层，程序员接触最多的一层，系统已经编写好大量的 api，我们直接调用对应的 API 就可以编写完成我们想要的应用程序。在这一层中主要 Android 的四大组件和响应的 ui 组件。
2. **application framework 层**。这一层具体是对应的 application api 中实现的底层，一般是资源管理器等核心，比如说 Resource Manager, Notification Manager ,Activity Manager , Content Providers  等等。
3. **libraries 层和虚拟机** 。这一层主要是不同的运行库，一般都是 c++ 编写的运行库。比如说， libc （从 BSD 继承来的标准 C 系统函数库）、媒体库，SGL (2D图形引擎)，OpenGL|ES (3D图形引擎)，Sqlite(数据库引擎)。最后还包括一个核心库。一开始是一个 Dalvik 虚拟机，后来 5.0 之后采用的是 ART（Android RunTime） 虚拟机。Dalvik 虚拟机执行 .dex 文件，同时该虚拟机是基于寄存器的，所有类都经过 java  编译器编译，然后通过 SDK 中的 dx 工具转换成对应的 .dex 文件，由虚拟机执行。
4. **Linux kernel层**。最底层的都是相关的 Linux kernel 的内核应用管理。注意的是，Android 的 Linux kernel 不是 GNU 的 Linux。Android 将驱动程序移动 userspace ，使得 Linux Driver 与 Linux kernel 分开。

#### Android studio 的安装教程
略