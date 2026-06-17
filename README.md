# 缓动函数过山车 🎢

> 在动画世界里，Timing is everything

一个交互式的缓动函数可视化工具，将枯燥的数学曲线转化为真实的物理体验。观察小车如何在不同"缓动函数"构建的坡道上加速、减速和反弹。

## ✨ 功能特点

- **物理模拟**：小车在轨道上的运动完美映射缓动函数的数学特性
- **丰富的缓动函数**：包含 Linear、Sine、Quad、Cubic、Quart、Quint、Expo、Circ、Back、Elastic、Bounce 等多种经典缓动函数
- **DIY 实验室**：编写你自己的缓动算法，实时预览效果
- **拖放排序**：拖动卡片调整顺序，方便对比不同缓动效果
- **全局控制**：一键启动/暂停所有轨道的动画
- **响应式设计**：适配各种屏幕尺寸

## 🚀 快速开始

### 前置条件

- Node.js (建议 18+)

### 运行项目

```bash
# 安装依赖
npm install

# 启动开发服务器
npm run dev

# 构建生产版本
npm run build

# 预览生产版本
npm run preview
```

## 🎨 技术栈

- **框架**：React 19 + TypeScript
- **构建工具**：Vite 6
- **样式**：Tailwind CSS
- **图标**：Lucide React

## 📁 项目结构

```
├── components/
│   ├── Hero.tsx          # 首页横幅
│   ├── CoasterTrack.tsx  # 标准缓动轨道组件
│   ├── CustomCoasterTrack.tsx  # 自定义轨道组件
│   └── CoasterCart.tsx   # 过山车小车组件
├── utils/
│   └── easings.ts        # 缓动函数定义
├── types.ts              # TypeScript 类型定义
├── App.tsx               # 主应用组件
├── index.tsx             # 入口文件
└── index.html            # HTML 模板
```

## 🧮 缓动函数说明

缓动函数本质是 **Time (t)** 到 **Progress (p)** 的映射。当 `t` 均匀增加时，`p` 的变化率决定了速度。

### 缓动函数分类

| 类别 | 函数 | 特点 |
|------|------|------|
| **Linear** | Linear | 匀速运动，无加速度 |
| **Sine** | EaseInSine, EaseOutSine, EaseInOutSine | 正弦曲线，平滑过渡 |
| **Quad** | EaseInQuad, EaseOutQuad, EaseInOutQuad | 二次方曲线 |
| **Cubic** | EaseInCubic, EaseOutCubic, EaseInOutCubic | 三次方曲线，更明显的加速感 |
| **Quart** | EaseInQuart, EaseOutQuart, EaseInOutQuart | 四次方曲线 |
| **Quint** | EaseInQuint, EaseOutQuint, EaseInOutQuint | 五次方曲线，极具戏剧性 |
| **Expo** | EaseInExpo, EaseOutExpo, EaseInOutExpo | 指数曲线，极速变化 |
| **Circ** | EaseInCirc, EaseOutCirc, EaseInOutCirc | 圆形曲线 |
| **Back** | EaseInBack, EaseOutBack, EaseInOutBack | 回拉效果，先退后再前进 |
| **Elastic** | EaseInElastic, EaseOutElastic, EaseInOutElastic | 弹性效果，橡皮筋般的回弹 |
| **Bounce** | EaseInBounce, EaseOutBounce, EaseInOutBounce | 弹跳效果，皮球落地 |

### 自定义缓动函数

在 DIY 实验室中，你可以编写自己的缓动算法：

```javascript
// 变量 t: 0 到 1 (时间)
// 返回值: 小车的水平位置 (通常 0 到 1，可以溢出)

const bounces = 4;
const decay = 3;

// 一个衰减的正弦波
return t + Math.sin(t * Math.PI * bounces) * 0.1 * Math.exp(-t * decay);
```

## 📝 License

MIT License

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！