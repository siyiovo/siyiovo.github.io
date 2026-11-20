# 双语机器人求职作品集实施计划

> **For agentic workers:** Use inline execution with `ub-mode`; complete each task and verify it before continuing.

**Goal:** 在 GitHub Pages 发布中文默认、可切换英文的 SLAM 与运动控制求职作品集。

**Architecture:** 使用 Hugo 静态生成和 Hugo Profile 起始模板。个人资料、双语项目内容和 UI 覆盖分别维护；GitHub Actions 构建并部署 Hugo 的 `public/` 目录。

**Tech Stack:** Hugo, Hugo Profile, Markdown, HTML/CSS, GitHub Actions.

## Global Constraints

- 中文为默认语言，英文版可直接访问，并提供可键盘操作的语言切换。
- 只将已确认的姓名、头像地址、邮箱、GitHub 主页和项目名作为个人事实。
- SLAM 内容必须标为示例；未知履历、技能、成果、数据和外链不得伪造。
- 简历文件未提供时不生成失效下载地址。
- 页面支持移动端、键盘焦点和减少动态效果偏好。
- GitHub Pages 构建须支持站点根路径和项目子路径。

---

### Task 1: 建立 Hugo Profile 项目

**Files:**
- Create: `hugo.yaml`
- Create: Hugo Profile theme files under `themes/hugo-profile/`
- Create: `.gitignore`
- Create: `README.md`

**Steps:**
- [x] 检查 Hugo 和 Go 可执行文件及版本；确认官方主题仓库的目录约定。
- [x] 获取 Hugo Profile 当前发布源码作为站点主题，不引入模板仓库的 Git 元数据。
- [x] 配置主题路径、站点标题、中文默认语言、英文语言、资源路径和主题版本说明。
- [x] 忽略 `public/`、Hugo 缓存和本机生成文件。
- [x] 写明本地构建、预览、添加项目和替换简历的操作。
- [x] 运行 Hugo 构建，确认空站点可以生成。

### Task 2: 建立双语内容与项目详情

**Files:**
- Create: `content/zh-cn/_index.md` and `content/en/_index.md`
- Create: `content/zh-cn/projects/` and `content/en/projects/` bilingual pages
- Create: `content/zh-cn/projects/slam-localization-demo/` bilingual example pages
- Create: language translation files and Hugo data/config for profile details
- Create: résumé resource placeholders only when a file is supplied

**Steps:**
- [x] 配置中文和英文的站点名称、导航、日期和语言切换标签。
- [x] 写入首页个人资料：姓名 Jinhua Deng、求职方向、邮箱、GitHub 主页和头像。
- [x] 建立 `agx-retargeting` 项目中英文详情页；只使用用户已给出的项目名，其余事实以清晰可编辑的提示字段呈现。
- [x] 建立明确标注为示例的 SLAM 定位项目页，不虚构量化结果、硬件、论文或仓库链接。
- [x] 验证语言切换能够返回对应项目页；无翻译对应页时回到目标语言首页。
- [x] 验证无简历文件时不渲染下载链接。

### Task 3: 定制工程作品集 UI

**Files:**
- Modify: Hugo Profile layouts and partials needed by the portfolio
- Create: `assets/css/portfolio.css` or the theme's established override location
- Create: local visual assets only when needed and available

**Steps:**
- [x] 应用 UI/UX Pro Max 为个人工程作品集检索得到的设计系统建议，并保留设计约束于主题覆盖样式。
- [x] 将首页层级调整为身份与方向、核心能力、精选项目、经历占位区、联系信息。
- [x] 为项目摘要和详情加入问题、职责、方案、验证结果、媒体与代码链接等清晰字段。
- [x] 保持浅色中性基底、多色强调、低装饰密度和稳定的内容宽度。
- [x] 实现窄屏导航、图片尺寸约束、可见焦点、对比度和 `prefers-reduced-motion`。
- [x] 确认头像加载失败时仍有可访问文本，未提供的作品图像不被伪造。

### Task 4: 配置 GitHub Pages 部署

**Files:**
- Create: `.github/workflows/hugo.yaml`

**Steps:**
- [x] 固定 Hugo 构建版本和 GitHub Actions 权限。
- [x] 配置官方 Pages artifact 构建与部署工作流。
- [x] 让 Hugo 使用 Pages action 提供的 base URL，避免资源路径在子目录部署时错误。
- [x] 本地检查 YAML、工作流触发条件、产物目录和权限。

### Task 5: 验证交付

**Files:**
- Verify: built output under `public/` (generated, ignored)
- Verify: rendered pages at desktop and mobile viewports

**Steps:**
- [x] 运行生产构建并检查中文首页、英文首页、项目详情页和资源路径。
- [x] 检查标题、描述、canonical/alternate language metadata 和链接目标。
- [x] 启动本地预览，用浏览器检查桌面与移动布局、语言切换、键盘操作及简历缺失状态。
- [x] 修复检查中发现的真实问题并重复对应验证。
- [x] 运行 `git rev-parse --is-inside-work-tree` 记录当前目录不是 Git 仓库；不创建仓库或提交记录。
