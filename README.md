# 📊 数据可视化交互网页 - 第6章示例

一个基于D3.js的现代化交互式数据可视化网页项目，展示多种图表类型和丰富的交互功能。

## ✨ 功能特性

### 📈 多种图表类型
- **风速图** - 24小时风速变化曲线，支持数据编辑
- **五边形图** - 规则正五边形，支持轴脊居中
- **六边形图** - 规则正六边形，支持轴脊居中  
- **正弦余弦图** - 数学函数曲线展示，周期2π

### 🎛️ 轴脊控制系统
- **隐藏/显示轴脊** - 独立控制上、下、左、右四条轴脊
- **轴脊居中** - 将原点(0,0)移动到图形正中心
- **批量操作** - 一键切换所有轴脊显示状态

### 🎨 视觉设计
- **RdPu配色方案** - 统一的紫红色系配色
- **响应式布局** - 适配不同屏幕尺寸
- **现代化UI** - 毛玻璃效果、圆角设计、平滑动画

### 🛠️ 实用功能
- **实时数据编辑** - 风速数据支持在线修改
- **图表导出** - 一键保存为PNG图片
- **状态提示** - 操作反馈和错误提示
- **重置功能** - 快速恢复默认设置

## 🚀 快速开始

### 本地运行

1. **直接打开**
   ```bash
   # 双击 visualization.html 文件在浏览器中打开
   ```

2. **本地服务器（推荐）**
   ```bash
   # 使用Python
   python -m http.server 8000
   
   # 使用Node.js
   npx http-server
   
   # 使用PHP
   php -S localhost:8000
   ```
   然后访问 `http://localhost:8000/visualization.html`

### 在线部署

#### GitHub Pages 部署

1. **Fork或克隆此仓库**
   ```bash
   git clone https://github.com/T-nini666/no6.git
   cd no6
   ```

2. **推送到GitHub仓库**
   ```bash
   git add .
   git commit -m "部署数据可视化项目"
   git push origin main
   ```

3. **启用GitHub Pages**
   - 进入仓库Settings页面
   - 找到Pages选项
   - Source选择"Deploy from a branch"
   - 选择main分支和/(root)文件夹
   - 点击Save保存

4. **访问网站**
   - 等待2-10分钟部署完成
   - 访问 `https://[你的用户名].github.io/no6/`

#### 其他平台部署

项目为纯静态文件，支持部署到：
- **Netlify** - 拖拽文件夹即可部署
- **Vercel** - 导入GitHub仓库自动部署
- **Gitee Pages** - 国内访问速度更快
- **Coding Pages** - 腾讯云提供的静态网站服务

## 📁 项目结构

```
第6章交互网页初版/
├── visualization.html    # 主页面文件（包含所有HTML、CSS、JS）
├── 第6章.ipynb           # Jupyter Notebook原始文件
└── README.md            # 项目说明文档
```

## 🛠️ 技术栈

### 前端技术
- **HTML5** - 语义化标签和现代Web标准
- **CSS3** - Grid布局、Flexbox、动画效果
- **JavaScript ES6+** - 现代JavaScript语法
- **D3.js v7** - 数据驱动文档可视化库

### 设计特性
- **响应式设计** - 移动端友好
- **无障碍访问** - 语义化HTML结构
- **性能优化** - 按需加载和事件委托
- **跨浏览器兼容** - 支持现代浏览器

## 📖 使用指南

### 基本操作

1. **切换图表类型**
   - 点击顶部的图表类型按钮
   - 支持风速图、五边形、六边形、正弦余弦四种类型

2. **编辑风速数据**
   - 仅在风速图模式下显示数据编辑面板
   - 修改24小时的风速数值
   - 点击"更新数据"应用更改

3. **控制轴脊显示**
   - 点击对应按钮隐藏/显示单个轴脊
   - 使用"全部切换"批量控制
   - 支持轴脊居中功能（风速图除外）

4. **保存图表**
   - 点击右上角的"📷 保存图片"按钮
   - 自动下载为PNG格式
   - 文件名包含图表类型和时间戳

### 高级功能

#### 轴脊居中原理
- 将坐标原点(0,0)移动到图形中心
- 隐藏上轴脊和右轴脊以避免视觉干扰
- 适用于对称图形的展示

#### 颜色映射系统
- 使用D3.js的`interpolateRdPu`颜色插值器
- 根据数据值自动分配颜色深浅
- 保持视觉一致性和美观性

## 🔧 自定义配置

### 修改数据范围
在JavaScript代码中找到对应的数据域设置：

```javascript
// 风速图
.domain([0, 23])     // X轴：0-23小时
.domain([0, 25])     // Y轴：0-25 m/s

// 多边形图  
.domain([-10, 10])    // X轴和Y轴：-10到10

// 正弦余弦图
.domain([-2*π, 2*π]) // X轴：-2π到2π
.domain([-2, 2])      // Y轴：-2到2
```

### 修改配色方案
替换RdPu为其他D3.js内置的颜色插值器：

```javascript
// 其他颜色选项
d3.interpolateBlues     // 蓝色系
d3.interpolateGreens    // 绿色系
d3.interpolateOranges   // 橙色系
d3.interpolateReds      // 红色系
d3.interpolateViridis   // Viridis色谱
```

## 🐛 常见问题

### Q: 图表不显示或显示异常？
A: 检查以下几点：
1. 确保网络连接正常（需要加载D3.js）
2. 使用现代浏览器（Chrome、Firefox、Safari、Edge）
3. 清除浏览器缓存后重试
4. 检查浏览器控制台是否有错误信息

### Q: 保存图片功能不工作？
A: 可能的原因和解决方案：
1. 确保在HTTPS环境下运行（本地HTTP服务器即可）
2. 检查浏览器是否阻止了下载
3. 尝试刷新页面后重试

### Q: 移动端显示异常？
A: 项目已适配移动端，如果遇到问题：
1. 确保使用移动版浏览器
2. 尝试横屏显示
3. 检查网络连接状态

### Q: 如何添加新的图表类型？
A: 需要修改以下部分：
1. 在HTML中添加新的图表类型按钮
2. 在JavaScript中添加绘制函数
3. 更新`updateChart()`函数的逻辑
4. 添加相应的样式定义

## 🤝 贡献指南

欢迎提交Issue和Pull Request来改进项目！

### 开发环境设置
1. Fork本仓库
2. 创建功能分支：`git checkout -b feature/new-feature`
3. 提交更改：`git commit -am 'Add new feature'`
4. 推送分支：`git push origin feature/new-feature`
5. 提交Pull Request

### 代码规范
- 使用语义化的变量和函数名
- 添加适当的注释说明
- 保持代码格式统一
- 确保跨浏览器兼容性

## 📄 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情。

## 🙏 致谢

- [D3.js](https://d3js.org/) - 强大的数据可视化库
- [GitHub Pages](https://pages.github.com/) - 免费的静态网站托管服务
- [jsDelivr](https://www.jsdelivr.com/) - 快速的CDN服务

## 📞 联系方式

如有问题或建议，欢迎通过以下方式联系：
- 提交GitHub Issue
- 发送邮件至项目维护者
- 参与项目讨论区

---

**⭐ 如果这个项目对你有帮助，请给个Star支持一下！**