#### 此项目是基于vue-cli 脚手架 使用nginx反向代理 进行跨域

需要修改的文件 
- config/dev.env.js
- config/prod.env.js
- config/index.js
- nginx/conf/nginx.conf

##### 1.将项目打包   运行命令 npm run build
##### 2.将打包后的dist目录下的文件放到nginx文件夹下的html文件夹下
##### 3.进入nginx文件夹下,运行命令 start nginx 
##### 4.浏览器输入 http://localhost:8080/#/xxxxx  xxxxx表示路由
##### 5.修改nginx.conf文件后需要重新运行 nginx -s reload
