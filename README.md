gh-pages 官方地址：https://github.com/tschaub/gh-pages

查看帮助命令：`npx gh-pages --help`

### 项目操作步骤：
1. 安装 gh-pages：
```npm install gh-pages --save-dev```
2. package.json 文件添加 deploy 脚本部分
```
    "scripts": {
        "deploy": "gh-pages -d dist"
    }
```
3. 运行下面命令：把 dist 文件夹里的内容，发布到 gh-pages 分支
```
npm run deploy
```
如果想查看 deploy 过程中的调试信息，运行下面命令：
```
NODE_DEBUG=gh-pages npm run deploy
```
4. 查看发布后的网站
``
