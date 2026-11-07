# MyBlog

基于 Django 开发的个人博客系统。

## 项目简介

MyBlog 是一个使用 Django 框架构建的个人博客项目，集成 DjangoUeditor 富文本编辑器，支持文章发布与管理，并可通过 uWSGI 部署上线。

## 技术栈

- **后端框架**：Django
- **富文本编辑器**：DjangoUeditor
- **部署**：uWSGI

## 项目结构

```
MyBlog/
├── DjangoUeditor/     # 富文本编辑器组件
├── blog/              # 博客核心应用
├── myblog/            # 项目配置目录
├── static/            # 静态资源文件
├── templates/         # HTML 模板
├── manage.py          # Django 管理脚本
├── requirements.txt   # 项目依赖
└── uwsgi.ini          # uWSGI 部署配置
```

## 快速开始

### 1. 克隆项目

```bash
git clone https://github.com/Gio-404/MyBlog.git
cd MyBlog
```

### 2. 安装依赖

```bash
pip install -r requirements.txt
```

### 3. 数据库迁移

```bash
python manage.py makemigrations
python manage.py migrate
```

### 4. 创建管理员账号

```bash
python manage.py createsuperuser
```

### 5. 启动开发服务器

```bash
python manage.py runserver
```

访问 http://127.0.0.1:8000/ 查看博客首页，访问 http://127.0.0.1:8000/admin/ 进入后台管理。

## 部署

项目包含 `uwsgi.ini` 配置文件，可使用 uWSGI 进行生产环境部署：

```bash
uwsgi --ini uwsgi.ini
```

建议配合 Nginx 作为反向代理使用。

## 功能特性

- 博客文章的发布、编辑与删除
- 富文本内容编辑（DjangoUeditor）
- 后台管理界面
- 静态资源管理
- uWSGI 部署支持

## 许可证

本项目未明确指定许可证，使用前请参考仓库中的相关说明。