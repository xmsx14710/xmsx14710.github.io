# Install Node.js
▶Install Node.js

>[Windows安装Node.js官方指南](https://docs.microsoft.com/en-us/windows/dev-environment/javascript/nodejs-on-windows)

- **Step 1**: Download & Install nvm-windows

  >NVM全称Node.js Version Manager（Node.js版本管理器）

  - [nvm-windows GitHub下载地址](https://github.com/coreybutler/nvm-windows/releases)

- **Step 2**: Install Node.js

  - 查看Node.js最新稳定的LTS版本
    ```
    nvm list available
    ```

  - <font color="red">注意此时可能会报错 </font> 

    >【可能是代理问题】找到代理服务器地址，打开Windows设置▶网络和Internet▶代理▶使用代理服务器，然后打开编辑即可看到本机代理服务器地址。

     ```
     # nvm proxy [url] 即是  nvm proxy 代理服务器地址
     nvm proxy http://127.0.0.1:port
     ```
  - 安装Node.js

    >nvm install < version \>,替换<version>为数字，即nvm install 16.15.1。

     ```
     nvm install 16.15.1
     ```
  - 使用该版本的Node.js

    >nvm use [version] 

    ```
    nvm use 16.15.1
    ```
  - **完成/finished**