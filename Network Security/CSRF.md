# 跨站请求伪造(Cross Site Request Forgery)

通过伪造用户请求达到攻击目的

## 攻击示例：
在允许外链的网站，通过使用网站自身带有创建或修改性质的api伪装为图片地址发送。当其他用户页面中出现这个伪造链接时由于浏览器将api识别为图片地址，则自动携带cookie发出get请求。在用户不知情的情况下由用户发起对自身的攻击

## 防范措施：
1. 严格按标准的 `RESTful` 设计规范设计网站api，get用于请求资源，post用于创建，put用于更新，delete用于删除，atch用于更新补丁
1. 关键请求需要携带token，token可内嵌至网页中
