# 配置参考

Zoom默认的配置文件位置为 `./zoom.ini`，也可以在运行时使用 `-c` 参数指定配置文件，如：

```
$ ./zoom -c [path/zoom.ini]
```

## 配置项说明

## zoom

#### app_name

- Type: `string`
- Default: `Zoom-CI`

应用名称, 显示在访问页面标题。
#### app_host

- Type: `string`
- Default: `http://localhost:7002`

应用访问域名, 结尾不要加 `/`，主要是在邮件中使用。

#### local_space

- Type: `string`
- Default: `/tmp/zoom_data`

本地工作目录，Zoom所需的临时文件和编译打包归档文件都会在此目录中。

#### remote_space

- Type: `string`
- Default: `~/.zoom`

目标主机临时工作目录，用来临时存放需要部署的打包文件。

#### cipher_key

- Type: `string`
- Default: `pG1L62EM0cPIIOwusQsbcV8Cs6j/M1RxLoXIZylWUC4=`

AES加密/解密使用的私钥，秘钥需要进行base64编码

## serve

#### addr

- Type: `string`
- Default: `:7002`

HTTP服务监听的端口，Zoom默认监听7002端口

#### read_timeout

- Type: `int`
- Default: `300`

读超时时间设置, 单位秒。

#### write_timeout

- Type: `int`
- Default: `300`

写超时时间设置, 单位秒。


#### idle_timeout

- Type: `int`
- Default: `300`

空闲连接超时设置, 单位秒。

## database

#### unix

- Type: `string`
- Default: ` `

以 Unix Socket 方式连接MySQL。

#### max_idle_conns

- Type: `int`
- Default: `100`

最大空闲连接数。

#### max_open_conns

- Type: `int`
- Default: `200`

MySQL最大连接数。

#### conn_max_life_time

- Type: `int`
- Default: `500`

最长连接生命周期，单位秒。

#### host

- Type: `string`
- Default: `127.0.0.1`

MySQL连接主机名。

#### port

- Type: `int`
- Default: `3306`

MySQL连接端口。

#### user

- Type: `string`
- Default: `zoom`

MySQL连接用户名。

#### password

- Type: `string`
- Default: `zoom`

MySQL连接密码。

#### dbname

- Type: `string`
- Default: `zoom`

Zoom数据库名。

## log

#### path

- Type: `string`
- Default: `stdout`

错误日志输出路径。

可选的值:

- stdout 打印到标准输出
- /path/file 输出到文件

## mail

#### enable

- Type: `int`
- Default: `0`

是否开启邮件发送功能。

#### smtp_host

#### smtp_port

#### smtp_user

#### smtp_pass

[filename](include/footer.md ':include')