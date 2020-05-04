## movie-zip (压缩版代码)
#### 一个基于VueCli的小项目，用到了Vue,Vuex,VueRouter,Element-UI,Better-scroll,swiper,axios等技术；
***
#### 项目预览:http://123.57.46.110/miaomiao/
![预览二维码](E:/新下载/Saved Pictures/movie.png)
#### 项目本地运行步骤:
- 点击 Clean and Download 按钮
```
download ZIP
```

- 本地解压（用编辑器打开,VScode/HBulidX/Sunlime等均可）

- 将文件拷贝到 nginx 的 html 目录下  
项目在开发过程中用到了反向代理来解决跨域问题。打包之后，使用 nginx 做代理服务器，并且做相关的配置。

- 打开 nginx.conf 文件，实现反向代理的相关配置
```
//在 service 中添加
location ^~/api/ {
	proxy_pass http://39.97.33.178/api/;
}

```

- 重新启动 nginx
```
nginx -s reload
```

- 在浏览器中输入对应 URL 进行访问 
```
//我的本地 nginx 的端口号为8888
http://localhost:8888/miaomiao
```
***
