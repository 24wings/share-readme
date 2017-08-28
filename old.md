# 狠享赚 平台构建进度

![](./images/fensi.jpg)
狠享赚是一套大型微信广告分销系统
# 微信端 用户入口

**扫描二维码进入应用**
![](images/qrcode.jpg);
应用首页 广告分类以及列表
![](./images/share1.jpg)
个人中心 
![](./images/share2.jpg)
收益日志
![](./images/share3.jpg)
提现记录
![](./images/share4.png)
我要收徒
![](./images/share5.jpg)
二维码收徒
![](./images/share8.jpg)
完善信息
![](./images/share7.jpg)
广告主 首页
![](./images/share6.png)
广告主 用户指南
![](./images/share9.jpg)
广告主 用户指南2
![](./images/share10.jpg)
任务详情页 通过Iframe 加载可以指定推广链接
![](./images/share11.jpg)

广告主发布任务
![](./images/advert-publishTask.png)
![](./images/advert-publishTask2.png)




技术架构 前端angular2  后端 Nodejs+koa+typescript+mongoose
* [x] 用户授权登陆 (比享客威盟更加方便,无需注册直接成为会员)
* [x] 用户授权成为徒弟  (比享客威盟更加方便推广,无需注册直接成为徒弟)
* [x] 用户点击广告后直接返利 [一切都只在一次点击中,所有过程都会完成]
* [x] ~~广告主发布任务~~
* [x] ~~广告主查看激活任务~~
* [x] ~~广告主查看所有任务~~
* [x] 三级分销 师徒关系 
    * [x]  A方案 该三级关系返利**已弃用**
        * [x] ~~单人 A 100%~~,
        * [x] ~~双人A 师傅B徒弟,B点击： A 5% B 95%~~
        * [x] ~~三人ABC C是B徒弟,B是A徒弟 C点击: A 5% B 10% C 85%~~
        * [x] ~~四人ABCD D是C徒弟,C是B徒弟,B是A徒弟 D点击: D 70% C 15% B 10%  A 5%~~
    * [x]  B方案 该三级关系返利**正在使用**
        * [x] 单人 A  0%
        * [x] 双人  B是A徒弟  B点击 B 0% A 100%~~
        * [x] 三人 C是B徒弟 B是A徒弟 C是B徒弟 C点击 C 0% B 95% A 5%
        * [x] ~~四人 D是C徒弟 C是B徒弟  B是A徒弟 D点击  D 0%
        * [x] C 85% B 10% A 5%
* [x] 广告栏目分类加载,下拉刷新加载广告
* [x] 高性能页面切换,页面切换动画
* [x] 视频时间轴分享后才能观看
* [x] 广告图片压缩上传
* [x]  页面加载动画
* [x] 用户的基础信息
* [x]  微信立即提现
    * [x] 提现限制,每天最多两次
    * [x] 提现拦截,没有完善信息的用户无法提现
* [x] ~~点击广告返利给师傅~~ 通过分享的广告才能返利给师傅,阅读广告不能获利
* [x] 微信支付,发布任务
* [x] 分享收徒二维码,可以直接收徒
* [x] 调用jssdk进行图文标题,分享朋友圈,分享给朋友
* [x] base64压缩任务图片上传
* [x] 视频监听分享朋友圈或朋友后才能观看,自定义停止时间轴
* [x] gzip 压缩文件,提升页面加载速度 
* [x] ~~下拉刷新熊动态图~~
* [x] ~~任务详情下的小标题进入公众号~~
* [x] 任务详情下进入一篇指定推广文章





> 技术架构优势,使用angular2在后续的开发工作中更有便捷性和可维护性,nodejs+koa 作为后台省略掉了session,cookie这些中间件和模板渲染的方式能让应用的性能获得极大的提升,总而言之,这一套应用的架构无论是性能还是功能都大大的超过了享客威盟
有钱都买不到的超高性能web应用速度
而从功能上讲,我们应用核心具备了三级分销系统,在用户点击广告的过程中,直接授权成为下级徒弟,并且完成了广告的传播计费方式,而且有了余额,而无需登录注册,一切只在于一次点击一次分享,所有的分享传播过程浑然天成.集成了功能与性能之美的一套系统。

# 广告商端 angualr2+material 
原有的广告商版本经过改写

旧版广告商登录界面
![](./images/old-advert-0.png)

旧版广告商首页
![](./images/old-advert-1.png)

旧版 广告商发布任务
![](./images/old-advert-2.png)

旧版  广告商发布任务第二栏
![](./images/old-advert-3.png)

旧版 广告商数据分析以及报表
![](./images/old-advert-4.png)


