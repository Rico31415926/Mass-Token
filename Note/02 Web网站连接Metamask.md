1. 新建html文件

   

   

2. 引入Vue

   https://cn.vuejs.org/guide/introduction.html

   

   ![image-20230813091810489](C:\Users\Ruichao\AppData\Roaming\Typora\typora-user-images\image-20230813091810489.png)





3. 思考页面布局，加上样式

   ![image-20230813093019667](C:\Users\Ruichao\AppData\Roaming\Typora\typora-user-images\image-20230813093019667.png)![image-20230813093056610](C:\Users\Ruichao\AppData\Roaming\Typora\typora-user-images\image-20230813093056610.png)

 



4. 引入ether.js

   https://docs.ethers.org/v5/
   
   ![image-20230813171227029](C:\Users\Ruichao\AppData\Roaming\Typora\typora-user-images\image-20230813171227029.png)





5. 参考Metamask开发文档的提示，编写以下代码

   ```js
   // 登录MetaMask
   async login(){
       
   	// Provider 是提供对区块链及其状态的只读访问，即连接
   	provider = new ethers.providers.Web3Provider(window.ethereum);
       
   	// 进行钱包授权
   	account = await provider.send("eth_requestAccounts", [])
       
   	// 获取签名者
   	signer = provider.getSigner()
   	
       // 如果account[0]存在，即表示连接成功，即为当前地址
   	if (account[0]) {
   		this.userAdd = account[0];
   	}
   
   }
   ```





6. VS Code安装Live Server 本地服务器

   ![image-20230814003959272](C:\Users\Ruichao\AppData\Roaming\Typora\typora-user-images\image-20230814003959272.png)

   然后在您的Html文件中，右键选择 Open with Live Server![image-20230814004620690](C:\Users\Ruichao\AppData\Roaming\Typora\typora-user-images\image-20230814004620690.png)





7. 点击登录按钮，经批准后，成功登录，并显示当前您的地址

   ![image-20230814004759557](C:\Users\Ruichao\AppData\Roaming\Typora\typora-user-images\image-20230814004759557.png)







8. 监听钱包的地址切换事件，更新数据

   .on 表示一直监听，.once表示监听一次

   ![image-20230814021609771](C:\Users\Ruichao\AppData\Roaming\Typora\typora-user-images\image-20230814021609771.png)

   
