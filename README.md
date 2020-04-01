# SSHPass

SSHpass offers you the ability to automatically offer a password via SSH when
you are prompted for it.

## Install

```bash
git clone git://github.com/kevinburke/sshpass.git
cd sshpass
./configure
make && make install
```
## 用法说明  
1：直接远程连接某台主机：  
`sshpass -p xxx ssh root@192.168.11.11`xxx为密码。  
2：远程连接指定ssh的端口：
`sshpass -p 123456 ssh -p 1000 root@192.168.11.11 (当远程主机不是默认的22端口时候)`  
3：从密码文件读取文件内容作为密码去远程连接主机  
`sshpass -f xxx.txt  ssh root@192.168.11.11`  
4:连接伪终端，避免避免第一次登录出现公钥检查
`sshpass -f /1.txt  ssh -t -o StrictHostKeyChecking=no -p 6000 root@yourip`  
## Notes

This repository is a mirror of http://sourceforge.net/projects/sshpass/develop

Pull requests will not be accepted

##### Maintainers

kevin burke <kev+sshpass@inburke.com>