后插件过多,模板渲染方式性能页面加载慢,进行改写,由material+angular2布局

功能列表
* [x] 手机号登录
* [x] 手机验证码注册
* [x] 发布广告任务,base64压缩任务图片,banner图片不压缩
* [x] 修改任务
* 管理任务页面,在余额大于20% 可以暂停任务,余额小于20%任务下架
* [x] 任务的一天,一周,一月 报表
* [x] 完善用户信息
* []  对公账户转账


线上地址:狠享赚广告商 入口 [http://wq8.youqulexiang.com/login](http://wq8.youqulexiang.com/login)

新版 广告商首页
![](images/new-advert-login.png)
新版 广告商注册页面
![](images/new-advert-register.png)
新版 广告商首页
![](images/new-advert.png)
新版 广告商 发布任务 第一步
![](images/new-advert-1.png)
新版  广告商  发布任务第二步
![](images/new-advert-3.png)
新版 广告商  发布任务第三步
![](images/new-advert-4.png)
新版 广告商 
![](images/new-advert-5.png)
新版 广告商身份中心
![](images/new-advert-6.png)
新版  个人中心和资质认证
![](images/new-advert-7.png)
新版  完善信息
![](images/new-advert-8.png)
新版 对公账户
![](images/new-advert-9.png)




# 系统管理后台
原有的系统后台管理加载过慢,现在重写已经性能和加载更快
![](./images/admin.png)



线上版本 [http://wq8.youqulexiang.com/admin/login](http://wq8.youqulexiang.com/admin/login)
 需要登录请联系 
* QQ: 2121718893   
* Email: 2121718893@qq.com
* 电话: 13419597065
* 

新版管理后台 登录界面
![](./images/new-admin-10.png)
新版管理后台  用户管理 三级关系树和收益日志
![](./images/new-admin.png)
新版管理后台  用户管理   关闭侧边栏
![](./images/new-admin-2.png)
新版管理后台  广告分享栏目管理以及 广告管理
![](./images/new-admin-3.png)
新版管理后台  广告分享 查看子栏目,关闭侧边栏
![](./images/new-admin-4.png)
新版管理后台  添加广告栏目
![](./images/new-admin-5.png)
新版管理后台    广告轮播管理
![](./images/new-admin-8.png)
新版管理后台 系统用户分析
![](./images/new-admin-9.png)




# 广告任务的编写

![](./images/advert.png)
* [x] 微信推广视频页面
* [x] 官网的编写
* [x] 应用的UI重写改版



汇总:
在一个月的过程中,整个技术部牺牲了大量的个人生活的时间,大量的精力,完成了平台的1.0构建(依然有不足之处),这是十几个人团队的事情,然而我们接到手上时,没有推脱,没有拒绝,凭着克服万难的信念一步步将平台构建完成,牺牲了许多本该休闲娱乐的时间,可以说没有技术部的努力,这个平台就不会存在。
在修改完了应用的瑕疵和Bug后,我们将继续展望2.0版本,为三级分销和广告系统增加更多功能和活力。例如社交系统和推广系统，定位广告等,让广告商能够直接借助微信平台与推广用户和普通用户进行沟通聊天推广商品等,例如更多推广方式,添加入广告发布模板中,如关注公众号,拨打手机,调用jssdk等地理定位.





后记:
三级分销系统+广告系统 是我们的技术架构.然而我们不仅仅局限于此,我们的系统是灵活的,可以是三级分销+电商,三级分销+医疗美容,三级分销+美食推广等等,期待有意向的人与我们进行商业合作.


技术架构

|平台|技术|原因|
|-|-|-|
|后台|Nodejs+Typescript+Koa+Mongoose|koa比express更加强健,性能更高,移除了大部分不必要的中间件,保留了Rest 风格构建的基本要素,mongoose配合typescript进行了orm的实体层泛型映射|
|狠享赚前端应用|Angular2+Typescript |构建一个强类型的应用系统,便于开发维护,单页面应用程序性能快,配合后台性能10ms之内返回数据,50ms之内完成页面切换加载,高性能动画|
|[狠享赚广告商后台](http://wq8.youqulexiang.com/login)|Angular2+Typescript |构建一个强类型的应用系统,便于开发维护,单页面应用程序性能快,配合后台性能10ms之内返回数据,50ms之内完成页面切换加载|
|[狠享赚管理后台](http://wq8.youqulexiang.com/admin/login) |Angular2+Typescript |构建一个强类型的应用系统,便于开发维护,单页面应用程序性能快,配合后台性能10ms之内返回数据,50ms之内完成页面切换加载|



[markdown 写作指南](http://www.cnblogs.com/rossoneri/p/4446440.html)






