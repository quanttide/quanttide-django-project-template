# 量潮Django项目模板

## 使用模板创建项目

```shell
django-admin startproject --template https://quanttide.coding.net/p/qtopen-django/d/django-project-template/git/archive/master.zip --name settings.yaml,Dockerfile <project_name> <local_directory> 
```

## 配置密钥

配置在`.secret.yaml`，格式和`settings.toml`相同。

## 本地调试

假设工作目录为当前目录

```shell
django-admin startproject --template . --name settings.yaml,Dockerfile django_example <example_project_dir>
```

## Docker Compose运行Django服务

主要用于模拟云端容器运行环境。常用于：
- 多租户等本地开发必须模拟云端环境的场景；
- 调试和修复容器配置。

### 环境变量

`.env`通过`.dockerignore`过滤，如果需要配置不太敏感的环境变量可以通过`docker-compose.yml`的`environment`配置项设置。
