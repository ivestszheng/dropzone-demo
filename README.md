# Dropzone Upload

### 介绍

基于 [Dropzone.js](https://docs.dropzone.dev/) 实现的文件上传。

## 快速开始

由于使用了 ES 模块 (`import/export`)，需要通过 HTTP 服务器来访问页面，而不能直接双击 index.html 文件。推荐以下方法：

### 方法 1：使用 Nginx 服务器

1. 安装 Nginx 服务器。
2. 配置 Nginx 服务器，将项目存放至`nginx 安装目录/html/dropzone-demo`。
3. 启动 Nginx 服务器。
4. 在浏览器中访问 http://localhost/dropzone-demo。

### 方法 2：Python 内置服务器

```bash
# 在项目根目录执行
python -m http.server 8000
```

然后在浏览器中访问 http://localhost:8000

### 方法 3：VS Code Live Server 扩展

安装 VS Code 的 Live Server 扩展，然后在 index.html 文件上右键选择 "Open with Live Server"

## 自定义配置

默认使用 `https://httpbin.org/post`作为上传路径进行测试。可自定义`config.js` 中的参数，`config.js`默认参数如下：

```js
const config = {
  url: "https://httpbin.org/post",
  dictDefaultMessage:
    "拖放文件到这里或<span class='click-to-upload'>点击上传</span>",
  // headers: {
  //     'Authorization': 'Your Token'
  // }
};
```
