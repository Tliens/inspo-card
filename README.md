# 灵感卡片 InspoCard

把文字一键变成精美卡片的免费网页工具 — 受 iOS 应用「吉光卡片」启发的开源网页实现。

**在线使用：https://tliens.github.io/inspo-card/**

## 核心功能

- **10 套排版模板**：素笺 / 书摘 / 手帐 / 日签 / 竖排（含朱红印章）/ 暗夜 / 渐变玻璃 / 杂志 / 便利贴 / 极简
- **8 套配色**：宣纸、月白、青瓷、绯红、樱粉、苔绿、鎏金、黛夜
- **6 种字体**：宋体（Noto Serif SC）、楷体、毛笔楷（Ma Shan Zheng）、行书（Zhi Mang Xing）、硬笔（Long Cang）、黑体 — 中文字体按 unicode-range 分包懒加载，用到的字形才下载
- **自由排版**：字号 / 行距 / 字距 / 对齐 / 6 种比例（3:4、1:1、4:3、9:16、16:9、长图）
- **长图模式**：高度随文字量自动扩展，并可按 3:4 均匀切分批量导出，适合小红书 / 朋友圈多图发布
- **高清导出**：2× 超采样 PNG（3:4 输出 2160×2880），支持复制到剪贴板
- **中英双语**：`?lang=en` 深链；亮 / 暗 / 跟随系统主题
- **纯本地**：所有渲染在浏览器完成，文字不上传；草稿自动保存于本机

## 技术要点

- 单文件 `index.html`（≈66KB），零外部 JS 依赖，Canvas 2D 渲染
- 中文字体经 [fontsource](https://fontsource.org/)（jsDelivr CDN）按需分包加载
- 中英混排自动换行（CJK 按字断行、拉丁按词断行），超长文本自动缩字号 + 省略号截断
- SEO：canonical / hreflang / JSON-LD（WebApplication + FAQPage）/ sitemap / OG 图

## 本地运行

```bash
python3 -m http.server 8975
# 打开 http://localhost:8975/
```

## 说明

本项目与「吉光卡片」App 及其开发团队无任何关联。

## License

MIT
