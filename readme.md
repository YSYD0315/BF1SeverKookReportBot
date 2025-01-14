## 基于BF1ClientAPI的kook服管机器人

> 写在最前面，由于该机器现在还处于基础开发阶段，所以很多配置项还是写死在代码里，如果你需要使用可能需要自行修改源代码，同样也可能会有很多bug。欢迎加入[ddf kook](https://kook.top/A17StS)体验功能
如果你想要自己部署，首先需要注册kook开发者中心，获取机器人应用token。

1. 在config/config文件中配置token即可

2. 在utils/bf1/default_account.json里配置pid，remid，sid即可
3. 在config/config文件中配置服务器内信息转发频道，游戏报告输出频道，自动踢出通报频道，游戏内报告输出时间间隔，玩家列表变更通知列表

 在根目录通过python run.py 运行主程序，报错缺什么你就装什么就行了(python版本3.10以上)。

 ```
 khl.py                       0.3.6 #这是kook bot 的python sdk
 ```

## TODO

 - [x] 服务器信息公屏播报（kd，rank，新的击杀王已诞生(等等）
 - [x] 公屏信息播报到kook频道
 - [x] 服务器信息输出到kook频道
 - [x] 禁用武器
 - [x] 换边检测与新加入检测
 - [ ] 进程守护
 - [ ] 远程关闭
 - [ ] 公屏投票踢人
 - [ ] 呼叫管理员
 - [ ] 指令鉴权系统
 - [ ] 公屏投票换图

## 更新日志

> 慢慢挤牙膏

- 2023-08-05 禁用武器，配置写入配置文件，优化播报信息长度
- 2023-08-07：
  -  进程守护：崩溃自动重启bf1
  -  远程启动：通过指令远程开关bf1
  -  客户端api 1.40版本适配
  -  新增违规武器踢出通报到游戏公屏
  -  调整文件结构，添加若干代码注释
- 2023-08-11：
  - 对游戏客户端api进行封装，对原有代码进行重构
  - 暂时移除投票换图，进程守护等功能等待下个版本的开发
  - 对转发服务器消息进行了过滤，不再转发服务器内机器人自身播报的信息
  - 将配置集中到config中
  - 换边检测和新加入玩家，退出玩家检测



 ## 致谢和其他

 这个项目大量抄袭(复用)了一个基于 [khl.py](https://github.com/TWT233/khl.py)的[xiaomai-bot: 战地1寄气人 (github.com)](https://github.com/g1331/xiaomai-bot)的kook移植版的代码，感谢[CrazyZhang666](https://github.com/CrazyZhang666/)大佬开源的BF1客户端API项目使kook机器人实时管理服务器成为了可能，msk大佬开放的bf1免origin版和bf1启动参数使登录更加便利和挂机占用更低。

 另外代码很屎山，欢迎各位大佬提出修改意见！

