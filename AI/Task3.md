代码托管在github上，地址是[task3](https://github.com/shannonkwan86/task3)
## 开发思路
选取阿里云百炼的联网搜索MCP 使得大模型可以联网搜索
![](assets/Task3/file-20260112193023051.png)

开发思路是通过LLM自己判断是否要进行调用MCP工具解答用户的问题，不调用工具就输出并结束。
具体而言是以下步骤。首先配置并连接，
![](assets/Task3/file-20260112193205584.png)
![](assets/Task3/file-20260112193215019.png)