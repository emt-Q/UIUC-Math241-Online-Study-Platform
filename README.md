# UIUC Math241 Online Study Platform

> 面向 UIUC MATH241 (Calculus III) 的一站式在线学习网站，覆盖 Stewart *Calculus* 第 12–14 章全部知识点。

## 这是什么

一个单文件深色主题学习网站（`index.html`），把课本 12–14 章（向量与空间几何 / 向量函数 / 偏导数与多元微分）的全部知识点重新组织为 18 个小节，适合 AP Calculus BC 3 分水平的学生从头理解：

- **全知识点覆盖**：131 个知识框，MathJax 渲染 900+ 公式，含全部定义、定理、公式与例题
- **补全跳步**：课本中省略的推导步骤逐行补齐（如 12.4 三重积、13.3 曲率推导、14.4 全微分、14.8 拉格朗日乘数法）
- **前置知识**：函数图像性质、两点间距离公式、三角函数、极坐标、圆锥曲线等前置内容穿插在对应位置
- **中英术语对照**：18 节标题附原书英文标题，30+ 专有名词首次出现处标注英文（如 母线 generatrix / 准线 directrix / 马鞍状 saddle-shaped）
- **笔记与收藏**：每节可收藏（☆）与写笔记，保存在浏览器 localStorage
- **精选视频**：18 节共 21 条 YouTube 高赞讲解视频（3Blue1Brown、Professor Leonard、The Organic Chemistry Tutor 等），点击卡片新标签打开
- **交互式可视化**（7 个）：
  - 12.1 三维坐标系与球面（自研 Canvas 3D，可拖拽旋转）
  - 12.2 向量加法（自研 Canvas 3D）
  - 12.3 点积与投影（自研 Canvas 2D）
  - 12.6 **二次曲面交互式画廊**（伊利诺伊大学 NMD 项目，Three.js，6 种标准曲面 + 参数滑杆 + 平面切片）
  - 13.3 曲率演示（自研 Canvas 2D）
  - 14.6 梯度场（自研 Canvas 2D）
  - 14.8 拉格朗日乘数法（自研 Canvas 2D）

## 快速开始

直接双击打开 `index.html` 即可使用（无需服务器）。推荐配合 GitHub Pages 在线访问：

1. 打开仓库 **Settings → Pages**
2. **Build and deployment** → Source 选择 **Deploy from a branch**
3. Branch 选 `main`，目录选 `/ (root)`，保存
4. 等待 1–2 分钟后访问 `https://<你的用户名>.github.io/UIUC-Math241-Online-Study-Platform/`

## 目录结构

```
├── index.html              # 主网站（全部功能都在此单文件内）
├── quadrics_gallery/       # 伊利诺伊大学二次曲面画廊（本地镜像，iframe 引用）
│   ├── *.html              # Intro + 6 种二次曲面页面
│   ├── js/                 # Three.js 引擎与各曲面脚本（r79）
│   ├── css/                # 画廊样式与滑动条样式
│   └── static_images/      # 画廊插图
└── README.md
```

## 技术说明

- 纯前端单文件：HTML + CSS + JavaScript + MathJax（公式渲染，需联网）
- 笔记/收藏使用 `localStorage`（key: `calc_guide_favs_v1` / `calc_guide_notes_v1`），仅保存在当前浏览器
- 自研可视化基于 Canvas 2D/3D 正交投影引擎（`make3D` / `make2D`），无需任何库
- 二次曲面画廊为伊利诺伊大学 [NMD Quadric Surfaces](https://nmd.web.illinois.edu/quadrics/) 项目的本地镜像（Three.js r79），iframe 嵌入于 12.6 节

## 免责声明

本网站为个人学习用途，内容整理自 Stewart《Calculus》第 12–14 章；二次曲面画廊版权归伊利诺伊大学 NMD 项目所有；视频链接归各创作者所有。请勿用于商业用途。
