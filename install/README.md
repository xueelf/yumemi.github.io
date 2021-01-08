### 项目安装

本项目不用安装任何第三方软件依赖，非常简单轻便，仅需三行命令即可运行

> 首先 clone 项目仓库（在此之前你需要安装并掌握 [nodejs](https://nodejs.org) 的相关知识）

```
git clone https://gitee.com/Dc_Yuki/YumemiBot.git
```

> 使用 npm 安装 node 模块

```
npm install
```

### 目录结构

> 修改`config_example`目录名称为`config`，并正确添加`botSetting.yml`文件所对应的参数

```
YumemiBot
├─ yumemi                     bot 目录
│  ├─ config                  配置信息
│  │  ├─ boss.yml             会战信息
│  │  ├─ botSetting.yml       基本参数（QQ 号、群号等信息）
│  │  ├─ command.yml          正则匹配
│  │  └─ pluginParam.yml      插件参数（模块多参数配置文件）
│  ├─ data                    资源目录
│  │  ├─ db                   数据库文件
│  │  └─ images               图片资源
│  ├─ plugins                 插件目录（存放编写好的插件）
│  ├─ message.js              消息监听处理函数
│  ├─ plugins.js              模块自动加载函数
│  └─ tool.js                 自定义工具类函数
└─ app.js                     程序主入口（用于登录 QQ）
```

### 启动程序

> さあ、ゲームを始めよ

```
node app.js
```

如上述步骤无误  
bot 启动成功后会自动在`config`目录下生成`pluginSetting.yml`文件

> 当然，如果你有 js 的相关知识，随时都可以编写自己的插件，详情可在 [插件开发](develop/) 一栏查看

!> 在群内发送`ver`即可收到以下回复，所有模块 **默认关闭** ，可发送`list`查看服务列表自行启用

![ver](../public/images/demo/ver.png)