LeakCanary

* Orm是内存泄漏检测工具，如android中bitmap处理容易导致OOM异常，我们可以用leakcanary来去测试监控。

* [配套视频](https://www.boxuegu.com/web/html/video.html?courseId=172&sectionId=8a9bdf305a3a4c00015a500b7aac01d2&chapterId=8a9bdf305a3a4c00015a500ba7db01d3&vId=8a9bdf305a3a4c00015a500bf5120263&videoId=C51690BA657EBB359C33DC5901307461)

* 爱生活,爱学习,更爱做代码的搬运工,分类查找更方便请下载黑马助手app


![黑马助手.png](http://upload-images.jianshu.io/upload_images/4037105-f777f1214328dcc4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

* 配置说明：

### 第一步：在module的build.gradle中添加依赖，包含debug与release
    	debugCompile 'com.squareup.leakcanary:leakcanary-android:1.3'
    	releaseCompile 'com.squareup.leakcanary:leakcanary-android-no-op:1.3'

### 第二步：定义MyApp类集成Application,在应用启动时初始化leakcanary观察对象refWatcher 

	refWatcher = LeakCanary.install(this);

### 第三步：在需要的页面调用refWatcher 开始观察。
 	 refWatcher.watch(this);

### 第四步：如果当前页面有内存泄漏问题，leakcanary会弹出notification提示并展示泄漏的错误信息详情。

* 详细的使用方法在DEMO里面都演示啦,如果你觉得这个库还不错,请赏我一颗star吧~~~

* 欢迎关注微信公众号

![](http://upload-images.jianshu.io/upload_images/4037105-8f737b5104dd0b5d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
