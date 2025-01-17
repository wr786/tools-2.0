# ASF-Tools2.0

## 介绍
ASOULFAN小工具前端仓库

## 环境需求

全局安装 `pnpm`

```
npm i -g pnpm
```

## 开发

1. 安装所有 node_modules

```
pnpm i
```

3. 将 `.env.example` 文件重命名为`.env.local`, 并按需修改其中配置

4. 启动开发服务器

```
pnpm dev
```

## 编辑器配置

`VS Code` 用户安装 `Vue Language Features (Volar)` 和 `eslint` 插件, 并禁用所有其他 `vue` 相关插件如 `vetur` 等。并将默认 `formatter` 改为 `ESLint`.

```json
{
  "editor.formatOnSave": true,
  
  "eslint.format.enable": true,
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact",
    "vue",
    "json"
  ],
  "[javascript]": {
    "editor.defaultFormatter": "dbaeumer.vscode-eslint",
  },
  "[javascriptreact]": {
    "editor.defaultFormatter": "dbaeumer.vscode-eslint",
  },
  "[typescript]": {
    "editor.defaultFormatter": "dbaeumer.vscode-eslint",
  },
  "[typescriptreact]": {
    "editor.defaultFormatter": "dbaeumer.vscode-eslint",
  },
  "[vue]": {
    "editor.defaultFormatter": "dbaeumer.vscode-eslint",
  },
  "[json]": {
    "editor.defaultFormatter": "dbaeumer.vscode-eslint",
  },
}
```

## 部署

### 普通部署

2. 构建

```
pnpm build
```

3. 预览

```
pnpm preview
```

### 部署到 Docker

1. 构建镜像

```sh
# 注意还有个点
docker build -t $NAME . 
```

2. 预览镜像

```sh
docker run -p 8080:80 $NAME
```



## Commit提交规范

### Header Header 部分只有 1 行，格式为 < type > : < subject >。

#### type 用于说明提交的类型： 

1. feat：增加**新页面**
2. style：只修改了**样式**，即不影响业务逻辑功能等
3. update :  更新修改代码逻辑，例如优化性能、 需求变更、修复bug等
4. doc :  更新文档相关

#### subject 用于说明提交内容：

1. 简要概括即可
2. 使用中文

#### subject 示例

update: XX页面更新某功能 （具体文字描述无硬性要求，简要概括即可）
