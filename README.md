# ASSRouter
Android系统学习路线
https://jsonchao.github.io/  安卓系统学习路线

做过哪些性能优化？是怎么评测和具体优化的？

查看源码隐藏api  https://github.com/anggrayudi/android-hidden-api

一、App启动速度优化

 1, https://blog.csdn.net/CrazyMo_/article/details/80035314

 2,Permission Denial: starting Intent { cmp=com.xxx.xxx}解决办法修改com.xxx.xxx应用的manifest.xml文 .   件，找到YourActivity标签，添加android:exported="true"一句即可，该句意思为该activity可以被其他应用访问

3，关于Callable 的使用：https://blog.csdn.net/codershamo/article/details/51901057 

4，解决黑白屏 https://blog.csdn.net/jie_0754/article/details/83024695 

5，app的启动流程 https://blog.csdn.net/CrazyMo_/article/details/79949334

6，ActivityThread 是什么 https://www.jianshu.com/p/d8972b4188df

二、App绘制优化
1，布局渲染  https://blog.csdn.net/CrazyMo_/article/details/80038948
2，新知识 用LinearLayout自带的分割线 https://www.jianshu.com/p/1987d6d4cf8b
3，布局绘制优化 https://blog.csdn.net/CrazyMo_/article/details/80149093
三、App内存优化
1，ava内存管理模型、内存分配、内存回收的机制 https://blog.csdn.net/CrazyMo_/article/details/80210657
2，内存泄漏分析和解决办法  https://blog.csdn.net/CrazyMo_/article/details/80214205
四、App瘦身
1，apk瘦身 https://juejin.im/post/59113583ac502e450280e5f3
五、App电量优化
1，https://juejin.im/post/5c6b97ea6fb9a049cd54c3d4  安装battery historian的两种方式：
使用docker安装，docker -- run -p :9999 gcr.io/android-battery-historian/stable:3.0 --port 9999
使用源码安装（比较麻烦，依次需要使用go环境 git环境 python环境 java环境 ）https://github.com/google/battery-historian
2,电量分析步骤 ：https://www.jianshu.com/p/a704e2268fe6 
3，你在哪个目录下执行adb bugreport bugreport.zip 就会在哪个目录下生成 bugreport.zip文件
4，解压 unzip bugreport.zip -d bug
5，执行分析命令  java -jar /Users/apple/Downloads/所有软件/chkbugreport.jar  /Users/apple/Downloads/所有软件/bugreport-walleye-PPR1.180610.009-2019-08-04-17-10-41.txt
六、网络优化
1，https://www.zhihu.com/question/29466887
2，安卓官方性能优化指导 http://hukai.me/android-training-course-in-chinese/connectivity/efficient-downloads/index.html
七、安卓的安全优化
1,webview的安全漏洞 https://blog.csdn.net/carson_ho/article/details/64904635
2，Android应用安全分析 https://blog.csdn.net/jiangwei0910410003/article/details/80375831

八，其他
2、为什么WebView加载会慢呢？
加载缓慢的原因和解决方案 ：https://blog.csdn.net/square_l/article/details/17681885
3、如何优化自定义View
优化思路 ：https://blog.csdn.net/WHB20081815/article/details/74474736
4、FC(Force Close)什么时候会出现？
引起fc的原因 以及和anr的区别：https://blog.csdn.net/hejianhua1/article/details/79813182
5、Java多线程引发的性能问题，怎么解决？
https://www.jianshu.com/p/e70f240a46f6
Android Framework相关

1、Android系统架构
https://hit-alibaba.github.io/interview/Android/basic/Android-Arch.html
2、View的事件分发机制？滑动冲突怎么解决？
https://juejin.im/post/5ac2d495f265da237e09e6d1
3、View的绘制流程？
Android view 绘制流程：https://jsonchao.github.io/2018/10/28/Android%20View%E7%9A%84%E7%BB%98%E5%88%B6%E6%B5%81%E7%A8%8B/
android开发者知识体系：https://github.com/JsonChao/Awesome-Android-Notebook
4、跨进程通信。
a，跨进程通讯 Mesager  https://blog.csdn.net/itachi85/article/details/50448409
b，使用aidl的方式  https://blog.csdn.net/itachi85/article/details/50451908
c,如何开启多进程 https://blog.csdn.net/itachi85/article/details/50386748
d，几种跨进程通讯的方式 https://blog.csdn.net/u011240877/article/details/72863432
5、Android系统启动流程是什么？（提示：init进程 -> Zygote进程 –> SystemServer进程 –> 各种系统服务 –> 应用进程）
https://juejin.im/post/5b7e72bbe51d453894001ef0
6、启动一个程序，可以主界面点击图标进入，也可以从一个程序中 跳转过去，二者有什么区别？
Android 面试100题目 ：https://juejin.im/post/58a6c38861ff4b0062ae4c25#heading-25
7、AMS家族重要术语解释。activity manager service
http://winnerliu.me/2018/06/08/%E6%B7%B1%E5%85%A5%E7%90%86%E8%A7%A3AMS-ActivityManagerService/
8、App启动流程（Activity的冷启动流程）。
https://blankj.com/2018/09/29/the-process-of-app-start/
9、ActivityThread工作原理。
https://blankj.com/2018/09/29/the-process-of-app-start/
https://www.jianshu.com/p/b6ac0c2fa240
10、说下四大组件的启动过程，四大组件的启动与销毁的方式。
同第9点
11、AMS是如何管理Activity的？
同第9点
12、理解Window和WindowManager。
https://blog.csdn.net/u012124438/article/details/77347732
13、WMS是如何管理Window的？
同第12点
14、大体说清一个应用程序安装到手机上时发生了什么？
https://blog.csdn.net/github_37130188/article/details/89577635

