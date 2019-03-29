gh-pages 官方地址：https://github.com/tschaub/gh-pages

查看帮助命令：`npx gh-pages --help`

### 项目操作步骤：
1. 安装 gh-pages：
```npm install gh-pages --save-dev```
2. package.json 文件添加 deploy 脚本部分（帮助命令中，选项信息：`-d, --dist <dist>        Base directory for all source files`）
```
    "scripts": {
        "deploy": "gh-pages -d dist"
    }
```
3. 运行下面命令：把 dist 文件夹里的内容，发布到 gh-pages 分支（此命令会：1. 自动创建 gh-pages 分支；2. 将 dist 文件夹下的内容`git add`到分支，然后依次运行：`git commit`、`git push`）
```
npm run deploy
```
如果想查看 deploy 过程中的调试信息，运行下面命令：
```
NODE_DEBUG=gh-pages npm run deploy
```
输出的调试信息，如下：
```
> gh-pages_demo@1.0.0 deploy /Users/chenag/Documents/WebstormProjects/gh-pages_demo
> gh-pages -d dist

GH-PAGES 67922: Cloning https://github.com/cag2050/gh-pages_demo.git into node_modules/gh-pages/.cache/github.com!cag2050!gh-pages_demo.git
GH-PAGES 67922: Cleaning
GH-PAGES 67922: Fetching origin
GH-PAGES 67922: Checking out origin/gh-pages
GH-PAGES 67922: Removing files
GH-PAGES 67922: Copying files
GH-PAGES 67922: Adding all
GH-PAGES 67922: Committing
GH-PAGES 67922: Pushing
Published
```
4. 查看发布后的网站：
https://cag2050.github.io/github_pages_demo/
