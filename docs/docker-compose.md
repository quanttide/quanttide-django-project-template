# Docker Compose运行Django服务

主要用于模拟云端容器运行环境。常用于：
- 多租户等本地开发必须模拟云端环境的场景；
- 调试和修复容器配置。

## 环境变量

如果需要配置不太敏感的环境变量可以通过`docker-compose.yml`的`environment`配置项设置。
