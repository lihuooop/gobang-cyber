# CYBER GOMOKU - 赛博朋克五子棋

一款融合赛博朋克美学风格的五子棋对战游戏，支持三个难度等级的 AI 对手。

## 特性

- :video_game: 经典五子棋玩法，15x15 标准棋盘
- :brain: 三种 AI 难度等级 - 简单、中等、困难
- :art: 赛博朋克主题设计 - 霓虹灯光、扫描线效果
- :arrows_counterclockwise: 悔棋功能 - 撤销你和 AI 的最后一步
- :sparkles: 胜利连线动画 - 五子连珠时高亮显示
- :art: 响应式布局 - 支持桌面和移动设备

## 使用方法

### 直接打开

下载 `index.html` 文件，在浏览器中直接打开即可开始游戏。

```bash
# 克隆仓库
git clone https://github.com/yourusername/gobang-cyber.git

# 进入目录
cd gobang-cyber

# 用浏览器打开 index.html
# Windows
start index.html
# macOS
open index.html
# Linux
xdg-open index.html
```

### 托管服务

将 `index.html` 部署到任何静态托管服务：

- GitHub Pages
- Vercel
- Netlify
- Cloudflare Pages

## 游戏操作

### 基本操作

1. **选择难度** - 点击 "简单"、"中等" 或 "困难" 按钮
2. **落子** - 点击棋盘上的空位放置棋子
3. **悔棋** - 点击 "悔棋" 按钮撤销最后一步
4. **重新开始** - 点击 "重新开始" 按钮重置游戏

### 游戏规则

- 玩家执黑棋先行，AI 执白棋
- 先在任意方向 (横/竖/斜) 连成五子者获胜
- 平局条件：棋盘下满且无人获胜

## AI 难度说明

| 难度 | 策略 | 特点 |
|------|------|------|
| 简单 | 70% 随机 + 30% 策略 | 适合新手练习 |
| 中等 | 全局位置评分 | 有一定挑战性 |
| 困难 | Minimax + Alpha-Beta 剪枝 | 需要认真应对 |

### AI 评分系统

AI 根据棋型威胁程度进行评分：

| 棋型 | 分数 |
|------|------|
| 五连 | 100000 |
| 活四 | 10000 |
| 冲四 | 1000 |
| 活三 | 500 |
| 眠三 | 100 |
| 活二 | 50 |
| 眠二 | 10 |
| 活一 | 2 |

## 技术实现

### 架构

- **单文件应用** - HTML + CSS + JavaScript 集成在单个文件
- **原生 JavaScript** - 无外部依赖
- **CSS 动画** - 使用 CSS 动画和 transitions
- **Google Fonts** - Orbitron (标题) + Share Tech Mono (正文)

### AI 算法

1. **候选位置筛选** - 仅评估有邻近棋子的位置
2. **多方向评估** - 检查水平、垂直、两个对角方向
3. **Minimax 搜索** - 困难模式使用深度优先搜索
4. **Alpha-Beta 剪枝** - 减少搜索树大小

### 视觉特效

- CRT 扫描线叠加效果
- 霓虹发光 (多层 box-shadow)
- 棋盘边框渐变呼吸动画
- 棋子弹入动画
- 胜利连线绘制动画

## 浏览器兼容性

| 浏览器 | 版本 |
|--------|------|
| Chrome | 80+ |
| Firefox | 75+ |
| Safari | 13+ |
| Edge | 80+ |

## 许可证

MIT License - 自由使用、修改和分发
