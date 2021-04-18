# 使用问题列表

#### 部署失败：[cmd] $ echo 'packfile empty' && exit 1 X

原因：构建脚本中未打包出tgz文件，检查是否使用 `tar -zcf` 命令进行打包。


#### 部署失败: task run failed, exit status 255
原因：部署服务在远程服务器没有[免登陆权限](server.md?id=秘钥配置) 

[filename](include/footer.md ':include')