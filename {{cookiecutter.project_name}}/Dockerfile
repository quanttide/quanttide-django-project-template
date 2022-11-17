# ----- 拉取环境 -----
# 量潮Django镜像PostgreSQL版
FROM quanttide-docker.pkg.coding.net/qtopen-django/django-with-postgresql/django-with-postgresql:latest


# ----- 复制文件到镜像 -----

# 创建 code 文件夹并将其设置为工作目录
RUN mkdir /app
WORKDIR /app

# 将当前目录复制到容器的 code 目录
ADD .. /app/


# ----- 安装Python依赖 -----

# 可以在requirements.txt里设置Django等已打包依赖的版本覆盖镜像默认版本。
RUN pip install -r requirements.txt


# ----- 运行Django服务 -----

# 暴露端口
EXPOSE 8000
# 运行manage.py命令
CMD python3 manage.py makemigrations \
    && python3 manage.py migrate \
    && python3 manage.py createcachetable \
    && exec gunicorn {{ cookiecutter.project_name }}.wsgi:application --bind 0.0.0.0:8000