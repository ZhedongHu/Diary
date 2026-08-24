## 本README以及网站均由AI生成，但日记内容是我自己写的

# 我的日记仓库 · 美化版网站

这是一个纯前端静态网页，用于美化 [zhedonghu/Diary](https://github.com/zhedonghu/Diary) GitHub Pages 日记站点。

## 文件结构

```
diary-site/
├── index.html   # 主页面（首页 + 日记列表 + 关于 + 页脚）
├── styles.css   # 样式（支持明暗双主题）
├── app.js       # 应用逻辑（日记数据、弹窗、主题切换、粒子背景）
└── README.md    # 本文件
```

## 部署方式

将三个核心文件（`index.html`、`styles.css`、`app.js`）放置于仓库根目录，GitHub Pages 会自动以 `index.html` 作为入口。

## 添加新日记

编辑 `app.js`，在 `DIARY_ENTRIES` 数组中添加一条新记录：

```js
{
    date: '2026-08-15',          // ISO 格式日期，用于排序和时间计算
    displayDate: '2026 年 8 月 15 日', // 展示用日期
    title: '日记标题',
    subtitle: 'English Subtitle', // 可选
    preview: '摘要预览文本…',
    path: '2026/August-15/README', // 对应仓库中的 README 路径（不含 .md）
    tags: ['生活', '感悟']         // 可选标签
}
```

同时在仓库中创建对应的 `2026/August-15/README.md` 文件，写入日记正文（Markdown 格式）。网站会自动从 GitHub Pages 加载并渲染。

## 特性

- 🎨 **精美设计** — 暖色调日记风格，卡片式时间线布局
- 🌙 **明暗双主题** — 自动跟随系统偏好，支持手动切换
- ✨ **粒子背景** — 轻量 Canvas 粒子动画，低性能开销
- 📖 **弹窗阅读** — 点击日记卡片弹出详情，支持 Markdown 渲染
- 📱 **响应式** — 适配桌面 / 平板 / 手机
- ⚡ **纯静态** — 零依赖、零构建，直接部署即可
