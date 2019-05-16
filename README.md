### 安装
Debian / Ubuntu:

    apt-get install git
    git clone https://github.com/GoCac/shadowsocksr.git

CentOS:

    yum install git
    git clone https://github.com/GoCac/shadowsocksr.git

Windows:

    git clone https://github.com/GoCac/shadowsocksr.git

**然后切换到分支 manyuser, 默认分支是空的，为了防止追杀**

### 初始化
If you clone it into `~/ssr-backup`  
move to `~/ssr-backup`, then run:

    bash initcfg.sh

### 配置

#### 命令行直接运行
move to `~/ssr-backup/shadowsocks`, then run:

    python server.py -p 628 -k asdfghjkl -m none -O auth_chain_a -o http_simple -d start
    python server.py -p 端口 -k 密码 -m 加密方式 -O 协议 -o 混淆 -d start

#### 配置文件
You can also use a configuration file instead (recommend), move to `~/ssr-backup` and edit the file `user-config.json`, then move to `~/ssr-backup/shadowsocks` again, just run:

    python server.py

To run in the background:

    ./logrun.sh

To stop:

    ./stop.sh

To monitor the log:

    ./tail.sh
