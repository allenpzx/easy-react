# 2021.12.31 技术分享

### 为什么要开发插件
1. 想要提升开发体验
2. 现有插件不能满足需求，你需要修改现有插件或写一个新的插件

### 为什么要开发 vscode 插件
免费开源，生态丰富，官方维护 前端友好, 具备web和桌面双客户端


### vscode 插件有哪些能力
太多了有空可以仔细阅读 [能力](https://code.visualstudio.com/api)
### snippet 有哪些能力
[能力](https://code.visualstudio.com/docs/editor/userdefinedsnippets#_snippet-syntax)

### 开发

开始之前先 nvm install v14，先不这样也行，但是后续还是要安v14, 因为 vsce 需要

1. 安装 terminal 工具
```javascript
npm install -g yo generator-code
```
2. generate 一个模版
```javascript
yo code
```
模版选择

> New Extension (TypeScript) 标准ts模版
> 
> New Extension (JavaScript) 标准js模版
> 
> New Color Theme 主题模版
> 
> New Language Support 支持语言的模版
> 
> New Code Snippets 代码片段模版 => (本次选用的示例)
> 
> New Keymap
> 
> New Extension Pack
> 
> New Language Pack (Localization)
> 
> New Web Extension (TypeScript)
> 
> New Notebook Renderer (TypeScript)

模版选择了之后还可以拥有另外模版的能力吗？
可以但是**不建议**，1. 是因为插件具备的能力最好单一 2. 具备某种能力需要配套的设置，可能**（一定）**配错 3. 某些情况也可以直接下载被人的插件修改（比如theme）

开发...

[发布](https://code.visualstudio.com/api/working-with-extensions/publishing-extension)

1. 安装 vsce， 需要 node v14 及其以上的版本
```javascript
npm install -g vsce
```
2. 登录 vsce，`publisher name` 去 Azure 里面注册登录即可
```javascript
vsce login <publisher name>
```
3. 打包
```javascript
vsce package
```
4. 发包
```javascript
vsce publish
```
5. 更新包 [语义化版本规范](https://semver.org/lang/zh-CN/)
```javascript
vsce publish 2.0.1 ｜ vsce publish minor ｜ ...
```
6. 撤包
```javascript
vsce unpublish (publisher name).(extension name)
```