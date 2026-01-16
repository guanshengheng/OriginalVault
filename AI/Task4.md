## 项目地址
代码放在github的仓库里[Task4](https://github.com/shannonkwan86/task4)

## 开发思路
大致思路就是把Task3里的cli项目借助前后端框架做成了简陋的web应用，然后我用docker打包镜像，并放到了我的阿里云服务器上。

## 开发过程

### 后端部分

文件结构如图
![](assets/Task4/file-20260116181258432.png)

使用**fastapi**框架。Task3中是直接在命令行中输入输出，现在改成通过前端读取用户输入，输出也是以json返回给前端。
agent.py作为service层，是Task3中的main.py，几乎没做修改，只将prompt作为参数传递进函数。
main.py作为controller层，cors跨域接受前端请求，pydantic模型解析json得到str类型的prompt传给agent.py，返回响应结果。

### 前端部分

使用**vue**框架，数据绑定、事件处理等方面简洁易用，更专注于逻辑的处理。
前端部分都在文件**agent-web\src\App.vue**里
send函数做了条件判断，正在发送则不能发送、输入为空不能发送。将用户输入添加进要展示的数组。发送http请求到后端，解析返回值，把md格式的页面转换成html渲染，添加进要展示的数组。另外有简单的错误处理。
html的骨架和css样式借助了ai工具完成。

### 打包部署