
# 联系方式
- 手机：13260560512
- Email：suxiaoweiwork@163.com





# 个人信息

 - 苏晓伟/男/1995 
 - 本科/湖北工业大学
 - 工作年限：2年
 - Github：https://github.com/ArmstrongGit

 - 期望职位：Android开发
 - 期望薪资：税前月薪9k~12k
 - 期望城市：上海


# 工作经历
## 上海商哲信息技术有限公司 （ 2016年6月 ~ 2018年2月 ）

### 快卖家乐项目 
###### 项目描述：
   快卖家乐项目是供联合利华饮食策划地推使用的一款App，地推在SFA（生意网络）上建立批发商和饭店信息。根据KPI考核目标，生成拜访任务计划，地推根据计划拜访批发商、饭店、快用家乐用户，完成考核目标。

###### 技术要点：
- 整体采用ViewPager+Fragment来搭建主体页面
- Fragment懒加载，Activity可见时加载
- 使用XRecyclerView，上拉加载更多，配合后台数据实现分页加载数据
- 封装MultipleStatusView封装了加载中、加载失败、空内容、加载错误视图，根据不同的状态展现对应的页面
- 通过zxing实现二维码的扫描识别来完成绑定功能
- 使用第三方PDF阅读来实现PDF文件的阅读
- 通过Bitmap.CompressFormat对照片的尺寸及质量压缩提高照片上传的效率同时保证照片的阅读质量
- 封装UploadUpdateManager来对App进行应用的升级提示及下载安装
###### 踩坑与填坑：
- 6.0运行时权限的适配
- 7.0apk下载的正确方式，通过provider来对7.0机型进行适配
- apk安装时intent添加install.FLAG_ACTIVITY_NEW_TASK 才会出现打开和完成页面
- 三星5.0以上6.0以下拍照适配，三星手机拍照后会自动旋转actvity，若对照片的路径没有存储会发生闪退的现象，需要在AndroidManifest中配置configChanges或者在生命周期中保存
- 部分国产ROM禁用了DownManager如要使用需要对其是否禁用进行判断


### toppingCoffee店长端项目

###### 项目描述：
   toppingCoffee店长端是供咖啡店店长使用的App，店长可使用其中一款App在商米V1或者具备打单功能的机器上使用，可以实现收银结账，打印小票，使用第二款App可以接收订单推送。
     
   ###### 技术要点：
- 头部采用AppBarLayout+CollapsingToolbarLayout+Toolbar来实现头部的特效
- 使用behavior来实现列表与头部的联动效果
- 采用开源框架Picasso来实现三级缓存技术缓存图片，提高程序的响应速度和流畅性
- 采用第三方FlowLayout来实现商品属性的选择
- 使用阿里推送来处理支付成功后的页面刷新
- 使用sunmiSDK操作打印机按照打印格式进行打印

     
### 叮咚伴学项目
###### 项目描述：
   叮咚伴学APP是为浙江叮咚网络有限公司为教育培训机构专门开发的CRM管理系统，并搭配叮咚伴学在线售课平台及Web管理端口。它是教育机构必备神器，学员、教务、售课三位一体，管控教育消费全生命周期，线上线下协同管理，为教育机构输出最优业务服务。

   ###### 技术要点：
- DrawerLayout+NavigationView实现左边菜单侧滑，通过监DrawerListener来实现自定义侧滑动画
- 重写onCreateOptionsMenu来修改toolbar，实现带搜索栏的状态栏
- 通过开源SegmentTabLayout来实现多个fragment视图的切换
- 通过ViewFlipper封装可左右滑动的日历，实现课表的日期的选择
- 自定义SwipeMenuLayout实现课表又滑菜单功能
- 自定义布局配合是适配器实现时间轴效果
   ###### 踩坑与填坑：
- 有转场动画的布局需要对应版本建立对应的布局
- Style中windowIsTranslucent属性设置为true，Activity滑动关闭时背景才不会是黑色

### Github项目介绍
   Github上的项目是个人开发过程中经验的总结，以及观看书籍及学习视频观看源码时总结的一些经验和代码，还有自己的一些探索。
   ###### 项目内容：
- 项目架构的三层，app+baselibrary+framelibrary  。app层主要是项目的具体代码与逻辑，baselibrary是基础层。
- baselibrary--基类BaseActivity对activity的代码进行了规范setContentView()、initTitle()、initView()、initData()；
- baselibrary--BaseTranslucentActivity是对沉浸式状态栏的一个封装，最小支持到4.4版本，[4.4,5.0)的状态栏用透明状态栏，适配了虚拟导航栏
- baselibrary--封装了注解Annotation:CheckNet、OnClick、ViewById
- baselibrary--封装AlertDialog采用Builder的设计模式
- framelibrary是项目层，项目常用的一些封装类在这里
- framelibrary--SelectImageActivity，图片选择框架的一个封装，选择模式有：单选、多选（可自定义张数，默认9张），是否有相机按钮。
-  framelibrary--图片选择完毕之后会用ImageUtils进行图片的大小及质量压缩，再采用NDK jpegturbo进行压缩
-  framelibrary--封装DaoSupportFactory运用工厂设计模式，通过反射的形式把bean对象直接转化为db表格，调用方式：创建表格：IDaoSupport<Person> daoSupport= 新增数据：DaoSupportFactory.getFactory().getDao(Person.class);
  daoSupport.insert(persons);
-   混合开发探索：前端界面采用H5的方式实现界面的呈现，可以引入MUI框架来快速的实现App上的一些效果，比如下拉刷新上拉加载、列表侧滑等等，中间通过封装的JsOperation来进行数据的传递后端采用OKHTTP来实现与后台数据的交互。
-   Material Design 控件的探索
-  Material Design 动画的探索
- NDK-增量更新
- 自定义全局异常捕获类，捕获异常存储日志，上传后台，自定义fixbug热修复
- 封装JsonCallback对后台返回的json数据进行解析，通过不同的状态码对应处理
- 封装DialogCallback统一的带等待窗口的处理类，继承自JsonCallback

      
# 技能清单

以下均为我熟练使用的技能

- 熟悉Java语言开发，理解面向对象的设计模式，良好的设计文档撰写能力；
- 熟悉Android下的XML、JSON、HTML的解析；
- 熟悉各种UI控件、动画和布局，有自定义UI控件开发能力；
- 根据业务变化、不断改善升级产品, 保证系统的性能、稳定性及可靠性；
- 熟悉C语言，有一定的NDK开发基础
- 有App Market线上产品
- 熟悉java后端开发

      
---      
# 致谢
感谢您花时间阅读我的简历，期待能有机会和您共事。
      

    
