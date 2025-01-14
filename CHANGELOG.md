## CHANGELOG

### 0.2.3 - 2020-05-15

1. 更多 action

2. 每个 action 除默认参数外，还可设置:
   - `api_path` `default=/v1/LuaApiCaller`
   - `iot_timeout` `default=self.timeout=10` IOTBOT 端处理允许等待的时间
   - `bot_qq` `default=self.qq` 机器人 QQ 号

### 1.0.0 - 2020-05-28

#### 大改动

1. 插件化
2. 效率更高，不漏消息
3. 更多快捷方法
4. 更多自定义参数

### 1.1.0 - 2020-06-19

1. 无需重启即可更新插件，正常调用`refresh_plugins`方法即可
2. 改了下刷新插件后的显示信息
3. 增加刷新 key 二次登陆 Action
4. 改善了生成模板

### 2.0.0

1. 支持队列发送
2. 支持中间件，可用于传递配置
3. 优化数据解析，提供解析更详细的函数
4. ...

### 2.1.0

1. 增加 webhook 功能，方便做远程服务
2. 废弃环境变量的配置方式，使用`.iotbot.json`进行配置
3. sugar 发送图片函数增加文字参数

### 2.2.0

1. 优化插件管理

### 2.2.1

1. 优化中间件的处理
2. 好友白名单改为好友黑名单
3. 配置文件增加群、好友黑名单配置项
4. Action 增加部分方法

### 2.3.1

1. 使用第三方库替代原来手动配置的 logger，日志不那么粗糙了
2. 移除 Action 中的设置日志参数

### 2.3.2

1. windows 上编码错误

### 2.3.4

1. 新增设置/取消管理员 Action
2. Action 对象的 host,port...等属性改为公开属性
3. 发送请求使用 session
4. GroupAdminsysnotifyEventMsgQQ 群系统消息通知消息完善
   ...

### 2.4.0

1. 移除 Action 每分钟限制发送频率的功能
2. 优化发送队列

### 2.4.1

1. action 检查 Ret 值时首先判断该字段是否存在

### 2.4.2

1. 封装获取包括群主在内的管理员方法

### 2.5.0

1. 优化插件管理，使用文件存储停用的插件信息
2. 添加 `is_botself`装饰器，只接收机器人自身消息
3. 去除冗余代码

### 2.5.1

1. 封装转发视频给群(repost_video_to_group)/好友(repost_video_to_friend)两个 action
2. 增加解析视频消息的 refine 函数

### 2.5.2

1. 修正误将 GetWebConn 作为心跳的错误

### 2.5.3

1. refine 函数不修改原上下文对象

### 2.6.0

1. 添加定时任务功能

## 2.6.1

1. 增加对发送错误码的描述

## 2.6.2

1. 优化 sugar 函数，增加对临时会话的支持
2. 好友消息增加字段 TempUin（临时会话的入口群聊 id)
3. refine 图片消息后对象的 GroupPic 列表成员由原始字典变为单独的图片对象

## 2.6.4

1. 增加辅助构建宏模块
2. 对旧版 atUser 参数做兼容
3. 模块 refine_message 更名为 refine

### 2.7.0

1. 可添加连接成功或断开连接后执行的钩子函数

### 2.7.1

1. [commit](https://github.com/xiyaowong/python--iotbot/commit/78820ac0134d24ae337a64e5c25d2738815c209e)

### 2.7.2

1. 增加接收函数装饰器(startswith)
2. 修改接收函数装饰器`equal_content`逻辑

### 2.7.3

1. 装饰器 equal_content 少一步对 MsgType 的判断
