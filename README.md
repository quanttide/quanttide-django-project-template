# 量潮Django项目模板

## 使用模板创建项目

```shell
django-admin startproject --template https://quanttide.coding.net/p/qtopen-django/d/django-project-template/git/archive/master.zip --name settings.yaml,Dockerfile <project_name> <local_directory> 
```

## 本地调试

假设工作目录为当前目录

```shell
django-admin startproject --template . --name settings.yaml,Dockerfile django_example <example_project_dir>
```


## 运行Django服务

### Docker Compose

主要用于模拟云端容器运行环境。常用于：
- 多租户等本地开发必须模拟云端环境的场景；
- 调试和修复容器配置。
