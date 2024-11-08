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

7、如果看到以下字样，就代表运行成功  
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

8、使用ip:端口访问  
默认管理员账号  
```
admin  123123
```

## 页面预览  
登录
![login](https://github.com/user-attachments/assets/adefeaf2-46cc-445f-a106-0abd7aa176da)
注册
![注册](https://github.com/user-attachments/assets/0e1ce0b1-a9be-410a-a5b9-05411b5a2be8)
2FA
![2FA](https://github.com/user-attachments/assets/60fc7c26-f9b9-4be2-a5fb-f536f33ab7ea)
忘记密码
![忘记密码](https://github.com/user-attachments/assets/041733f5-73af-433f-ab60-dbfed148a76a)
![重置密码](https://github.com/user-attachments/assets/e29bce0d-e258-420a-8446-ec5fadcfd6a4)
共享页
![首页](https://github.com/user-attachments/assets/38928d62-7162-41fa-a9e6-86efffa1ef29)
![个人页](https://github.com/user-attachments/assets/2854ad46-a4d1-47b2-ac9b-1d3afab62fa0)
管理员仪表盘
![管理员仪表盘](https://github.com/user-attachments/assets/8f54e760-5c99-478d-b88f-d46be917ef24)
用户管理
![用户设置](https://github.com/user-attachments/assets/cbd89e16-b398-449b-a3bf-6753867e268f)
GPT账号管理
![gpt](https://github.com/user-attachments/assets/482f767e-89c2-414a-810f-3dde0ec76d3e)
Claude账号管理
![claude](https://github.com/user-attachments/assets/bba0fdd2-2179-4c8e-98c0-b7863870aad9)

