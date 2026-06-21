# LaTeX 文档模板使用说明

基于 `book` 文档类的中文 LaTeX 模板，支持章节、公式、代码、图片、表格等常见排版需求。

## 特性

- **中文支持**：使用 `ctex` 宏包，提供楷书、宋体等中文字体
- **自定义封面**：支持图片封面（`cover.png`），自动生成标题、作者、日期信息
- **三级标题**：章（chapter）、节（section）、子节（subsection）、子子节（subsubsection）
- **数学公式**：集成 `amsmath`、`amssymb`，支持行内公式、独立公式、多行公式
- **代码排版**：使用 `listings` 宏包，预置 Python 代码样式
- **专业表格**：支持 `booktabs` 三线表、`tabularx` 自适应宽度表格
- **交叉引用**：对图表、公式、章节等进行标签引用
- **算法环境**：自定义可跨页的算法环境 `breakablealgorithm`
- **超链接**：使用 `hyperref` 支持网页、邮箱链接及 PDF 书签

## 前置要求

- TeX 发行版：TeX Live / MikTeX（推荐 XeLaTeX 编译）
- 编译器：**XeLaTeX**（最佳中文支持）

## 文件结构

```
├── main.tex        # 主文档（模板说明 + 使用示例）
├── cover.png       # 封面图片
├── main.pdf        # 编译输出示例
└── readme.md       # 本文件
```

## 编译方法

```bash
# 方式一：XeLaTeX（推荐）
xelatex main.tex
xelatex main.tex    # 第二次编译生成目录和交叉引用

# 方式二：latexmk（自动多次编译）
latexmk -xelatex main.tex
```

*首次编译需执行两次以确保目录（TOC）和交叉引用编号正确。*

## 模板内容概览

### 快速入门
- 文档结构与章节命令
- 字体样式（粗体、斜体、楷书、宋体）与字号
- 文字颜色（`xcolor` 宏包）
- 无序/有序列表
- 图片插入（单张与并排）
- 表格（基础表格与 `booktabs` 三线表）
- 代码块（`listings`，预置 Python 样式）
- 数学公式（行内公式 `$...$`、独立公式 `\[...\]`、`equation`、`align` 环境）
- 交叉引用（`\label` / `\ref` / `\eqref` / `\pageref`）
- 注释与特殊字符转义
- 间距调整

### 进阶功能
- 自定义命令（`\newcommand`）
- 文献引用（`\cite`）
- 超链接（`\href`、`\url`）
- 编译注意事项

## 页面设置

| 参数 | 值 |
|------|------|
| 纸张 | A4 |
| 上边距 | 25.4mm |
| 下边距 | 25.4mm |
| 左边距 | 20mm |
| 右边距 | 20mm |
| 页眉高 | 2.17cm |
| 页眉间距 | 4mm |

## 自定义封面

替换 `cover.png` 即可更换封面图片。标题、作者、日期在 `main.tex` 末尾的导言区设置：

```tex
\title{你的标题}
\author{你的名字}
\date{\today}
```

## 依赖宏包

ctex, amsmath, amssymb, graphicx, hyperref, listings, booktabs, tabularx, geometry, xcolor, titlesec, titletoc, fancyhdr, algorithm, algpseudocode, mathpazo, newpxtext, multirow, 等。

## 作者

yanbo
