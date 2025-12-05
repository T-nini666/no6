# 数据可视化交互网页 - 第6章示例

这是一个基于D3.js的交互式数据可视化网页项目，包含多种图表类型和轴脊控制功能。

## 功能特性

- 📊 多种图表类型：风速图、五边形、六边形、正弦余弦函数
- 🎛️ 轴脊控制：隐藏/显示轴脊、居中轴脊
- 🎨 统一的RdPu配色方案
- 📷 图片保存功能
- 📱 响应式设计

## 本地运行

1. 直接在浏览器中打开 `visualization.html` 文件
2. 或者使用本地服务器（推荐）：
   ```bash
   # 使用Python
   python -m http.server 8000
   
   # 使用Node.js
   npx http-server
   ```

## 部署到GitHub Pages

1. 确保你的仓库是公开的
2. 进入仓库的Settings页面
3. 找到Pages选项
4. 在Source中选择"Deploy from a branch"
5. 选择master分支和/(root)文件夹
6. 点击Save，等待几分钟后访问 `https://T-nini666.github.io/no6/`

## 文件结构

```
第6章交互网页初版/
├── visualization.html    # 主页面文件
├── 第6章.ipynb           # Jupyter Notebook文件
└── README.md            # 说明文档
```

## 技术栈

- HTML5
- CSS3 (Grid布局, Flexbox)
- JavaScript (ES6+)
- D3.js v7

## 使用说明

1. 选择图表类型进行切换
2. 对于风速图，可以修改24小时的风速数据
3. 使用轴脊控制功能调整图表显示
4. 点击"保存图片"导出当前图表

## 注意事项

- 需要网络连接以加载D3.js库
- 推荐使用现代浏览器（Chrome, Firefox, Safari, Edge）
- 本地文件协议运行时某些功能可能受限，建议使用HTTP服务器