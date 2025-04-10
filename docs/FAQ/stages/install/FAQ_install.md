# FAQ

* 此文档包含了在安装过程中可能遇到的一些常见问题及其解决方案。

## 权限不足 & Permission Denied
- **问题描述**：在安装过程中，出现权限不足的错误提示。
- **解决方案**：
    - 检查当前用户是否具有足够的权限来执行安装操作。
    - 如果在Linux系统上，尝试使用`sudo`命令来提升权限。
- **示例**：
    ```bash
    curl -sSL https://shovel.cyberspike.top/install.sh -o install.sh && sudo bash install.sh
    ```

## 解压失败
- **问题描述**：在安装过程中，解压缩镜像文件失败。
- **解决方案**：
    - 此问题可能是下载的镜像文件损坏或不完整导致的、或解压密码不正确。
    - 尝试删除已下载的镜像文件，并重新运行安装脚本。
    - 或查看quick-start中的获取验证码的正确流程，重新获取并输入验证码。
- **示例**：
    ```bash
    rm -rf image.7z
    ```

## 网络问题
- **问题描述**：在安装过程中，出现网络连接错误或下载速度缓慢。
- **解决方案**：
    - 检查网络连接是否正常。
    - 如果在中国大陆地区，建议使用国内镜像源或VPN来加速下载。
    - 或查看quick-start中的手动下载镜像的正确流程，手动下载并放入脚本同目录下。
  
## KeyError: 'ContainerConfig'
- **问题描述**：在安装过程中，出现KeyError: 'ContainerConfig'的错误提示。
- **解决方案**：
    - 此问题是由于Docker版本过低导致的，并用户手动使用了docker-compose命令。
    - 建议升级Docker到最新版本。
    - 建议使用脚本安装，脚本会自动安装最新版本的Docker和docker compose。
    - 如果您执意手动启动，那么请使用`docker compose up -d`命令来启动服务(但这种启动方式未经测试，可能出现一系列意料之外的问题)。
  
## 想要卸载或重装Shovel
- **问题描述**：在安装过程中，想要卸载或重装Shovel。
- **解决方案**：
    - 如果您想要卸载Shovel，您需要执行以下几步。
    1. 停止所有Shovel相关的Docker容器。
    2. 删除所有Shovel相关的Docker镜像。
    3. 删除Shovel相关的Volumes。
