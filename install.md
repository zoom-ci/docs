> 安装 Zoom 非常简单，若您在安装过程中遇到问题或无法找到解决方式，请[提交Issue](https://github.com/zoom-ci/zoom-ci/issues)，我们会尽力解决您的问题。

## 环境需求

**操作系统**

Linux / macOS + Bash. 需要注意的是Zoom不支持Win系统。

**MySQL**

MySQL 5.6+

**Git**

升级操作系统Git到最新版本。

## 安装/升级

### 1、下载[最新版本release包](https://github.com/zoom-ci/zoom-ci/releases),并将其拷贝到任意目录（比如：~/zoom_workspace）;

#### 全新安装
```shell
$ ./zoom-v1.0.3-darwin-amd64   # 这里以mac 64位版为例 

 _____________________________
       ___                    
         /                    
 -------/-----__----__---_--_-
       /    /   ) /   ) / /  )
 ____(_____(___/_(___/_/_/__/_
     /   Make CI/CD Easier.  
 (_ /                         


Service:              zoom
Version:              v1.0.3
Config Loaded:        ./zoom.ini
Log:                  stdout
Mail Enable:          0
HTTP Service:         :7002
Start Running...
```

#### 升级安装
如果您是从syncd2.0.0升级到zoom，需要注意，两个方式：
1）、先将syncd对应的配置文件改名为zoom.ini，并拷贝zoom可执行文件（第1步下载的文件）同级目录；
2）、在运行zoom的时候，通过“-c”参数指定配置文件地址，
上面两个方式可自行选择，之后在第一次运行时增加参数 “ -upgrade syncd”（系统会自动进行更新数据库以及配置），后续执行则不需要使用。
```shell
$ ./zoom-v1.0.3-darwin-amd64 -upgrade syncd   # 这里以mac 64位版为例 

 _____________________________
       ___                    
         /                    
 -------/-----__----__---_--_-
       /    /   ) /   ) / /  )
 ____(_____(___/_(___/_/_/__/_
     /   Make CI/CD Easier.  
 (_ /                         


Service:              zoom
Version:              v1.0.3
Config Loaded:        ./zoom.ini
Log:                  stdout
Mail Enable:          0
HTTP Service:         :7002
Start Upgrading from Syncd2.0 ... OK  # 这里提示OK则表示升级成功
Start Running...
```

### 2、打开浏览器，访问 `http://localhost:7002` (出现下图界面)，配置数据库及管理员信息，安装完成。
<img class="app-img-eg" height="400" src="assets/img/zoom-install.png" />


[filename](include/footer.md ':include')