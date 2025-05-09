

[![Shovel Logo](img/favicon.ico)](https://github.com/diamond-shovel/diamond-shovel)
# SHOVEL PLUGINS

### 开放式安全插件生态库

---

### 📦 插件目录

#### 官方核心插件

| 插件名称 | 版本 | 描述 | 维护状态 |
|---------|------|------|---------|
| [fingerprinter](plugins/official/fingerprinter) | 1.0.0 | CMS指纹识别引擎 | 官方维护 ✅ |
| [nmapper](plugins/official/nmapper) | 1.0.0 | Nmap端口扫描集成 | 官方维护 ✅ |
| [fofa_mapper](plugins/official/fofa_mapper) | 1.0.0 | FOFA数据采集器 | 官方维护 ✅ |
| [http_port_visitor](plugins/official/http_port_visitor) | 1.0.0 | Web服务信息采集 | 官方维护 ✅ |
| [company_investigator](plugins/official/company_investigator) | 1.0.0 | ICP备案信息收集 | 官方维护 ✅ |
| [domain_seeker](plugins/official/domain_seeker) | 1.0.0 | 子域名收集引擎 | 官方维护 ✅ |
| [nuclei_reactor](plugins/official/nuclei_reactor) | 1.0.0 | 漏洞检测框架 | 官方维护 ✅ |

#### 社区优质插件（精选）

| 插件名称 | 版本 | 描述 | 提交者 | 评分 |
|---------|------|------|--------|-----|
|XXXX| XXXX| XXXX |XXXX | ⭐⭐⭐⭐ |
| XXXX| XXXX| XXXX | XXXX| ⭐⭐⭐⭐ |
---

### 🛠️ 贡献指南

#### 提交新插件流程

1. **Fork仓库**  
   `点击右上角Fork按钮创建你的副本`

2. **创建插件分支**  
   ```bash
   git checkout -b feat/plugin-your-plugin-name
   ```

3. **遵循目录规范**  
```tree
plugins/
├── community/
│   └── your_plugin/
│       ├── config.ini
│       ├── help.json
│       ├── plugin.ini
│       ├── plugin.py
│       └── worker.py
└── official/
```

4. **提交PR**  
   描述插件功能、测试用例和兼容性说明

#### 代码规范要求

✅ 必须包含单元测试  
✅ 使用Python类型注解  
✅ 遵循PEP8代码风格  
✅ 提供清晰的文档注释  
✅ 声明依赖库及版本要求  

---



### 💬 社区支持

https://forum-shovel.hscsec.cn/

---

📌 法律声明：本工具仅限合法授权测试使用，开发者不对滥用行为负责<br> 
📧 商务合作：shovel@hscsec.cn | 🌐 官网：https://www.hscsec.cn


让我们一起打造更强大的Shovel插件生态！🚀
