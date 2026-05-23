# 家庭菜谱看板 - 项目约定

## 产品概述

可视化家庭菜谱看板，支持菜谱浏览、详情查看、管理增删改。
定位：个人/家庭使用的轻量级菜谱管理工具。

## 技术栈

- 纯前端 HTML + CSS + JavaScript
- 单文件，无依赖
- localStorage 数据持久化
- 无后端（当前版本）

## 文件结构

```
recipes-board/
├── index.html      # 全部代码（HTML + CSS + JS）
├── CLAUDE.md       # 本文件
└── README.md       # 用户使用说明
```

## 开发约定

### CSS 命名（BEM）
```
模块__元素--修饰符
如：.recipe-card__title, .btn--primary
```

### CSS 变量
```
--color-*     色彩系统
--radius-*    圆角系统
--space-*     间距系统
```

### JavaScript
```
数据函数：loadRecipes(), saveRecipes()
渲染函数：renderRecipes(), renderAdminList()
操作函数：openDetail(), closeDetail(), openForm(), handleSubmit()
```

## 功能现状

| 功能 | 状态 | 说明 |
|------|------|------|
| 菜谱浏览 | ✅ 完成 | 网格卡片展示 |
| 菜谱详情 | ✅ 完成 | 弹窗展示 |
| 新增菜谱 | ✅ 完成 | 表单弹窗 |
| 编辑菜谱 | ✅ 完成 | 表单弹窗 |
| 删除菜谱 | ✅ 完成 | 管理面板 |
| 图片支持 | ⚠️ 有限 | 仅支持 URL，暂不支持本地上传 |
| 多设备同步 | ❌ 不可用 | 数据存在本地 localStorage |
| 响应式布局 | ✅ 完成 | 桌面/手机自适应 |

## 未来目标

### 优先级：高
- **多设备同步**：接入 Cloudflare Workers 或类似服务，实现多人数据共享
- **本地上传图片**：支持选择本地文件作为菜谱图片

### 优先级：中
- **搜索功能**：按菜名、标签搜索
- **分类管理**：自定义分类筛选
- **打印功能**：导出菜谱为可打印格式

### 优先级：低
- **国际化**：中英文切换
- **主题切换**：深色模式
- **数据导出**：JSON/CSV 导出备份

## 部署信息

- GitHub Pages: https://yiqianfan.github.io/Recipes-Board/
- 仓库: https://github.com/YiqianFan/Recipes-Board

## 更新日志

- 2026-05-23: v1.0 完成基础功能，部署到 GitHub Pages