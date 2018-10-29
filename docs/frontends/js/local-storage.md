

# 如何给localStorage设置一个有效期？

![本文由@IT·平头哥联盟-首席填坑官∙苏南 分享，公众号：honeyBadger8](../_banner/banner17.png)

> 作者：[首席填坑官∙苏南](https://github.com/meibin08/ "首席填坑官∙苏南")<br/>
> 公众号：`honeyBadger8`，群：912594095，本文原创，著作权归作者所有，转载请注明原链接及出处。

## 引言

​　　这个话题其实在上次分享[<小程序填坑记里讲过了>](https://blog.csdn.net/weixin_43254766/article/details/82811714 "做完小程序项目、老板给我加了5k薪资～")已经讲过，但后来群里/评论都有些同学，提到了一些疑问，问能否单独整理一篇更为详细的分享，讲解一下细节和完善提到的不足，如是有了下文👇。

## 思考点
　　从我们接触前端起，第一个熟悉的存储相关的Cookie或者来分析我们生活中密切相关的淘宝、物流、闹钟等事物来说起吧，
+ Cookie从你设置的时候，就会给个时间，不设置默认会话结束就过期；
+ 淘宝购物 从你下单付款起，就会给这件货物设置一个收货期限时间，过了这个时间自动认为你收货（即`订单结束`）；
+ 闹钟 你设置的提醒时间，其实也就是它的过期时间；
+ 再比如与您每天切身相关的产品需求，过完需求，你给出的上线时间，也就是这个需求的过期时间；
+ 再通俗点讲，您今年的生日过完到明年生日之间也是相当于设置了有效期时间；

!> 以上种种，我们能得出一个结论任何一件事、一个行为动作，都有一个时间、一个节点，甚至我们可以黑`localStorage`，就是一个完善的API，为什么不能给一个设置过期的机制，因为`sessionStorage`、`Cookie`并不能满足我们实际的需求。

## 实现思路

　　抱歉，黑`localStorage`不完善，有点夸张了，综合上述的总结，问题就简单了，给`localStorage`一个过期时间，一切就都so easy ？到底是不是，来看看具体的实现吧：

#### 简单回顾

　　



![宝剑锋从磨砺出，梅花香自苦寒来，做有温度的攻城狮!，公众号：honeyBadger8](../_banner/card.gif)

> 作者：苏南 - [首席填坑官](https://github.com/meibin08/ "@IT·平头哥联盟-首席填坑官")
>
> 链接：https://honeybadger8.github.io/blog/
> 
> 交流群：912594095[`资源获取/交流群`]、公众号：`honeyBadger8`
>
> 本文原创，著作权归作者所有。商业转载请联系`@IT·平头哥联盟`获得授权，非商业转载请注明原链接及出处。 




