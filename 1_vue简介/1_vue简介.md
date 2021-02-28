# 1_vue简介
##  1_1 Web前端开发阶段
- 阶段1：原代码开发阶段（html+css+javascript），简称hcj开发。
- 阶段2：代码库阶段（js中使用jQuery，css中使用Bootstrap响应式框架（有成熟的网站结构等））。
- 阶段3：框架开发阶段，MVC模式和MVVM模式。
## 1_2 前端框架系统架构
- MVC和MVVM模式
- 主流MVVM模式
## 1_3 前端框架系统架构解刨
### 1_3_1 MVC模式（数据单向通信）：模型（Model）、视图（View）和控制器（Controller）
- View：接收用户动作（Dom事件，Ajax等），传递指令给Controller。
- Controller：接收到指令完成业务逻辑，要求Model改变状态。
- Model：将新的数据发送给View，用户动作触发的结果反馈。
### 1_3_2 MVVM模式（数据双向通信）：模型（Model）、视图（View）和视图模型（View&Model）
- View：接收用户动作（Dom事件，Ajax等）。
- Model：与View&Model进行数据双向绑定，Model层监听View&Model的变化。
- View&Model监听View层请求状态的变化，同时刷新View层显示。
Angular，谷歌开发，MVVM框架。大型复杂应用。
React，Facebook开发JS库（不是严格意义上的MVVM框架），标准的JS规范。中大型应用、移动跨平台。
Vue，尤雨溪，2014年开发，MVVM框架，中小型轻量级应用。
##  1_4 Vue框架下载
vue.js下载地址：https://vuejs.org/js/vue.js
## 1_5 Vue框架引入方式
- 本地文件引入，下载vue.js放置在相对目录。
- CDN方式引入，CDN是内容分发网络，就近引入原则，CDN方式引入vue.js地址：https://unpkg.com/vue
- NPM和Webpack模块包引入
	- NPM是前端主要开发工具，把复杂的js文件库组织成模块化管理方式，使用时，只需要引入指定模块即可。
	- Webpack把模块化编码的程序进行打包生成，从而允许在不支持es6语法的浏览器中访问。
- Vue-Cli工具
	- vue-cli工具是vue官方提供的模块和打包集成管理工具，需要npm和node环境的支持。
	- Vue在线练习网站：jsfiddle.net，地址为：https://jsfiddle.net