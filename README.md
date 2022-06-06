## 插件简介

LoveKKCommentModify是一款Typecho邮件通知类插件，支持SMTP、Send Cloud、阿里云邮件推送三种邮件通知方式。

在评论审核通过、用户评论文章、用户评论被回复时对不同场景进行不同的邮件通知。

测试找回密码等功能均正常

修改自[gogobody](https://github.com/gogobody/LoveKKCommentModify)

特色：  
1. 添加站长辅助功能，支持在文章页给审核不通过的文章作者发邮件。 
2. 支持审核通过的自动发邮件。
3. 支持其他作者发文章的时候提醒管理员。


## 安装方法

> 1. 将下载的压缩包进行解压并上传至`Typecho`插件目录中，注意目录名称更改为`LoveKKCommentModify`；
> 2. 后台激活插件；
> 3. 根据自己的实际情况选择邮件发送接口方式；
> 4. 根据所选的邮件发送接口，配置相应接口参数。

## 自定义模板说明

插件共有七个模板，保存在插件`theme`目录下，分别为：

> 1. approved.html：邮件审核通过通知模板。
> 2. author.html：文章评论通知作者模板。
> 3. reply.html：评论回复通知被回复者模板。
> 4. foeget.html：忘记密码
> 5. notifyAuthorCheck：提醒作者查看投稿信息
> 6. postcheckfail：审核人通知作者 投稿审核不通过
> 7. postchecksucc: 审核人通知作者 投稿通过
三个模板使用变量作为内容替换，您只需在自己的模板中增加相应的模板变量即可，模板变量列表如下：

### approved.html

> 1. {blogUrl}：博客地址
> 2. {blogName}：博客名称
> 3. {author}：评论者名称
> 4. {permalink}：文章链接
> 5. {title}：文章标题
> 6. {text}：评论内容

### author.html

author.html内变量与approved.html内变量一致。

### reply.html

> 1. {blogUrl}：博客地址
> 2. {blogName}：博客名称
> 3. {author}：被回复者名称
> 4. {permalink}：文章链接
> 5. {title}：文章标题
> 6. {text}：被回复者评论内容
> 7. {replyAuthor}：回复者名称
> 8. {replyText}：回复内容