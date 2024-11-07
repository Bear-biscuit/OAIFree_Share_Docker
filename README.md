## 项目介绍  
基于始皇的OAIFree服务，搭建一个共享站，方便给自己的小伙伴们使用  

## 配置项  

请修改<kbd>.env</kbd>文件中的相关配置

关于邮箱部分，使用的是[cloudflare_temp_email](https://github.com/dreamhunter2333/cloudflare_temp_email)项目，请根据作者的部署教程进行部署(非必需)

## 部署 

1、克隆项目  

2、安装```docker```

3、安装```docker-compose```
确保安装的版本大于2.29.2

4、修改<kbd>.env</kbd>文件中的配置信息 

5、查看<kbd>docker-compose.yml</kbd>文件中的端口部分
```
- "5000:5000"  # 映射端口,前面的是你运行成功后访问网站的端口  

- "3306:3306"  # 映射 MySQL 的端口,一般不需要修改，如果你有一个正在运行的MySQL数据库，可能会有端口冲突，到时候执行更改这个端口即可
```

6、在项目目录运行```docker-compose up```

7、如果看到一下字样，就代表运行成功  
```
flask_app  | 在主进程中初始化自动刷新, 当前时间: 2024-11-07 13:05:04.351826
flask_app  | 设置初始定时器, 延迟秒数: 250715.195757
flask_app  |  * Serving Flask app 'run.py'
flask_app  |  * Debug mode: off
flask_app  | WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
flask_app  |  * Running on all addresses (0.0.0.0)
flask_app  |  * Running on http://127.0.0.1:5000
flask_app  |  * Running on http://172.18.0.3:5000
flask_app  | Press CTRL+C to quit
```



