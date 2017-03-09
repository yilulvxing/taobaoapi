淘宝开放平台api

最近开发的项目要和淘宝进行对接，中间各种坑 就不...

淘宝很多开放的api都是要在阿里的聚石塔内完成调用的，所以购买聚石塔内的ecs和rds竟然是必须的
而且费用还...

好了言归正传，下面开始流程
1.仔细阅读淘宝的开发入门，后面坑不少
http://open.taobao.com/docs/doc.htm?spm=a219a.7629140.0.0.8fOFMG&treeId=1&articleId=103232&docType=1

2.购买ecs，rds；注意如果要用到redis服务的要单独购买因为淘宝开放的端口很少很少，这一点表示很...
另外rds也是必须购买的，不然很多接口申请通过不了

3.需要认证权限的接口，要单独获得淘宝的code值，参考如下
http://open.taobao.com/docs/doc.htm?spm=a219a.7629140.0.0.g0IIpq&treeId=49&articleId=102635&docType=1#s5

code值一天才会返回一个，然后根据code值获得access_token/sessionKey；
传入sessionKey才能获得要授权的接口；这个过程记得保存淘宝api返回的token的信息
不然在后续会非常的...

4.淘宝的开放平台的控制台会有一些版本的sdk下载，可以根据文档处理

5.api在线调试工具
http://open.taobao.com/apitools/apiTools.htm?spm=a219a.7395905.0.0.h7pZ5w&catId=5&apiId=46&apiName=taobao.trades.sold.get&scopeId=

PS，以上很多操作需要商家店铺的管理员账号操作
记录了一些简单的步骤，但是实际里面的坑会非常多。集成的接口没有上传，php版本
