# 可行性分析

通过一个基于 Minecraft Forge 的模组，来下载资源包，并在启动前就修改相关配置，从而在游戏启动后，自动装上。

## 1. 自动更新部分

能够在启动前下载最新版本资源包

- 资源包大小目前在 5M 以内，后续可能会增加体积，暂定为 6M；
- 下载应当不超过 10s，故下载速度应当在 600k/s 以上；
- 下载后能够修改原版 `option.txt` 文件，使最新版资源包优先级最高；
- 下载优先级要高一些，要在游戏读取 `option.txt` 之前就完成；

## 2. 游戏内反馈功能

能够让玩家在游戏内通过快捷键反馈相关错误，或者意见

- 支持 JEI，玩家鼠标指针指向的物品，摁下快捷键，可以打开反馈界面；
- 反馈界面会自动获取指向物品相关翻译信息；
- 玩家可以快捷通过选项来指出翻译错误类型；
- 远程服务器获取这些翻译错误；

## 3. 公告功能

能够让玩家在游戏内打开公告，公告获取指定动态服务器内容，发布相关更新消息，或者其他说明。

- 类似于 `MPUtils` 模组，不过公告加载是动态的；
