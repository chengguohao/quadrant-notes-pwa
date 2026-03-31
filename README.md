# 四象限记事 PWA  

一个简洁美观的四象限记事工具，支持闹钟提醒，可以安装到手机桌面。

## 📱 功能特性

- ✅ 四象限分类管理（重要紧急、重要不紧急、不重要紧急、不重要不紧急）
- ✅ 新增/编辑/删除记事
- ✅ 字符限制（每条最多1000字）
- ✅ 日期筛选（年月日选择）
- ✅ 关键词搜索
- ✅ 闹钟提醒（浏览器通知）
- ✅ 响应式设计，适配手机屏幕
- ✅ 单击编辑，双击全屏
- ✅ 历史记录导出（JSON格式）
- ✅ 离线缓存（Service Worker）
- ✅ PWA支持（可安装到桌面）

## 🚀 部署说明

### 必须上传的文件（4个）

以下4个文件**必须**上传到GitHub仓库：

1. **quadrant-notes.html** - 主应用文件
2. **manifest.json** - PWA清单文件
3. **service-worker.js** - Service Worker文件（离线缓存）
4. **icon.svg** - 应用图标

### 可选上传的文件

- **README.md** - 项目说明文件（本文件）
- **.gitignore** - Git忽略文件（可选）

### 本地其他文件（不需要上传）

以下文件在本地使用，但**不需要**上传到GitHub：

- `node_modules/` - 依赖包目录
- `.git/` - Git配置目录
- `.idea/` - IDE配置目录
- 其他开发工具生成的文件

## 📋 部署步骤

### 方法1：GitHub Pages（推荐，最简单）⭐

1. 在GitHub创建新仓库：`quadrant-notes-pwa`
2. 上传必须的4个文件：
   - quadrant-notes.html
   - manifest.json
   - service-worker.js
   - icon.svg
3. 进入仓库 **Settings** → **Pages**
4. 在 "Build and deployment" 中选择 "Deploy from a branch"
5. 选择分支：**main**
6. 点击 **Save**
7. 等待1-2分钟，GitHub会自动部署
8. 在Pages页面顶部会显示访问URL，如：`https://yourusername.github.io/quadrant-notes.html`

### 方法2：Netlify（自动化部署）⭐

1. 注册Netlify账号：[https://www.netlify.com](https://www.netlify.com)
2. 点击 "New site from Git"
3. 选择GitHub并授权
4. 选择 `quadrant-notes-pwa` 仓库
5. 点击 "Deploy site"
6. Netlify会自动部署，生成URL如：`https://random-name.netlify.app`

### 方法3：Vercel（自动化部署）⭐

1. 注册Vercel账号：[https://vercel.com](https://vercel.com)
2. 点击 "Add New Project"
3. 选择 "Continue with GitHub"
4. 选择 `quadrant-notes-pwa` 仓库
5. 点击 "Import"
6. Vercel会自动部署，生成URL如：`https://quadrant-notes.vercel.app`

## 📱 在手机上使用

### Android手机

1. 打开Chrome浏览器
2. 访问你的PWA URL
3. 浏览器会自动检测到PWA
4. 点击地址栏的"安装"图标
5. 或点击菜单 → "添加到主屏幕"

### iOS手机

1. 打开Safari浏览器
2. 访问你的PWA URL
3. 点击"分享"按钮
4. 选择"添加到主屏幕"

### 桌面浏览器

1. 打开Chrome/Edge浏览器
2. 访问你的PWA URL
3. 点击地址栏的"安装"图标

## 🔧 开发说明

### 文件结构

```
quadrant-notes-pwa/
├── quadrant-notes.html    # 主应用（必须上传）
├── manifest.json          # PWA清单（必须上传）
├── service-worker.js      # Service Worker（必须上传）
├── icon.svg              # 应用图标（必须上传）
├── README.md             # 项目说明（可选上传）
└── .gitignore           # Git忽略（可选）
```

### 本地开发

本地开发时，你会有其他文件（如node_modules、.git目录等），这些**不需要**上传到GitHub。GitHub Pages会自动从仓库根目录读取必须的4个文件。

## ⚙️ 配置说明

### manifest.json

- 定义应用名称、图标、主题色
- 配置PWA安装和显示模式
- 设置快捷方式

### service-worker.js

- 缓存HTML、manifest和图标文件
- 拦截网络请求，提供离线支持
- 清理旧缓存

### quadrant-notes.html

- 包含PWA meta标签
- 注册Service Worker
- 实现所有功能逻辑

## 🎯 优势

- ✅ 完全免费
- ✅ 无需配置服务器
- ✅ 自动HTTPS
- ✅ 全球CDN加速
- ✅ 自动部署
- ✅ 支持离线使用

## 📝 注意事项

1. **HTTPS要求**：PWA必须使用HTTPS协议才能安装到手机桌面，GitHub Pages自动提供HTTPS
2. **文件路径**：确保manifest.json中的路径正确（`/quadrant-notes.html`）
3. **Service Worker**：如果不上传service-worker.js，PWA仍可正常工作，只是没有离线缓存
4. **图标格式**：icon.svg必须是有效的SVG格式
5. **测试**：部署后在不同浏览器测试PWA功能

## 🚀 快速开始

1. 将4个必须文件上传到GitHub
2. 使用GitHub Pages启用（方法1）
3. 在手机浏览器访问部署后的URL
4. 安装到手机桌面
5. 开始使用！

## 🐛 调试工具

如果部署后页面无法正常显示，请使用调试工具：

### 访问调试页面
1. 在浏览器中访问：`https://yourusername.github.io/quadrant-notes-pwa/debug.html`
2. 调试页面会自动检查：
   - HTML文件是否存在
   - Service Worker是否正常
   - Manifest文件是否正确
   - 浏览器支持的功能

### 常见问题和解决方案

#### 问题1：只显示仓库名称，页面空白
**可能原因**：
- 浏览器缓存了旧版本
- GitHub Pages还在部署中
- JavaScript错误导致页面无法加载

**解决方案**：
1. **清除浏览器缓存**：
   - Chrome：Ctrl+Shift+Delete 或 设置→隐私和安全→清除浏览数据
   - Safari：设置→Safari→清除历史记录与网站数据
   - Firefox：Ctrl+Shift+Delete
2. **强制刷新页面**：Ctrl+F5
3. **等待部署完成**：GitHub Pages可能需要1-3分钟
4. **检查控制台错误**：按F12打开开发者工具，查看Console标签
5. **使用无痕模式**：避免缓存干扰

#### 问题2：Service Worker注册失败
**解决方案**：
1. 确保service-worker.js文件已上传
2. 检查文件路径是否正确
3. 清除浏览器缓存后重试

#### 问题3：图标不显示
**解决方案**：
1. 确保icon.svg文件已上传
2. 检查manifest.json中的图标路径
3. 清除浏览器缓存

#### 问题4：PWA无法安装
**解决方案**：
1. 确保使用HTTPS协议
2. 检查manifest.json是否正确
3. 清除浏览器缓存
4. 尝试使用无痕模式

## 📞 技术支持

- HTML5 + CSS3 + JavaScript
- PWA (Progressive Web App)
- Service Worker
- LocalStorage数据存储
- 响应式设计

---

**开始使用你的四象限记事PWA吧！** 🎉
