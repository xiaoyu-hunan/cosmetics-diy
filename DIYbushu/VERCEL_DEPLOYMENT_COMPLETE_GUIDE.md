
# 🚀 Vercel部署完整指南

## 部署前检查清单

### ✅ 必要文件
- [ ] vercel.json (已优化)
- [ ] api/index.py (已优化)
- [ ] web_app.py (已检查)
- [ ] requirements.txt (已检查)
- [ ] cosmetics_diy.db (已检查)
- [ ] templates/ (已检查)
- [ ] .vercelignore (已创建)

### ✅ 配置优化
- [ ] 函数超时时间: 30秒
- [ ] 内存分配: 1024MB
- [ ] Python版本: 3.9
- [ ] 安全头设置: 已配置
- [ ] 环境变量: 已设置

## 部署步骤

### 方法1: Vercel CLI (推荐)
```bash
# 1. 安装Vercel CLI
npm install -g vercel

# 2. 登录Vercel
vercel login

# 3. 部署到预览环境
vercel

# 4. 部署到生产环境
vercel --prod
```

### 方法2: Vercel网站
1. 访问 https://vercel.com
2. 连接GitHub仓库
3. 选择项目根目录
4. 点击Deploy

## 部署后验证

### 1. 基本检查
- 访问部署URL
- 检查首页是否正常加载
- 测试搜索功能
- 验证API接口

### 2. 性能检查
- 页面加载时间 < 3秒
- API响应时间 < 1秒
- 数据库查询正常

### 3. 错误监控
- 查看Vercel控制台日志
- 监控函数执行状态
- 检查错误率

## 常见问题解决

### FUNCTION_INVOCATION_FAILED
- 检查Flask应用导入
- 验证数据库连接
- 查看详细错误日志

### FUNCTION_INVOCATION_TIMEOUT
- 优化数据库查询
- 减少响应数据
- 增加超时时间

### DEPLOYMENT_NOT_FOUND
- 检查vercel.json配置
- 验证API文件路径
- 重新部署

## 监控和维护

### 日常监控
- 检查部署状态
- 监控响应时间
- 查看错误日志

### 定期维护
- 更新依赖包
- 优化性能
- 备份数据

## 联系支持

如果遇到问题：
1. 查看Vercel控制台
2. 检查函数日志
3. 联系Vercel技术支持
