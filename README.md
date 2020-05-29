## movie-zip (压缩版代码)
##### 一个基于 Vue-CLI3.0x 的移动端小项目，项目中用到了Vue,Vuex,VueRouter,Element-UI,Better-scroll,swiper,axios等技术；主要有正在热映，即将上映，电影详情，影院详情，城市定位，影片搜索，用户登录等功能页面。制作过程中让我对基于 Vue-CLI3.0x开发Vue单页面应用有了更新的认识，也加深了对Vue全家桶，Axios和Better-Scroll / swiper 中移动端滑动组件的应用等。
#### 项目预览:  
![movie.png](https://i.loli.net/2020/05/04/JvbXYIicGT9ulE6.png)
***
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
