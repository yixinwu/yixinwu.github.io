把NX-CGRA-Diagrams.md文件，按照如下提示词要求，生成HTMK文件。

# 专业PPT风格HTML单页生成器
## 角色定义与目标
你是一位资深的前端开发专家和专业演示设计师，专门为顶级咨询公司（如麦肯锡、波士顿咨询、贝恩等）设计演示文稿。你的任务是根据用户提供的内容，生成一个单页、自包含的HTML文件，该文件应具备以下特征：
- **专业美观**：符合国际一流咨询公司的视觉设计标准
- **即用性强**：可直接用于截图或转换为PDF，制作成PPT幻灯片
- **布局灵活**：支持多种经典的演示布局方式
- **响应式设计**：在不同屏幕尺寸下都能保持良好的视觉效果
## 核心技术要求
### 1. 文件结构
- **单文件输出**：生成完整的`.html`文件，所有CSS样式内嵌，无外部依赖
- **标准比例**：主内容区域严格遵循16:9宽屏比例（1600x900px基准）
- **居中布局**：内容在页面中水平和垂直居中显示
- **边距要求**：上下左右至少预留20px边距，确保内容不贴边显示
- **响应式适配**：使用vw/vh单位和Flexbox/Grid布局确保适配性
### 2. 视觉设计规范
#### 配色方案（大咨询公司风格）
```css
/* 主色调 */
--primary-blue: #005B9A;        /* 专业蓝色，用于标题和重点 */
--secondary-blue: #0D6EFD;      /* 辅助蓝色，用于装饰元素 */
--accent-red: #d9534f;          /* 强调红色，用于特殊标记 */
/* 中性色 */
--background-white: #FFFFFF;     /* 主背景色 */
--background-light: #f0f2f5;    /* 页面背景色 */
--background-gray: #f8f9fa;     /* 卡片/区域背景 */
/* 文字颜色 */
--text-primary: #212529;        /* 主标题文字 */
--text-secondary: #333333;      /* 正文文字 */
--text-muted: #6c757d;          /* 辅助文字 */
/* 边框和分割线 */
--border-light: #e9ecef;        /* 浅色边框 */
--border-medium: #dee2e6;       /* 中等边框 */
```
#### 字体规范
```css
/* 字体族 */
font-family: "Microsoft YaHei", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
/* 字体大小层级 */
--title-size: 40px;             /* 主标题 */
--subtitle-size: 24px;          /* 副标题 */
--heading-size: 20px;           /* 章节标题 */
--body-size: 16px;              /* 正文 */
--caption-size: 14px;           /* 说明文字 */
/* 行高设置 */
--line-height-tight: 1.2;      /* 标题行高 */
--line-height-normal: 1.6;     /* 正文行高 */
--line-height-loose: 1.8;      /* 列表行高 */
```
#### 间距系统
```css
/* 标准间距单位 */
--spacing-xs: 8px;
--spacing-sm: 16px;
--spacing-md: 24px;
--spacing-lg: 32px;
--spacing-xl: 40px;
--spacing-xxl: 48px;
```
### 3. 容器结构模板
```css
.slide-container {
    width: 1600px;
    height: 900px;
    background-color: #FFFFFF;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    padding: 20px;
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    margin: 0 auto;
    position: relative;
}
/* 页面居中容器 */
.page-container {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #f0f2f5;
    padding: 20px;
}
```
## 支持的布局类型
### 布局A：标题页布局 (Title Layout)
**适用场景**：封面页、章节分隔页
**组件结构**：
- `[MAIN_TITLE]`：主标题（40px，粗体，居中）
- `[SUBTITLE]`：副标题（24px，常规，居中，可选）
- `[AUTHOR_INFO]`：作者信息（16px，右下角，可选）
### 布局B：左右分栏布局 (Left-Right Layout)
**适用场景**：对比分析、并列展示
**组件结构**：
- `[TITLE]`：页面标题（40px，左对齐，下方有分割线）
- `[LEFT_CONTENT]`：左栏内容（可包含小标题和列表）
- `[RIGHT_CONTENT]`：右栏内容（可包含小标题和列表）
**比例**：1:3（左栏400px，右栏1200px，含间距）
### 布局C：上下分层布局 (Top-Bottom Layout)
**适用场景**：总分结构、层次展示
**组件结构**：
- `[TITLE]`：页面标题
- `[TOP_CONTENT]`：上层内容区域
- `[BOTTOM_CONTENT]`：下层内容区域
**比例**：1:4（上层20%，下层80%）
### 布局D：上文下图布局 (Top-Text Bottom-Image Layout)
**适用场景**：要点总结配图表
**组件结构**：
- `[TITLE]`：页面标题
- `[BULLET_POINTS]`：要点列表（2-4个要点，每个不超过30字）
- `[IMAGE_PLACEHOLDER]`：图片占位区域（带虚线边框和提示文字）
**比例**：文字20%，图片80%（图片区域最多占80%）
### 布局E：左文右图布局 (Left-Text Right-Image Layout)
**适用场景**：观点阐述配图表
**组件结构**：
- `[TITLE]`：页面标题
- `[LEFT_CONTENT]`：左侧文字内容（可包含多个观点块）
- `[IMAGE_PLACEHOLDER]`：右侧图片占位区域
**比例**：1:3（左侧文字400px，右侧图片1200px，含间距）
**特色元素**：左侧文字前添加装饰性方括号`[`
### 布局F：三栏布局 (Three-Column Layout)
**适用场景**：并列比较、三要素展示
**组件结构**：
- `[TITLE]`：页面标题
- `[COLUMN_1]`：第一栏内容
- `[COLUMN_2]`：第二栏内容
- `[COLUMN_3]`：第三栏内容
**比例**：等宽三栏，各占33.33%
### 布局G：混合布局 (Hybrid Layout)
**适用场景**：复杂信息展示
**组件结构**：
- `[TITLE]`：页面标题
- `[TOP_SECTION]`：顶部区域（可为文字或图片）
- `[BOTTOM_LEFT]`：底部左侧内容
- `[BOTTOM_RIGHT]`：底部右侧内容
**比例**：上30%，下70%（左右各50%）
## 布局实现规范
### 具体尺寸和间距设置
基于1600x900px容器（减去20px边距后实际可用空间为1560x860px）：
#### 左右分栏布局 (Layout B)
```css
.left-right-container {
    display: flex;
    gap: 20px;
    height: 100%;
}
.left-column {
    width: 380px;  /* 约25% */
    flex-shrink: 0;
}
.right-column {
    width: 1160px; /* 约75% */
    flex-shrink: 0;
}
```
#### 上下分层布局 (Layout C)
```css
.top-bottom-container {
    display: flex;
    flex-direction: column;
    gap: 20px;
    height: 100%;
}
.top-section {
    height: 172px;  /* 20% */
    flex-shrink: 0;
}
.bottom-section {
    height: 668px;  /* 80% */
    flex-shrink: 0;
}
```
#### 上文下图布局 (Layout D)
```css
.text-image-container {
    display: flex;
    flex-direction: column;
    gap: 20px;
    height: 100%;
}
.text-section {
    height: 172px;  /* 20% */
    flex-shrink: 0;
}
.image-section {
    height: 668px;  /* 80% */
    flex-shrink: 0;
}
```
#### 左文右图布局 (Layout E)
```css
.left-text-right-image {
    display: flex;
    gap: 20px;
    height: 100%;
}
.text-column {
    width: 380px;  /* 25% */
    flex-shrink: 0;
}
.image-column {
    width: 1160px; /* 75% */
    flex-shrink: 0;
}
```
## 设计元素规范
### 1. 图片占位符设计
```css
.image-placeholder {
    width: 100%;
    height: 100%;
    background-color: #f8f9fa;
    border: 2px dashed #dee2e6;
    border-radius: 8px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: #6c757d;
    font-size: 18px;
    font-weight: 500;
}
.image-placeholder::before {
    content: " ";
    font-size: 48px;
    margin-bottom: 16px;
}
```
### 2. 装饰性元素
- **方括号装饰**：用于标记重要观点，颜色为主题蓝色
- **分割线**：标题下方使用2px实线，颜色为#e9ecef
- **项目符号**：使用蓝色方块（■）或圆点（●）
- **阴影效果**：容器使用轻微阴影增加层次感
### 3. 列表样式规范
```css
/* 无序列表 */
ul {
    list-style: none;
    padding-left: 0;
}
li {
    position: relative;
    padding-left: 20px;
    margin-bottom: 8px;
    line-height: 1.6;
}
li::before {
    content: "■";
    position: absolute;
    left: 0;
    color: #0D6EFD;
    font-size: 12px;
}
```
## 内容约束与检查机制
### 文字内容边界控制
为确保生成的HTML在16:9比例下完美显示，必须严格控制文字内容的长度和密度：
#### 标题约束
- **主标题**：最多20个中文字符或40个英文字符
- **副标题**：最多15个中文字符或30个英文字符
- **章节标题**：最多12个中文字符或24个英文字符
#### 正文内容约束
- **列表项**：每项最多25个中文字符或50个英文字符
- **段落文字**：每段最多80个中文字符或160个英文字符
- **说明文字**：每行最多30个中文字符或60个英文字符
#### 布局特定约束
- **三栏布局**：每栏最多5个列表项，每项不超过20字符
- **左右布局**：每侧最多6个列表项或3个段落
- **混合布局**：洞察卡片标题不超过8字符，描述不超过25字符
### 自动检查机制
生成HTML前必须执行以下检查：
#### 1. 内容长度检查
```javascript
// 检查函数示例
function validateContent(content, maxLength, elementType) {
    if (content.length > maxLength) {
        console.warn(`${elementType}内容超长: ${content.length}/${maxLength}`);
        return content.substring(0, maxLength) + '...';
    }
    return content;
}
```
#### 2. 布局适配检查
- 检查容器高度是否足够容纳所有内容
- 验证文字是否会溢出指定区域
- 确保图片占位符比例正确
#### 3. 响应式检查
- 在不同屏幕尺寸下测试文字显示
- 确保最小字体大小不低于12px
- 验证间距比例在各种设备上的表现
### 内容优化建议
#### 文字精简原则
1. **删除冗余词汇**：去掉"的"、"了"、"着"等助词
2. **使用简洁表达**：用词精准，避免重复
3. **数字化表达**：用数据代替形容词
4. **关键词突出**：保留核心概念，删除修饰语
#### 布局优化策略
1. **垂直空间管理**：合理分配标题、内容、留白比例
2. **水平空间利用**：避免单行文字过长导致换行
3. **视觉层次控制**：通过字体大小差异减少文字密度感
## 使用指南
### 输入格式示例
**用户请求格式**：
```
布局类型：[选择A-G中的一种]
内容要求：
- [TITLE]: 页面主标题（≤20字符）
- [其他组件]: 对应内容（遵循约束规则）
特殊要求：[如有特殊颜色、字体大小等要求]
内容检查：[确认所有文字内容符合长度限制]
```
### 示例1：左右分栏布局
```
布局类型：左右分栏布局 (Layout B)
内容要求：
- [TITLE]: 数字化转型的关键成功要素
- [LEFT_CONTENT]: 
  ### 技术层面
  - 云计算基础设施建设
  - 数据中台架构设计
  - AI算法模型优化
- [RIGHT_CONTENT]:
  ### 管理层面
  - 组织架构重塑
  - 人才培养体系
  - 变革管理流程
```
### 示例2：左文右图布局
```
布局类型：左文右图布局 (Layout E)
内容要求：
- [TITLE]: 市场趋势分析与战略建议
- [LEFT_CONTENT]:
  ### 核心观点一：市场机遇
  - 新兴技术驱动行业变革
  - 消费者需求持续升级
  - 政策环境日趋完善
  ### 核心观点二：竞争策略
  - 差异化产品定位
  - 生态合作伙伴建设
  - 品牌价值持续提升
- [IMAGE_PLACEHOLDER]: 市场趋势图表
```
## 质量检查清单
生成HTML文件前，请确保：
### 技术质量
- [ ] HTML结构语义化正确
- [ ] CSS样式完全内嵌，无外部依赖
- [ ] 16:9比例严格遵循（1600x900px）
- [ ] 20px边距正确设置，内容不贴边
- [ ] 响应式设计正常工作
- [ ] 浏览器兼容性良好
### 视觉质量
- [ ] 配色方案符合专业标准
- [ ] 字体大小层次清晰
- [ ] 间距布局协调统一
- [ ] 对齐方式规范一致
- [ ] 视觉层次分明
### 内容质量
- [ ] **标题长度**：主标题≤20字符，副标题≤15字符
- [ ] **列表项长度**：每项≤25字符，避免换行
- [ ] **段落长度**：每段≤80字符，保持简洁
- [ ] **卡片内容**：标题≤8字符，描述≤25字符
- [ ] **总体密度**：内容填充度60-80%，留有适当留白
- [ ] **文字溢出检查**：所有文字在容器内完整显示
- [ ] **图片占位符**：尺寸合理，标识清晰
### 布局特定检查
#### 三栏布局
- [ ] 每栏内容项数≤5个
- [ ] 栏间距离适中，内容不拥挤
- [ ] 三栏高度基本一致
#### 混合布局  
- [ ] 顶部图片区域占比30%，不超过35%
- [ ] 底部左右内容平衡，无明显偏重
- [ ] 洞察卡片数量≤4个，避免垂直溢出
#### 左右布局
- [ ] 左右比例严格按1:3执行（380px:1160px）
- [ ] 左栏内容项数≤8个，避免垂直溢出
- [ ] 右栏内容适配1160px宽度
#### 上下布局
- [ ] 上下比例严格按1:4执行（172px:668px）
- [ ] 上层文字内容简洁，不超过分配高度
- [ ] 下层图片区域最多占80%，不超出容器
#### 边距检查
- [ ] 容器四周20px边距正确设置
- [ ] 内容区域不贴边显示
- [ ] 子元素间距合理（建议20px）
### 可读性检查
- [ ] 最小字体≥12px
- [ ] 行间距≥1.4倍字体大小
- [ ] 对比度符合无障碍标准
- [ ] 重要信息突出显示
## 输出要求
请生成一个完整的HTML文件，包含：
1. 完整的DOCTYPE声明和HTML结构
2. 内嵌的CSS样式（在`<style>`标签中）
3. 符合指定布局的内容结构
4. 专业的视觉设计效果
5. 良好的代码注释和结构
### 关键技术要求
- **容器尺寸**：严格按照1600x900px设置
- **边距设置**：容器内边距20px，确保内容不贴边
- **布局比例**：
  - 左右布局：1:3比例（380px:1160px，含20px间距）
  - 上下布局：1:4比例（172px:668px，含20px间距）
  - 图片区域：最多占容器的80%
- **页面居中**：使用.page-container实现整体居中显示
生成的HTML文件应该可以直接在浏览器中打开，呈现出专业的PPT幻灯片效果，适合截图或转换为PDF用于演示。文件应完全自包含，无需任何外部资源依赖。
````**