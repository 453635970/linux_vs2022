# linux_vs2022



wsl --install

wsl --install -d Ubuntu


# 查看是否安装成功
wsl --list --verbose

  NAME      STATE           VERSION
* Ubuntu    Running         2


# 检查 WSL 版本：
 wsl --version


更新软件包列表 
sudo apt update

安装软件包
sudo apt install gedit

卸载软件包：
sudo apt remove gedit


----------------------------------------使用vs2022 开发linux程序 
查看ip
ip addr




配置 WSL 与 VS2022 连接
sudo apt update
sudo apt install gcc g++ gdb make ninja-build


# 安装 OpenSSH 服务器（若未安装）
sudo apt update
sudo apt install openssh-server
sudo service ssh start



linux 是root的话
sudo nano /etc/ssh/sshd_config
修改
PermitRootLogin prohibit-password → 改为 PermitRootLogin yes（允许 root 用密码登录）
PasswordAuthentication no → 改为 PasswordAuthentication yes（允许密码认证）

sudo service ssh restart
# 检查状态
sudo service ssh status


通过绝对路径进入目录
cd /home/user/documents

进入当前目录下的子目录
cd music

返回上一级目录
cd ..

回到用户主目录
cd ~