## 修改git提交方式为**ssh**
* 了解ssh公钥登录  
所谓"公钥登录"，原理很简单，就是用户将自己的公钥储存在远程主机上。登录的时候，远程主机会向用户发送一段随机字符串，用户用自己的私钥加密后，再发回来。远程主机用事先储存的公钥进行解密，如果成功，就证明用户是可信的，直接允许登录shell，不再要求密码。
* 生成ssh公钥/私钥(rsa)  
<https://help.github.com/articles/working-with-ssh-key-passphrases/>  
```
  ssh-keygen -t rsa -C "email@address.com"
```                    
passphrase: 对私钥设置口令
* 将公钥上传到远程主机  
如果使用github, 可以选择是在账户中添加, 也可以选择在单个项目中添加
* 修改本地git库 url 
<https://help.github.com/articles/changing-a-remote-s-url/>
或者直接修改`respository/.git/config`中`url`选项  
* 修改用户名  
<http://stackoverflow.com/questions/4220416/can-i-specify-multiple-users-for-myself-in-gitconfig>
```
  git config user.name Name  
  git config user.email email@address.com
```
       
  
