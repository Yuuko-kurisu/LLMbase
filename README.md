# 知识分享

## 修改流程

推荐使用 `pnpm` 包管理工具
1. 安装[node](https://nodejs.cn/download/)>=16.0.0
2. 使用 `npm install -g pnpm` 安装
3. 克隆本仓库代码 `https://github.com/hust-404/hust-404.github.io.git`
4. 运行`pnpm install` 初始化项目
5. 本地修改完成之后运行 `pnpm docs:dev`，确保没有问题再提交

## 添加图片

1. 在`public/assets/images`路径下存放图片文件，文件名示例*bytetransformer1.png*
2. 在md文档中添加图片，上下各空一行以正确显示图片标题

```plain
![alt name ](/assets/images/posts/2023-6/image.xxx "image title")
更多功能和问题请参考：

- [vuepress-theme-hope](https://theme-hope.vuejs.press/zh/guide/markdown/intro.html)
- [Markdown基本语法和示例](https://theme-hope.vuejs.press/zh/cookbook/markdown/)
- [Markdown增强语法](https://plugin-md-enhance.vuejs.press/zh/)
- [pnpm安装](https://pnpm.io/installation)

    - pnpm安装失败可以尝试手动安装
    ```
    curl -fsSL https://get.pnpm.io/install.sh | sh -
    ```

