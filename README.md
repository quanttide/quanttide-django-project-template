# 量潮Django项目模板

量潮Django项目模板。
基于Python项目模板工具库[`cookiecutter`](https://cookiecutter.readthedocs.io/en/stable/index.html)制作，
参考其官方建议Django模板[`cookiecutter-django`](https://cookiecutter-django.readthedocs.io/en/latest/index.html)。

## Usage

### 使用cookiecutter模板创建项目

```shell
cookiecutter https://e.coding.net/quanttide/qtopen-django/django-project-template.git
```

### 配置Django密钥

在`.secret.yml`，格式和`settings.toml`相同。示例如下：

```yaml
# .secret.yml
default:
  SECRET_KEY: fake-secret-key
```

### 迁移数据模型

```shell
python manage.py migrate
```

项目根目录生成`db.sqlite3`。

### 运行Django服务

```shell
python manage.py runserver
```

## License

[Apache 2.0](LICENSE)
