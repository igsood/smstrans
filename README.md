# smstrans1.0 (短信转发APP For Android)
## 需求与背景
- 最近新入手了一张**腾讯大王卡**，腾讯系APP免流量这一优惠实在是太有诱惑力了。经过一番苦苦挣扎，旧手机卡也只好**退位让贤**了。但是，总有美中不足。新手机卡虽然年轻有流量，但旧手机卡资格老哇，各种app、各种网站每次登录时总免不了默念旧手机号几遍，时不时的还要收几个登录验证码。
- 所以，索性对新旧号码来个大分工。上网的事情归新卡腾讯大王卡负责，管理各种账户的事情归旧手机卡负责，能这样倒是很省心、很方便。并且用新卡腾讯大王卡跟生人联系，也就不那么容易就暴露微信、支付宝号之类的，***总之你开心就好***。
- 可惜掏出手机来就傻眼了。只！能！插！一！个！卡！:() 习惯了带一个手机出门，就要带两个手机了？绝对的麻烦（摇头中……）。
- 是要想个办法了。first choice!换个双卡的手机：坚果Pro、金立S10、华为P10、小米6变焦双摄拍人更美……o_Oo_Oo_O跑题啦——就这样被你带跑。不就是入手了一张**腾讯大王卡**么，怎么扯到买手机上去了？什么鬼
- 其实问题也简单啦，不就是一个验证码么，旧手机卡收到短信直接转发给新大王卡就行了。就这么愉快的决定了，问题解决了，好开森啊。好啦好啦，你你你~，还是个技术宅么~ 说你呢~ 别浪费时间往下看了，**请Ctrl+w离开此页面！**。
- 技术宅们keep going。***手机短信转发***。好吧，还是写个app吧，就For Android就够了。这个app只运行一个服务就行，用来监听手机的广播，只要监听到新短信就向另一个手机号上转发。顺便起个名，就叫smstrans吧。
## 功能与实现
- 短信监听服务，常驻内存用以监听短信通知
- 有新短信接收时，监听服务获取新短信内容并作处理（判断、过滤、拼接）
- 将处理后的短信以短信形式发给指定的手机号
- 授权权限：接收讯息、读取讯息、读取手机状态和身份、发送短信
- 注册广播机制获取新短信消息
- 将广播注册在系统中（在AndroidManifest.xml中注册）
## 程序修改履历
1. 2017-07-25 v0.1 创建
2. 2017-07-27 v0.2 添加特定短信转发过滤、转发格式修改，解决长短信显示时不合并的问题
