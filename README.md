# wanandroid-kotlin
# RxLife


# ViewModel
 ``` kotlin
     //在同一个Fragment或者Activity中,多次获取的ViewModel都是同一个对象
     val viewModel = ViewModelProviders.of(this).get(MainViewModel::class.java)
```
```kotlin
    //Subclasses must have a constructor which accepts {@link Application} as the only parameter.
    class SubAndroidViewModel constructor(application : Application) : AndroidViewModel(application) {
        //只能使用Application对象作为唯一的参数,Application的子类都不行
    }
```
从数据源中(本地或者网络)获取到数据反馈给ui层,


# git
## 分支
```
查看分支：git branch

创建分支：git branch <name>

切换分支：git checkout <name>

创建+切换分支：git checkout -b <name>

合并某分支到当前分支：git merge <name>

删除分支：git branch -d <name>
```


# dagger2
[参考博客](https://www.jianshu.com/p/cd2c1c9f68d4)

# RxJava2
一切数据都是流,just,error,empty等创建型操作符都是为了向下继续发送数据流,确保下游观测者可以接收到信息(包含异常信息)
ObserVableTransformer处理的全局异常信息,依旧需要在Observer中做接收

# Room数据库
添加依赖
```
def room_version = "2.1.0-alpha02"
    implementation "androidx.room:room-runtime:$room_version"
    kapt "androidx.room:room-compiler:$room_version" // use kapt for Kotlin
    // optional - RxJava support for Room
    implementation "androidx.room:room-rxjava2:$room_version"
```
参考博客: https://www.cnblogs.com/littlepanpc/p/9269549.html


# databinding
 1. 绑定adapter
 2. 
 
# RecyclerView
    1. 优化
    2. 瀑布流
    3. 多itemType布局
    4. 动画
    5 .滚动和快速滑动
    6. SnapHelper
    7. LayoutManager
    8. 如何复用view
    9. position
       getAdapterPosition 和 getLayoutPosition
       
    
# 多状态布局
    

# material design

## CollapsingToolbarLayout
 折叠的FrameLayout,用作AppBarLayout的直接子View
## CoordinatorLayout

## AppBarLayout

## ToolBar

## 反射
 如果通过类名生成对应的类

## DrawerLayout
 参考官方文档:https://developer.android.google.cn/training/implementing-navigation/nav-drawer
 
 
# Fragment
屏幕旋转时,Activity/Fragment生命周期怎么变化?
    经历了完整的生命周期变化,通过onSaveInstanceState保存的数据可以在onRestoreInstanceState中取出
    数据加载的操作还会再走一次,ViewModel恢复数据似乎并没啥用
对于Activity:
    -------onCreate
    -------onStart
    -------onResume
    -------onPause
    -------onSaveInstanceState
    -------onStop
    -------onDestroy
    -------onCreate
    -------onStart
    -------onRestoreInstanceState,我是保存的状态
    -------onResume
 
# 参考项目
https://github.com/git-xuhao/KotlinMvp
https://github.com/MindorksOpenSource/android-mvvm-architecture
https://github.com/iammert/AndroidArchitecture
https://github.com/jenly1314/WanAndroid
https://github.com/jshvarts/OfflineSampleApp
https://github.com/KunMinX/android-viabus-architecture
[直播间送礼物控件](https://github.com/jenly1314/GiftSurfaceView)
https://github.com/pedrovgs/EffectiveAndroidUI
https://github.com/sockeqwe/mosby
[阅读器](https://github.com/smuyyh/BookReader)
https://github.com/chentao0707/SimplifyReader
https://github.com/uber/RIBs
https://github.com/ivacf/archi
https://github.com/TommyLemon/Android-ZBLibrary
https://github.com/codeestX/GeekNews
https://github.com/Bilibili/boxing
https://github.com/GitLqr/LQRWeChat
https://github.com/esoxjem/MovieGuide
https://github.com/jaydenxiao2016/AndroidFire
[仿微信朋友圈](https://github.com/Naoki2015/CircleDemo)
https://github.com/BaronZ88/MinimalistWeather
https://github.com/rallat/EffectiveAndroid
https://github.com/iMeiji/Toutiao
[咕咚翻译](https://github.com/maoruibin/TranslateApp)
[全民直播](https://github.com/jenly1314/KingTV)
[ColorfulNews](https://github.com/kaku2015/ColorfulNews)
https://github.com/UCodeUStory/S-MVP
[仿京东商城](https://github.com/liu-xiao-dong/JD-Test)
https://github.com/woxingxiao/GracefulMovies
[EasyReader](https://github.com/laotan7237/EasyReader)
[虎扑体育](https://github.com/gzsll/TLint)
https://github.com/liuyanggithub/SuperMvp
//以这个为参考
[wanandroid](https://github.com/songmao123/WanAndroid)


[googlesamples-sunflower](https://github.com/googlesamples/android-sunflower)








# 心得
1. 架构能力
2. 做几款不同类型的App
3. 主流开源框架深入原理
4. android基础要点深刻掌握原理
5. 学习能力和解决问题的能力
