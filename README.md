# PHP / Nginx / MySQL 本地开发环境

> 使用 **Docker Compose** 一键启动的轻量级 LEMP 开发栈，内置：
>
> * **Nginx** (Alpine 最新版)
> * **PHP‑FPM 8.0**
> * **MySQL 8.0**
>
> 开箱即用，适合快速原型开发和日常学习测试。

---

## 📂 项目目录结构

```text
.
├── docker-compose.yml        # 服务编排文件
├── nginx/                    # Nginx 配置目录（挂载到 /etc/nginx/conf.d）
│   └── default.conf          # 虚拟主机配置
├── php/                      # 代码目录（挂载到 /var/www/html）
│   ├── index.html            # 静态首页示例
│   ├── 1.php                 # PHP 测试脚本 1
│   └── 2.php                 # PHP 测试脚本 2
└── mysql/                    # MySQL 数据持久化卷（首次启动自动创建）
```

> **提示**：目录命名与 `docker-compose.yml` 中卷挂载保持一致，可自由增删文件。

---

## 🚀 快速开始

1. **克隆仓库**

   ```bash
   git clone YOUR_REPO_URL_HERE
   ```

2. **启动全部服务**

   ```bash
   docker compose up -d   # 第一次会自动拉取镜像
   ```


