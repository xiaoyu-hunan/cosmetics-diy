# GitHub上传指南

## 准备工作

### 1. 安装Git
如果您的系统还没有安装Git，请先安装：

**Windows:**
- 访问 https://git-scm.com/download/win
- 下载并安装Git for Windows

**验证安装:**
```bash
git --version
```

### 2. 创建GitHub账户
- 访问 https://github.com
- 注册新账户或登录现有账户

## 上传项目到GitHub

### 方法一：使用GitHub Desktop（推荐新手）

1. **下载GitHub Desktop**
   - 访问 https://desktop.github.com
   - 下载并安装GitHub Desktop

2. **创建新仓库**
   - 打开GitHub Desktop
   - 点击 "Create a new repository on your hard drive"
   - 选择当前项目文件夹：`C:\Users\BOOK\OneDrive\桌面\DIYbushu`
   - 仓库名称：`cosmetics-diy`
   - 点击 "Create repository"

3. **发布到GitHub**
   - 在GitHub Desktop中点击 "Publish repository"
   - 选择 "Keep this code private" 或 "Make public"
   - 点击 "Publish repository"

### 方法二：使用命令行

1. **初始化Git仓库**
   ```bash
   cd "C:\Users\BOOK\OneDrive\桌面\DIYbushu"
   git init
   ```

2. **添加所有文件**
   ```bash
   git add .
   ```

3. **提交更改**
   ```bash
   git commit -m "Initial commit: Cosmetics DIY project"
   ```

4. **在GitHub上创建仓库**
   - 访问 https://github.com/new
   - 仓库名称：`cosmetics-diy`
   - 选择 "Public" 或 "Private"
   - 不要勾选 "Add a README file"
   - 点击 "Create repository"

5. **连接本地仓库到GitHub**
   ```bash
   git remote add origin https://github.com/你的用户名/cosmetics-diy.git
   git branch -M main
   git push -u origin main
   ```

### 方法三：使用GitHub网页界面

1. **创建新仓库**
   - 访问 https://github.com/new
   - 仓库名称：`cosmetics-diy`
   - 选择 "Public" 或 "Private"
   - 点击 "Create repository"

2. **上传文件**
   - 点击 "uploading an existing file"
   - 将项目文件夹中的所有文件拖拽到上传区域
   - 添加提交信息：`Initial commit: Cosmetics DIY project`
   - 点击 "Commit changes"

## 启用GitHub Pages

1. **进入仓库设置**
   - 在GitHub仓库页面，点击 "Settings" 标签

2. **配置Pages**
   - 在左侧菜单中找到 "Pages"
   - 在 "Source" 下选择 "GitHub Actions"

3. **自动部署**
   - 推送代码到main分支时，GitHub Actions会自动构建和部署
   - 部署完成后，访问 `https://你的用户名.github.io/cosmetics-diy`

## 部署到其他平台

### Vercel部署
1. 访问 https://vercel.com
2. 点击 "New Project"
3. 选择你的GitHub仓库
4. 点击 "Deploy"

### Heroku部署
1. 访问 https://heroku.com
2. 创建新应用
3. 连接GitHub仓库
4. 启用自动部署

## 常见问题

### Q: 如何更新代码？
A: 修改本地文件后，使用以下命令：
```bash
git add .
git commit -m "描述你的更改"
git push
```

### Q: 如何克隆仓库到其他电脑？
A: 使用以下命令：
```bash
git clone https://github.com/你的用户名/cosmetics-diy.git
```

### Q: 忘记GitHub密码怎么办？
A: 可以使用Personal Access Token替代密码，或重置密码。

## 下一步

项目上传到GitHub后，您可以：

1. **分享项目**：将GitHub链接分享给其他人
2. **协作开发**：邀请其他人参与项目开发
3. **部署应用**：使用GitHub Pages、Vercel等平台部署
4. **持续更新**：定期推送代码更新

## 技术支持

如果遇到问题，可以：
- 查看GitHub官方文档
- 在项目Issues中提问
- 搜索相关教程和解决方案
