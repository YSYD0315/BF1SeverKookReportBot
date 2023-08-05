## 基于BF1ClientAPI的kook服管机器人

> 写在最前面，由于该机器现在还处于基础开发阶段，所以很多配置项还是写死在代码里，如果你需要使用可能需要自行修改源代码，同样也可能会有很多bug。欢迎加入[ddf kook](https://kook.top/A17StS)体验功能
>
 如果你想要自己部署，首先需要注册kook开发者中心，获取机器人应用token如下形式：

```
1/MjAwMzg=/aF749t46Xb1x4e/hFcWjpQ==  #这个token填入在core/bot.py文件中
```

 设置默认服管账号命令为

 ```
 在utils/bf1/default_account.json里配置pid，remid，sid即可
 ```

 另外你需要更改

 ```
modules/self_contained/bf1_import/__init__.py中的一些clid#频道id修改为你的kook服务器的频道id可通过kook开发者模式复制
 ```

 在根目录通过python run.py 运行主程序，报错缺什么你就装什么就行了。

 ```
 khl.py                       0.3.6 #这是kook bot 的python sdk
 ```

## TODO

 - [x] 服务器信息公屏播报（kd，rank，新的击杀王已诞生(等等）
 - [x] 公屏投票换图
 - [x] 公屏信息播报到kook频道
 - [x] 服务器信息输出到kook频道
 - [ ] 公屏投票踢人
 - [ ] 呼叫管理员
 - [ ] 禁用武器

 ## 致谢和其他

 这个项目大量抄袭(复用)了一个基于 [khl.py](https://github.com/TWT233/khl.py)的[xiaomai-bot: 战地1寄气人 (github.com)](https://github.com/g1331/xiaomai-bot)的kook移植版的代码，感谢[CrazyZhang666](https://github.com/CrazyZhang666/)大佬开源的BF1客户端API项目使kook机器人实时管理服务器成为了可能，msk大佬开放的bf1免origin版和bf1启动参数使登录更加便利和挂机占用更低。

 另外代码很屎山，欢迎各位大佬提出修改意见！