三、Android优秀三方库源码

1、你项目中用到哪些开源库？说说其实现原理？
一、网络底层框架：OkHttp实现原理 责任链模式  builder模式 工厂模式 维护着三个ArrayDeque  分同步和异步方法 
      https://www.jianshu.com/p/7b29b89cd7b5
      https://www.2cto.com/kf/201608/532612.html?munghe=okdr13
有关双端队列 ArrayDeque的文章  http://blog.jrwang.me/2016/java-collections-deque-arraydeque/
二、网络封装框架：Retrofit实现原理
1， 讲的比较含糊的okhttp 文章     https://zhuanlan.zhihu.com/p/35121326
2，retrofit+okHttp+mvp+rxJava2+Dragger2 的项目 https://github.com/chengzichen/Flyabbit
3，设计模式基础 http://www.runoob.com/design-pattern/facade-pattern.html
4，讲的比较好的retrofit的原理 https://juejin.im/entry/59ad567df265da24777a161d
5，动态代理 https://www.runoob.com/design-pattern/proxy-pattern.html
三、响应式编程框架：RxJava实现原理
1，rxjava 原理  https://blog.csdn.net/TellH/article/details/71534704
2，讲的更清楚  https://juejin.im/post/5b1fbd796fb9a01e8c5fd847
3，自己实现的rxjava demo  https://github.com/TellH/RxJavaDemo/tree/master/src/my_rxjava
4，rxjava的原理 https://juejin.im/post/5b1fbd796fb9a01e8c5fd847#heading-6
5，扔物线文章 http://gank.io/post/560e15be2dca930e00da1083
四、图片加载框架：Glide实现原理
1，Android主流第三方库分析  
  glide 4.8源码的分析：https://jsonchao.github.io/categories/%E5%AE%89%E5%8D%93%E4%B8%BB%E6%B5%81%E4%B8%89%E6%96%B9%E5%BA%93%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90/
2，学到的新单词 retriever 猎犬
3,glide 3.7 的源码分析篇 https://zhuanlan.zhihu.com/p/24738598和 使用篇 https://www.jianshu.com/p/cea08d72ad4c
五、事件总线框架：EventBus实现原理
1，https://juejin.im/post/5ae2e6dcf265da0b9d77f28e#heading-5
2，粘性广播  http://www.voidcn.com/article/p-uuzkhqpg-bbs.html
3，eventbus编译处理 避免反射消耗
六、内存泄漏检测框架：LeakCanary实现原理
1，https://juejin.im/post/5ab8d3d46fb9a028ca52f813 
2，新单词 volatile  /välətl/
七、依赖注入框架：ButterKnife实现原理 （Java Annotation Processing（Java注解解析器））
1，@BindString(R.string.jump)的注解 没怎么使用到
2，unbind解绑实际使用有风险 网络请求没有及时关闭，数据请求成功，而view被销毁 了，报npe。
八、依赖全局管理框架：Dagger2实现原理
1，https://blog.csdn.net/u014639129/article/details/52543708
2，mvp模式实现presenter和activity的解耦 https://blog.csdn.net/wingichoy/article/details/51981756
3，dragger 2的使用  https://www.jianshu.com/p/b266314a97db
4，理解 dragger 2代码解耦  https://www.jianshu.com/p/b266314a97db 
5，apt 相关 https://blog.csdn.net/xx326664162/article/details/68490059
九、数据库框架：GreenDao实现原理

四、热修复、插件化、Gradle

1、热修复和插件化
2、模块化和组件化
3、gradle

五、设计模式与架构设计

1、设计模式
2、架构设计

六、其它高频面试题

1、保活方案
2、Android动画框架实现原理。
3、Activity-Window-View三者的差别？
4、低版本SDK如何实现高版本api？
5、说说你对Context的理解？
6、Android的生命周期和启动模式
7、ListView和RecyclerView系列
8、如何实现一个推送，消息推送原理？推送到达率的问题？
9、动态权限系列。
10、自定义View系列。
11、对谷歌新推出的Room架构。
12、没有给权限如何定位，特定机型定位失败，如何解决?
13、Debug跟Release的APK的区别？
14、android文件存储，各版本存储位置的权限控制的演进，外部存 储，内部存储
15、有什么提高编译速度的方法？
16、Scroller原理。
17、Hybrid系列。
18、如果在当前线程内使用Handler postdelayed 两个消息，一个 延迟5s，一个延迟10s，然后使当前线程sleep 5秒，以上消息的执行 时间会如何变化？
19、Android中进程内存的分配，能不能自己分配定额内存？20、下拉状态栏是不是影响activity的生命周期，如果在onStop的 时候做了网络请求，onResume的时候怎么恢复 21、Android长连接，怎么处理心跳机制。
20、下拉状态栏是不是影响activity的生命周期，如果在onStop的 时候做了网络请求，onResume的时候怎么恢复
21、Android长连接，怎么处理心跳机制
22、CrashHandler实现原理？
23、SurfaceView和View的最本质的区别？
24、Android程序运行时权限与文件系统权限
25、曲面屏的适配。
