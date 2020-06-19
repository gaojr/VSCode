# VSCode

Visual Studio Code 相关

## 安装方式

下载地址：[Download Visual Studio Code](https://code.visualstudio.com/download)

1. User Installer
   - 默认+官方推荐，只为当前用户安装，不需要管理员权限
2. System Installer
   - 为所有用户安装，需要管理员权限
3. .zip
   - 便携版，解压即可用
   - 不支持自动更新

## 文件路径（windows）

| 文件夹内容 | 安装版                             | 便携版                       |
| :--------: | :--------------------------------- | :--------------------------- |
|  用户数据  | %APPDATA%\\Code\\User              | `解压路径`\\data\\user-data  |
|    插件    | %USERPROFILE%\\.vscode\\extensions | `解压路径`\\data\\extensions |

## 设置、配置文件路径

- 快捷键 : `用户数据路径`\\keybindings.json
- 语言 : `用户数据路径`\\locale.json
- 设置 : `用户数据路径`\\settings.json
- eslint 忽略 : `用户数据路径`\\.eslintignore
- eslint 配置 : `用户数据路径`\\.eslintrc.json
- prettier 忽略 : `用户数据路径`\\.prettierignore
- prettier 配置 : `用户数据路径`\\.prettierrc.json

## 便携版

参考：[Portable Mode in Visual Studio Code](https://code.visualstudio.com/docs/editor/portable)

**注意** 便携版只支持 zip 解压的 vscode

### 使用便携版

1. 下载 VS Code 的 zip 包并解压
2. 在解压路径下创建 `data` 文件夹
3. 复制用户数据目录到 `data` ，并重命名为 `user-data`
4. 复制插件目录到 `data`
5. 在 `data` 下创建名为 `tmp` 的空文件夹

windows 下的目录结构：

```
|- 解压路径
|   |- Code.exe
|   |- data
|   |   |- user-data
|   |   |   |- ...
|   |   |- extensions
|   |   |   |- ...
|   |   |- tmp
|   |   |   |- ...
|   |- ...
```

### 更新便携版

将 `data` 文件夹复制到更新版本的 VS Code 解压路径下。

## prettier + eslint + typescript + stylelint

npm 安装：

```sh
npm i -g prettier
npm i -g eslint eslint-config-prettier eslint-plugin-prettier
npm i -g typescript @typescript-eslint/parser @typescript-eslint/eslint-plugin
npm i -g stylelint stylelint-order stylelint-config-recess-order stylelint-plugin-stylus stylelint-config-prettier stylelint-prettier
```

命令行使用：

```sh
# eslint 检测
eslint * --ext .ts,.js
# eslint 修复
eslint --fix * --ext .ts,.js
# stylelint 检测
stylelint *.css
# stylelint 修复
stylelint --fix *.css
# prettier 检测
prettier --list-different "**/*.{css,ts,js,json,md}"
# prettier 修复
prettier --write "**/*.{css,ts,js,json,md}"
```
