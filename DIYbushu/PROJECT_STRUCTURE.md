# 项目结构说明

## 核心文件

```
cosmetics-diy/
├── web_app.py              # Flask Web应用主程序
├── extract_pdf_data.py     # 数据提取和数据库初始化脚本
├── wsgi.py                 # WSGI配置文件，用于生产环境部署
├── requirements.txt        # Python依赖包列表（开发环境）
├── requirements-prod.txt   # Python依赖包列表（生产环境）
├── README.md              # 项目说明文档
├── LICENSE                # MIT许可证
└── .gitignore             # Git忽略文件配置
```

## 部署配置文件

```
├── .github/
│   └── workflows/
│       └── deploy.yml     # GitHub Actions自动部署配置
├── vercel.json            # Vercel部署配置
├── Procfile               # Heroku部署配置
├── runtime.txt            # Python版本指定
├── Dockerfile             # Docker容器配置
├── docker-compose.yml     # Docker Compose配置
├── nginx.conf             # Nginx配置文件
└── gunicorn.conf.py       # Gunicorn服务器配置
```

## 模板文件

```
├── templates/             # HTML模板文件
│   ├── base.html         # 基础模板
│   ├── index.html        # 首页
│   ├── search.html       # 搜索页面
│   ├── product_detail.html # 产品详情页
│   ├── categories.html   # 分类页面
│   └── category.html     # 分类产品列表页
```

## 文档文件

```
├── DEPLOYMENT_GUIDE.md           # 部署指南
├── QUICK_START.md               # 快速开始指南
├── VERCEL_DEPLOYMENT_COMPLETE_GUIDE.md # Vercel部署完整指南
├── 让他人访问指南.md             # 网络访问指南
├── 部署完成总结.md               # 部署总结
└── 配方导入总结.md               # 配方导入总结
```

## API目录

```
├── api/                  # API相关文件（如果有）
```

## 部署方式

### 1. GitHub Pages
- 使用GitHub Actions自动部署
- 配置文件：`.github/workflows/deploy.yml`

### 2. Vercel
- 配置文件：`vercel.json`
- 支持Python Flask应用

### 3. Heroku
- 配置文件：`Procfile`、`runtime.txt`
- 使用Gunicorn作为WSGI服务器

### 4. Docker
- 配置文件：`Dockerfile`、`docker-compose.yml`
- 支持容器化部署

## 开发环境设置

1. 克隆仓库
2. 创建虚拟环境
3. 安装依赖：`pip install -r requirements.txt`
4. 初始化数据库：`python extract_pdf_data.py`
5. 启动应用：`python web_app.py`

## 生产环境部署

1. 安装生产依赖：`pip install -r requirements-prod.txt`
2. 使用Gunicorn启动：`gunicorn wsgi:app`
3. 或使用Docker：`docker-compose up -d`
