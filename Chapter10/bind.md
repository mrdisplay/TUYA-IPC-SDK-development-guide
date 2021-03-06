# 设备的强绑定、弱绑定是什么？  

* 背景
有些对安全性要求比较高的设备，不能随意地把设备重置并配网。  
试想一下这种场景：  
你家院子里有个摄像头，你是用来监控家里的情况，设备就放在那，别人踮脚就能碰到，某天一个"坏人"，重置了你的设备，并配到自己的用户下面，他就能通过摄像头监控你家的情况，想想就吓人。  
强绑定就是解决这个问题，不让”坏人”随意绑定你的设备。  

* 绑定等级介绍  
这里所谓“绑定”是指“人”与“设备”之间的关系，“人”对于与其有绑定关系的“设备”，有操控权限。  
绑定级别是设备的一种属性。即强绑定是指这个设备是强绑定的设备，并不是指人是强绑定的人。   
我们把绑定级别分成三个等级，分别是，强绑定、中绑定、弱绑定。  

* 1.强绑定  

1.1.概念  

当前绑定用户必须先从app上解绑设备后，下一个人才能进行配网操作。  

好处是安全，坏处是操作麻烦，目前ipc和门锁的部分设备选择使用强绑定，为了安全性可以牺牲一些操作的简便性。  

1.2.那如果强行进行配网会怎么样？  

会在你配网的app上提示你，设备已经被别人绑定，你不能配网。

<img src="bind.assets/wps1.jpg" alt="img" style="zoom:30%;" />

1.3.如何解绑设备？  

a.正常操作是这个设备的当前绑定用户在app上移除设备。  

b.特殊情况下，比如测试设备，不知道被谁测试过，或者绑定的那个人联系不上了  

我们提供了在iot平台解绑教程  

* 2.中绑定  

2.1.概念  

级别比强绑定稍弱。前一个绑定用户不移除，后一个用户也可以配网，但是会给前一个用户发送push和消息中心，通知前一个用户。  

介于强绑定和弱绑定之间，只比弱绑定多一个通知。  

* 3.弱绑定  

3.1.概念  

最弱的绑定级别，也是占比最大的一类。设备可以随意被重置，随意被另一个用户绑定，不需要前一个用户同意，也不需要给前一个用户发送通知。  

 