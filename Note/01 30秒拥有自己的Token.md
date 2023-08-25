使用openzeppelin的ERC20模板，快速创建令牌

https://docs.openzeppelin.com/contracts/4.x/

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.9;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract MyToken is ERC20 {
    constructor() ERC20("MyToken", "MTK") {
        _mint(msg.sender, 10000 * 10 ** decimals());
    }
}
```



 

名称：“MyToken”

![image-20230630222453769](C:\Users\Ruichao\AppData\Roaming\Typora\typora-user-images\image-20230630222453769.png)



简称：“MTK”

![image-20230630222553949](C:\Users\Ruichao\AppData\Roaming\Typora\typora-user-images\image-20230630222553949.png)



数量：10000

![image-20230630222616850](C:\Users\Ruichao\AppData\Roaming\Typora\typora-user-images\image-20230630222616850.png)



