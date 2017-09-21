# Nodejs安装与配置

下载地址：https://nodejs.org/en/download/releases/

根据linux系统版本和根据项目需要来选择Nodejs版本

    # wget https://nodejs.org/download/release/v8.0.0/node-v8.0.0-linux-x64.tar.gz

较新的版本都会带有npm

**解压，重命名**

    # tar -zxvf node-v8.0.0-linux-x64.tar.gz
    
    # mv node-v8.0.0-linux-x64 nodejs
    
**软连接**

    # ln -s /usr/local/nodejs/bin/npm /usr/local/bin/
    
    # ln -s /usr/local/nodejs/bin/node /usr/local/bin/
    
**检查版本**

    # node -v
    
    # npm -v