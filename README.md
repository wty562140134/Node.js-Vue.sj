# Node.js-Vue.sj

## 配置环境
### 安装Node.js,使用nvm管理工具管理node.js版本:
1.  windows:
    [访问](https://github.com/coreybutler/nvm-windows/releases)解压安装后将nvm添加到环境变量中<br>
    打开控制台输入 nvm -v查看是否安装成功
2.  linux:
    
        curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash 
        wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash
    下载完成后cd到nvm路径
        
        ~/.nvm
     进行安装,安装完成后添加环境变量
        
        source ~/.bashrc
        vim ~/.bash_profile, ~/.zshrc, ~/.profile, or ~/.bashrc
     添加
     
        export NVM_DIR="${XDG_CONFIG_HOME/:-$HOME/.}nvm"[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
     使用
     
        nvm -v
      查看是否安装成功<br>
3.    nvm常用命令:
         arch参数表示系统位数，默认是64位，如果是32位操作系统，需要执行命令：nvm install <version> 32
         安装指定版本:
         
          nvm install <version> [<arch>]
         使用指定版本:
         
          nvm use <version> [<arch>]
         卸载指定版本:
         
          nvm uninstall <version>
         查看目前已安装的 node 及当前所使用的 node:
         
          nvm ls
         查看目前线上所能安装的所有 node 版本:
         
          nvm ls-remote
         使用指定版本作为预设使用的 node 版本:
         
          nvm alias default <version>
         使用淘宝镜像
          
          npm install -g cnpm --registry=https://registry.npm.taobao.org
         
         
          
### 安装VUE.js
1.[查看](https://cn.vuejs.org/v2/guide/installation.html#NPM)最新安装稳定版 -g为全局安装

    npm install vue -g
若想安装最新版,先卸载原来已有的版本

    npm uninstall vue-cli -g
    npm install -g @vue/cli

## 下载依赖
安装webpack

    npm install webpack -g
构建项目

    vue init webpack <projectname>
cd到项目路径下安装依赖包
    
    vue install 
  对于快速原型开发使用构建一个全局的扩展(https://cli.vuejs.org/zh/guide/prototyping.html)
  
    npm install -g @vue/cli-service-global
