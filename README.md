# ChatGPT For Minecraft to China

为Minecraft服务器集成安全的ChatGPT功能，专为中国网络环境优化。

## 🚀 功能特性
- **安全代理**：内置Nginx反向代理，自动处理网络限制
- **数据隔离**：每位玩家独立加密数据库
- **多语言支持**：中英双语界面实时切换
- **审计追踪**：敏感操作实时告警与日志记录
- **权限管理**：细粒度权限控制体系

## 📦 安装指南
1. 将插件JAR文件放入 `plugins/` 目录
2. 重启服务器生成配置文件
3. 编辑 `config.yml` 配置代理和密钥策略
4. 按需配置 `proxies.yml` 自定义代理

## ⚙️ 配置说明
```
# 核心配置项
proxy:
  mode: plugin       # 代理模式 [plugin/none/custom]
  nginx: 
    port: 8443       # 代理监听端口

security:
  encryption: 
    algorithm: AES-256-GCM  # 加密算法
```
📜 指令手册
指令	权限	描述
/chatgpt ask	chatgpt.user.ask	向AI提问
/chatgptadmin reload	chatgpt.admin	重载配置
/chatgpt_emergency lock	chatgpt.emergency	紧急锁定

🔒 权限节点
chatgpt.user.base: true    # 默认开放基础功能
chatgpt.admin: op          # OP默认拥有管理权限
chatgpt.emergency: false   # 需手动授予紧急权限
🛠️ 开发者指南

# 克隆仓库
git clone https://github.com

# 构建项目
mvn clean package

# 依赖管理
```
<dependency>
  <groupId>com.squareup.okhttp3</groupId>
  <artifactId>okhttp</artifactId>
  <version>4.11.0</version>
</dependency>
```
📄 开源协议
本项目基于 MIT License 开源。详见 LICENSE 文件
