# Google Search Console 提交指南

## ✅ 已完成部分

### 1. sitemap.xml
- 位置: `./toolhive/sitemap.xml`
- 已推送到 GitHub，Vercel 部署后会生效
- 包含17个URL：首页 + 16个工具页面

### 2. robots.txt
- 位置: `./toolhive/robots.txt`
- 已推送到 GitHub

---

## 📋 需要手动完成的步骤

由于当前网络环境无法访问 Google，请按以下步骤手动操作：

### 步骤1：访问 Google Search Console
1. 打开浏览器访问: https://search.google.com/search-console
2. 登录 Google 账号 (anxuanqi690@gmail.com)
3. 点击 "添加资源"

### 步骤2：添加网站属性
1. 选择 "网址前缀" 方式
2. 输入: `https://toolhive-two.vercel.app`
3. 点击 "继续"

### 步骤3：验证所有权（HTML 标签方式）
1. Google 会显示验证代码，类似:
   ```html
   <meta name="google-site-verification" content="XXXXXXXXXXXXXXXX" />
   ```
2. **复制这个 meta 标签**
3. 将其添加到 `./toolhive/index.html` 的 `<head>` 标签内（建议放在 description meta 标签之后）

### 步骤4：推送验证
```bash
cd toolhive
git add index.html
git commit -m "Add Google site verification meta tag"
git push
```

### 步骤5：等待部署
- 等待 Vercel 自动部署（约 1-2 分钟）
- 部署完成后回到 Google Search Console 点击 "验证"

### 步骤6：提交 sitemap
1. 验证成功后，左侧菜单点击 "站点地图"
2. 在 "添加站点地图" 输入框输入: `sitemap.xml`
3. 点击 "提交"

### 步骤7：请求索引
1. 使用 URL 检查工具检查首页
2. 点击 "请求编制索引"

---

## 📁 已创建的文件

| 文件 | 路径 | 状态 |
|------|------|------|
| sitemap.xml | ./toolhive/sitemap.xml | ✅ 已推送 |
| robots.txt | ./toolhive/robots.txt | ✅ 已推送 |

---

## 🔗 验证链接
- 网站首页: https://toolhive-two.vercel.app
- Sitemap: https://toolhive-two.vercel.app/sitemap.xml
- Robots: https://toolhive-two.vercel.app/robots.txt
