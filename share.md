# 2021.12.31 技术分享

### 为什么要开发插件
1. 想要提升开发体验
2. 现有插件不能满足需求，你需要修改现有插件或写一个新的插件

### 为什么要开发 vscode 插件
免费开源，生态丰富，官方维护 前端友好


### vscode插件有哪些能力
太多了有空可以仔细阅读 [能力](https://code.visualstudio.com/api)

### 开发的大致步骤

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
可以但是不建议，1. 是因为插件具备的能力最好单一 2. 