# Blog
我的博客
前端
名称：blog
技术栈：Vue+Element+Layui
主要页面：
首页
博客
留言
日记
友联
关于
404页面
主要功能：
用户登录/注册
用户添加/修改头像
用户留言/回复
文章搜索
最近访客
Canvas特效
 
后端
名称：blogadmin
技术栈：Node+Express+MongoDB
中间件：session存储用户信息和时效期
主要功能：
文章管理
发表文章
管理文章
用户管理
权限管理
留言管理
删除留言
日记管理
发表日记
管理日记
友链管理
添加友链
删除友链
名称 方法 API 参数 说明 getArticleShow get /article/getShow skip,limit,tag 获取文章列表 getArticle post /article _id 获取单篇文章信息 getArticleInfo post /article/getInfo 无 获取文章 getArticleExtend post /article/extend tag 获取延伸阅读 getArticleSearch post /article/search keywords 搜索文章 getRegisterVCode post /register/vcode 无 获取验证码图片 getRegisterCheckVcode post /register/checkVcode svgCode 验证码的提交验证 postRegister post /register 必需有user、 pwd、 svgCode 注册 postLogin post /login options 登录 postIfLogin post /login/ifLogin 无 是否登录 postLogout post /login/logout 无 登出
commitMessage post /message/commit options 留言
commitChildMessage post /message/childCommit options 子留言 getMessageList post /message/getList skip=0,limit=5 留言列表默认限制五条 getVisitor get /visitor 无 最近访客 getDiart get /diary 无 日记 getLinks get /links 无 友链
Blog接口
名称 方法 API 参数 说明 postArticle post /article/add type,title,content,tag,surface 发表文章 getArticle get /article/get"+ ?
skip=${skip}&limit=${limit}
skip=0,limit=5 请求文章 deleteArticle post /article/delete _id 删除文章 updateArticle post /article/update _id,options 更新文章 getArticleInfo get /article/getInfo 无 请求articleInfo getUserList get /user/get 无 请求用户 列表 getUserInfo get /user/info?id="+id _id 请求单个 用户数据 deleteUser post /user/delete _id 删除用户 updateUser post /user/update _id,data 更新用户 数据 getMessageList get /message/get 无 请求留言 列表 deleteMessage post /message/delete _id 删除留言 postDiary post /diary/submit txt,img 发表日记 getDiary get /diary 无 请求日记 deleteDiary post /diary/delete _id 删除日记 updateDiary post /diary/update _id,data 更新日记 postLinks post /links/submit options 发表友链 getLinks get /links 无 请求友链 deleteLinks post /links/delete _id 删除友链 login post /login options 管理员登 录 ifLogin post /login/ifLogin 无 管理元是 否登录
BlogAdmin接口
数据库
articleinfos--获取文章
articles--文章
diaries--日记
links--友链
messages--留言
sessions--用户登录信息
users--用户
visitors--访客
