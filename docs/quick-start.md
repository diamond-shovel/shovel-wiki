



## 🚀 Shovel 快速部署指南

### 环境准备
✅ **最低配置要求**  
- 操作系统：Ubuntu 20.04+/CentOS 7+  
- 内存：8GB+  
- 磁盘：40GB+ 可用空间  
- 网络：开放80端口  


```
# 检查端口占用情况
sudo lsof -i :80
```

---

### 一键部署流程



```bash
curl -sSL https://shovel.cyberspike.top/install.sh -o install.sh && bash install.sh
```

**注意**: 国内部分地区脚本直连github仓库获取镜像可能会出现卡顿等网络问题，建议手动从[官方仓库](https://github.com/ansanyuan/shovel-workbench)下载最新[镜像包](https://github.com/ansanyuan/shovel-workbench/releases)并重命名为image.7z，放入脚本的同目录下


![](img/2025-04-09-15-52-57.png)

如图:

![](img/2025-04-09-16-03-15.png)

并运行安装脚本即可

🔄 **安装过程将自动完成以下操作**：  

1. 初始化Docker环境  
2. 下载基础镜像（约1GB）   
3. 部署核心服务组件  
4. 加载插件（速度根据服务器性能而定）

---

## 📲 验证码获取流程

当出现以下提示时：  

```
请输入镜像激活码：
```

1. 访问公众号 中龙技术
2. 发送关键词 **SHOVEL-ACTIVATE**  
3. 获取验证码

---

## ⚙️ 自定义配置（可选）

### 设置管理员密码

<img src="./img/password.png?raw=true" alt="shovel" style="width: 50%;">

---

## 🎉 部署完成验证

1. 访问控制台  
   `http://<你的服务器IP>`

2. 登录验证  

   ```
   默认账号：admin
   初始密码：安装过程中设置的密码
   ```

3. 查看服务状态  

```bash
docker ps -a --format "table {{.ID}}\t{{.Names}}\t{{.Status}}"
```
---

## 🚨 常见问题排查

### 端口冲突处理

```bash
# 查看占用80端口的进程
sudo lsof -i :80

# 临时结束占用80端口的进程，有风险需自行甄别
sudo systemctl stop xxx
```

## 正式开始您的shovel之旅

Shovel 创新地引入了资产组和策略，让工作更加高效便捷，所以让我们从新建资产组开始，详情请见文档

1. **创建资产组和负责实体：** 将相关资产分组，并指定负责实体以便管理。

   <img src="./img/creat.jpg?raw=true" alt="shovel" style="width: 100%;">


   

2. **创建策略：** 选择目标资产组，并根据场景配置不同插件，可以批量导入，直接粘贴进多行ip或域名即可。

   

   <img src="./img/strategy.jpg?raw=true" alt="shovel" style="width: 60%;">

   

3. **开始任务：** 选择策略即可开始任务，也可手动导入和管理资产。

   <img src="./img/start.jpg?raw=true" alt="shovel" style="width: 100%;">

   

   

4. **定时任务（可选）：** 在任务菜单中创建定时任务，实现自动化操作。

   <img src="./img/time.jpg?raw=true" alt="shovel" style="width: 100%;">

