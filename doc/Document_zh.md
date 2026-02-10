# Liquid Theme 文档

[English](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document.md) • [中文](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_zh.md) • [Deutsch](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_de.md) • [Español](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_es.md) • [Français](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_fr.md)

## 目录结构

### Release 包

```bash
│  liquid-dark.css
│  liquid-ink-dark.css
│  liquid-ink.css
│  liquid.css
│  Demo.md
│  Document.md
│
└─liquid # 主题使用的字体文件
```

### 源代码

```bash
├─.github
│  └─workflows
├─dist # 组合后的 CSS 文件
├─font # 所有字体文件
├─media # Liquid Theme 预览图
└─src # 源代码
   ├─Deploy # 用于构建发布包的 Python 脚本
   └─liquid # CSS 组件
```



## 用法

### 添加自定义CSS（推荐）

这是最简单的自定义方式。

请参阅 <https://support.typora.io/Add-Custom-CSS/> 了解具体方法。

### 修改发布的CSS文件

首先将 Liquid Theme 安装到 PC 上，然后在主题文件夹中修改 `xxxxx.css` 文件。

### 修改项目的源代码

从 [Releases](https://github.com/ruiyangzhou01/Liquid/releases) 页面下载 `Source code (zip)`，然后修改 `src` 目录下的 CSS 文件。
