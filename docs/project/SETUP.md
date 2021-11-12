# 项目设置

本文档描述了设置 `bpmn-js` 开发环境的必要步骤。

## TLDR;

在 Linux 上, OS X 或 Windows? [git](http://git-scm.com/), [NodeJS](nodejs.org) 和 [npm](https://www.npmjs.org/doc/cli/npm.html) 准备好？查看 [setup script section](https://github.com/bpmn-io/bpmn-js/blob/master/docs/project/SETUP.md#setup-via-script) 下面.


## 手动步骤

确保你有 [git](http://git-scm.com/), [NodeJS](nodejs.org) 和 [npm](https://www.npmjs.org/doc/cli/npm.html)  在继续之前安装.


### 获取项目 + 依赖项

以下项目来自 [bpmn-io](https://github.com/bpmn-io) GitHub 上的项目

* [bpmn-js](https://github.com/bpmn-io/bpmn-js)
* [diagram-js](https://github.com/bpmn-io/diagram-js)
* [bpmn-moddle](https://github.com/bpmn-io/bpmn-moddle)

并通过以下方式将它们克隆到一个公共目录中

```
git clone git@github.com:bpmn-io/bpmn-js.git
git clone git@github.com:bpmn-io/diagram-js.git
git clone git@github.com:bpmn-io/bpmn-moddle.git
```

### 链接项目

[Link dependent projects](https://docs.npmjs.com/cli/link) 彼此之间立即拿起变化.

```
.
├─bpmn-js
│   └─node_modules
│       ├─diagram-js <link>
│       └─bpmn-moddle <link>
├─diagram-js
├─bpmn-moddle
```

#### 在 OS X, Linux

使用 [npm-link](https://docs.npmjs.com/cli/link) or `ln -s <target> <link>`.

#### 在 Windows

使用 `mklink /d <link> <target>` [(docs)](http://technet.microsoft.com/en-us/library/cc753194.aspx).

### 安装依赖关系

执行 `npm install` 在每个项目上获取它们的依赖性.


### 确认一切正常.

执行 `npm run all` 在每个项目中。一切都会好起来的。


### 通过脚本设置

整个设置可以通过设置脚本自动化 [Linux/OS X](https://github.com/bpmn-io/bpmn-js/blob/master/docs/project/setup.sh) 和 [Windows](https://github.com/bpmn-io/bpmn-js/blob/master/docs/project/setup.bat).
