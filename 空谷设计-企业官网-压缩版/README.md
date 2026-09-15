# 空谷设计 KONGGU DESIGN · 企业官网

酒店与康养空间设计企业官网（静态站点，纯 HTML/CSS/JS，无需构建）。

## 访问方式

- GitHub Pages：仓库 Settings → Pages → 选择分支 main → / (root) → Save
- 本地预览：直接双击打开 index.html

## 目录结构

```
├── index.html        # 首页（单页站点，黑金主题）
├── images/           # 图片资源（已压缩优化）
└── 使用说明.txt
```

## 技术说明

- Tailwind CSS（CDN）+ Google Fonts（CDN），需联网加载
- 所有图片路径为相对路径，支持部署到任意子路径
- 已添加 .nojekyll 以保证 GitHub Pages 直接托管
