# dove

这是我正在写的即时通讯app，界面都是照着微信画的，加上了微博的话题功能。
界面展示在/assets/show

## 日志

2019-10-07：前端的整体框架和四大页面总算是做好了

2019-10-09：注册界面上传头像不是很完美，也不知道微信那个图是哪来的，我自己截的话感觉也不太好，先拿icon顶一顶吧，也没有裁剪图片的功能，得上传正方形图片才能刚好，还没在前端验证输入合法性，正在愁dart怎么和后端交互，dart完全没学过，完全是一边写一边百度，后端语言是用C++还是go也没想好呢...

2019-10-10：今天成功的让前端和dart和后端的go成功交互了，注册页面已经能够把注册信息序列化并发给后端了，但是怎么回复前端怎么接收回复还不知道怎么处理，明天再看看网上dart和java通信的博客研究研究，再有就是注册页面的TextField只有回车之后才能显示格式错误的错误信息，如果不结束输入的话，错误信息显示不出来而且注册按钮也没法按下去，而且还没有判断如果输入空格或者邮箱格式错误啥的都没整呢...我好难啊，想系统的学一下dart语言，却发现b站上只有那么点最最最基础的东西...

2019-10-15：dart怎么接收go的回复信息...可愁死我了

2019-10-16：前端能发消息给后端，后端能回复，前端也能接收了，但是现在不知道app每次启动时怎么判断登录状态，尝试在initstate申请后台判断，结果失败了...想在本地判断，结果不知道文件外怎么访问组件里的变量...

2019-11-06：时隔数周，期间学了学redis和mysql，终于又回来了，登录状态是用shared_preferences库写的，加了个loading页，我貌似发现为啥这些app都要有个启动页了，23333，进了启动页去判断本地有没有登录标记，再分别调转到登录页和主页

2019-11-07：今天聊天界面基本知道怎么搞了，就是对话框的样式还没写好，还有就是知道了textcontroller这个东西，提交之后可以把输入框的内容清空

2019-11-08：今天把聊天界面写完了，自己可以往出发消息，但是因为没写后端，所以对面发来的消息还没写，但是基本都差不多，然后联系人的详情页面也写完了，就是微信有个发消息的图形文字，我没找到，感觉那就是个文本，不是图标，先这样吧，也挺好的

2019-11-10：有了之前的积累，今天很快就把“我的”页面的设置完成了，并把退出功能也写到了设置里，然后这个项目就定名为“鸽子”了，至此前端界面基本就画完了，不过还有一些不完美的地方，会陆续的进行更改，接下来的任务就是设计数据库，把所有的功能都好好的想一下，把数据模型也都建好，规范一下接口什么的

2019-12-10：配合后端把登陆注册写完了