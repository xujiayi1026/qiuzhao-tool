<div align="center">

# 🔴 秋招投递工具台

**一个为秋招求职者设计的投递管理系统**

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)](#)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)](#)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)](#)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](#)

**🌐 在线体验 → [xujiayi1026.github.io/qiuzhao-tool](https://xujiayi1026.github.io/qiuzhao-tool/)**

*手机 / 电脑均可访问，无需安装、无需登录、数据本地存储*

</div>

---

## 📖 项目简介

秋招期间，投递记录分散在 Excel、备忘录、聊天记录里，状态更新不及时，容易错过笔试和面试。

**秋招投递工具台** 是一个纯前端单页应用，把所有投递记录集中管理：从投递、笔试、面试到 Offer，每一步进度一目了然。

> 🎯 **设计目标**：打开即用 · 零学习成本 · 手机友好 · 数据不丢失

---

## ✨ 功能特性

### 📊 数据看板
- 六项核心指标实时统计：总投递 / 待处理 / 笔试中 / 面试中 / 已 Offer / 已拒绝
- 数字变化带有递增动画，进度条按状态自动推进

### 📝 投递管理
- **新增 / 编辑 / 删除** 投递记录
- 记录字段：公司、岗位、类别、投递时间、状态、备注、岗位 JD
- **图片上传**：支持截图上传（如岗位 JD 截图、笔试通知），以 Base64 存储
- **岗位 JD 文本**：直接粘贴岗位描述，面试前随时回看

### 🏷️ 多维筛选
- **状态筛选**：全部 / 待处理 / 笔试 / 面试 / Offer / 拒绝
- **类别筛选**：互联网 / 快消 / 央国企 / 银行 / 其他
- **关键词搜索**：公司、岗位、类别、备注模糊匹配

### 💾 数据安全
- **本地存储**：数据保存在浏览器 localStorage，不上传任何服务器
- **导出备份**：一键导出 JSON 文件
- **导入恢复**：换设备 / 换浏览器时导入即恢复
- **自动种子数据**：首次打开自动填充示例记录

### 📱 移动端适配
- 表格自动转换为**卡片式布局**，手机阅读体验优秀
- 筛选按钮横向滑动，弹窗全屏宽度，按钮尺寸适合手指点击

---

## 🖼️ 界面预览

> 📌 截图占位：将截图放入 `screenshots/` 目录后取消下方注释

<!--
### 桌面端

![桌面端首页](screenshots/desktop-home.png)
![新增投递弹窗](screenshots/desktop-modal.png)

### 手机端

| 首页看板 | 记录卡片 | 筛选 |
|:---:|:---:|:---:|
| ![手机首页](screenshots/mobile-home.png) | ![手机卡片](screenshots/mobile-card.png) | ![手机筛选](screenshots/mobile-filter.png) |
-->

<table>
<tr>
<td width="33%" align="center"><b>🖥️ 桌面端</b><br><i>截图占位</i></td>
<td width="33%" align="center"><b>📱 手机端</b><br><i>截图占位</i></td>
<td width="33%" align="center"><b>✏️ 编辑弹窗</b><br><i>截图占位</i></td>
</tr>
<tr>
<td align="center">📊 六项统计 + 表格视图<br>状态 / 类别双筛选</td>
<td align="center">📇 卡片式布局<br>字段一目了然</td>
<td align="center">🖼️ 图片上传 + JD 粘贴<br>全字段编辑</td>
</tr>
</table>

---

## 🛠️ 技术方案

| 维度 | 方案 |
|------|------|
| 架构 | **单文件 HTML**（HTML + CSS + JS 全内联），零依赖、零构建 |
| 存储 | `localStorage`，Key：`autumnRecruitData`，JSON 序列化 |
| 图片 | `FileReader` 读取为 Base64 DataURL 直接存储 |
| 样式 | CSS 变量 + Grid/Flexbox + `@media` 响应式断点（768px / 380px） |
| 动画 | CSS Transition/Keyframes + 轻量 JS 数字递增动画 |

### 为什么选择单文件？

1. **可部署在任何静态托管**：GitHub Pages / Gitee Pages / 任意 Web 服务器
2. **可双击本地打开**：无网络也能使用
3. **代码可读性高**：一个文件讲完全部逻辑，适合面试时讲解

---

## 🚀 快速开始

### 方式一：在线访问（推荐）

直接打开 **[xujiayi1026.github.io/qiuzhao-tool](https://xujiayi1026.github.io/qiuzhao-tool/)**

### 方式二：本地运行

```bash
git clone https://github.com/xujiayi1026/qiuzhao-tool.git
cd qiuzhao-tool
```

双击 `index.html` 即可运行，或启动本地服务器：

```bash
python -m http.server 8000
# 访问 http://localhost:8000
```

---

## 📂 项目结构

```
qiuzhao-tool/
├── index.html      # 全部代码（结构 + 样式 + 逻辑）
├── README.md       # 项目说明
└── screenshots/    # 界面截图（待补充）
```

---

## 🔮 后续规划

- [ ] 数据云端同步（WebDAV / GitHub Gist）
- [ ] 面试倒计时提醒
- [ ] 投递漏斗转化分析图表
- [ ] 多端数据二维码互传
- [ ] 导出 Excel 格式

---

## 👤 关于作者

**秋招 PM 求职者** · 通过构建真实工具来打磨产品思维

- 🔗 本项目：[xujiayi1026/qiuzhao-tool](https://github.com/xujiayi1026/qiuzhao-tool)
- 💡 欢迎提 Issue 交流产品想法

---

<div align="center">
<sub>如果这个工具对你有帮助，欢迎 ⭐ Star 支持</sub>
</div>
