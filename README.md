---
title: Qinglong
emoji: 🏃
colorFrom: yellow
colorTo: purple
sdk: docker
pinned: false
app_port: 5700
---

Space secrets(Private)说明:   
ADMIN_USERNAME:登陆用户名   
ADMIN_PASSWORD:登陆密码   
RCLONE_CONF:rclone配置内容，可选   

## 注意 
docker-entrypoint-rclone.sh为可以在容器重置时恢复数据的配置，需要设置上面的RCLONE_CONF  
其中名称为huggingface,文件夹为:/qinglong   
rclone远程文件夹为huggingface:/qinglong   
进入后台后需要新建个同步的计划任务代码为:  

```
rclone delete huggingface0:/qinglong/db/database.sqlite && rclone sync /ql/data huggingface0:/qinglong
```
备份时间可以根据自己的情况设置我这里设置每天1点更新: 0 1 1 * * * 

Check out the configuration reference at https://huggingface.co/docs/hub/spaces-config-reference

[huggingface]
type = webdav
url = https://pan.hefamily.net/dav
vendor = other
user = yuanshang000@yssc0.top
pass = bMMj6XaI3P7EfNfJLUSK9N7sDGagAJytjCVbUwAaOyxz1H_3vybtAZ54cpaM1udH

[huggingface0]
type = webdav
url = https://pan.hefamily.net/dav
vendor = other
user = ys0@yssc0.top
pass = 3inmJO3VLYrncmltfa7eqviz0f3EUH6QL-1SfKWNYADYurC96Au81CtnURXEA5aT



[huggingface1]
type = webdav
url = https://pan.hefamily.net/dav
vendor = other
user = ql@yssc0.top
pass = nWspl3HXutmwRJCxcykkkRgbjGVW0G9tBZl4xg42-C86XT6vqocI51CFQb43S2f0
