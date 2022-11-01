用于 Typecho 博客程序具的评论邮件通知插件，仅支持 1.2.0 及以上版本

# 特性

高效：使用异步发信，不影响评论速度

简洁：后台简洁、代码简洁、核心代码不足300行

方便：保存插件配置自动发送测试邮件，自动记录发信错误日志可随时检查，正常发信无日志

拥有完善的发信逻辑，如下表所示：

看不懂也没关系，总之体验很不错就对了！！！

| 评论者 | 上级评论者 | 新评论通知站长 | 上级被评论通知 | 评论者审核通过 |
| ------ | ---------- | -------------- | -------------- | -------------- |
| 站长   | -          | ×              | ×              | ×              |
| 站长   | 站长       | ×              | ×              | ×              |
| user1  | -          | √              | ×              | √              |
| user1  | user1      | √              | ×              | √              |
| 站长   | user1      | ×              | √              | ×              |
| user1  | 站长       | ×              | √              | √              |
| user1  | user2      | √              | √              | √               |

# 模板

| 变量         | 含义         |
| ------------ | ------------ |
| {time}       | 评论发出时间 |
| {author}     | 昵称         |
| {mail}       | 邮箱         |
| {url}        | 网址         |
| {ip}         | IP           |
| {agent}      | UA           |
| {text}       | 内容         |
| {parentName} | 父级评论昵称 |
| {parentText} | 父级评论内容 |
| {parentMail} | 父级评论邮箱 |
| {title}      | 文章标题     |
| {permalink}  | 评论链接     |
| {siteTitle}  | 网站标题     |
| {siteUrl}    | 网站地址     |


# 说明

目前异步发信可能无法成功执行，暂未找到原因

# 更新

1.1.0

增加 测试日志记录模式

增加 手动关闭异步以解决某些奇怪情况无法发信的问题

博客地址：https://www.zhaoyingtian.com/archives/mailer.html
