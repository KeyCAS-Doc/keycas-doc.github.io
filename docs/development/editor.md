---
layout: default
title: 编辑器
parent: 开发者
---
# 编辑器
{: .no_toc }

如果您希望为本项目的无代码网页编辑器贡献内容或代码，请参阅此文档
{: .fs-6 .fw-300 }


<details open markdown="block">
  <summary>
    目录
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

---
## 相关链接

* [Silex meta repository](https://github.com/silexlabs/silex-meta)
* [Silex](https://github.com/silexlabs/Silex/)
* [Silex Doc](https://docs.silex.me/en/home)
* [KeyCAS](https://github.com/JeremyZXi/KeyCAS)
* [GrapesJS文档](https://grapesjs.com/docs/modules/Components.html)

## 如何添加新的组件
Silex允许我们通过配置文件`client-config.js`为编辑器添加新的组件和块。
组件和块的具体添加方式请参照[GrapesJS文档](https://grapesjs.com/docs/modules/Components.html)
```typescript
config.on('silex:startup:end', () => {
        const editor = config.getEditor()
        //whatever your block is
        }
```

## 如何添加新的插件
与组件类似，我们也可以通过配置文件`client-config.js`为编辑器添加新的GrapesJS插件

例如：

```typescript
import 'https://unpkg.com/grapesjs-navbar'
//....rest part of the config
config.on('silex:grapesjs:start', () => {
        const grapesjsNavbar = window['grapesjs-navbar']
        config.grapesJsConfig.plugins = [
            ...config.grapesJsConfig.plugins,
            'grapesjs-navbar',
        ]
    })
```

## 贡献代码

如果您希望为我们贡献代码，请遵循以下步骤

{: .warning }
> 注意，以下出现的所有`<>`并不是代码的一部分，它只是用来告诉您应该修改哪里，因此在您修改完成后请删除他们

{: .important }
> 以下操作默认您有安装Git以及Node.js

{: .note }
> [IntelliJ IDEA](https://www.jetbrains.com/idea/)为学生提供免费版本，推荐使用。


1. **分叉(Fork)项目**

在GitHub中打开[JeremyZXi/KeyCAS](https://github.com/JeremyZXi/KeyCAS)，点击右上角的`Fork`。这会想您的账户添加一份该项目的副本

2. **克隆项目**

您需要一个本地副本（通过命令行）

```bash
# 打开命令行工具/终端
# 进入您希望使用的路径（这步可省略）
cd <your-desired-working-directory>
git clone https://github.com/<您的用户名>/KeyCAS.git
```

3. **设置上游仓库**

请将[JeremyZXi/KeyCAS](https://github.com/JeremyZXi/KeyCAS)设置为上游仓库，以便您提交代码（执行pull request）

```bash
cd KeyCAS
git remote add upstream https://github.com/JeremyZXi/KeyCAS.git
```

4. **创建一个新的分支**

{: .note }
> 这步可以省略，但是保持分支是个好习惯

创建您的分支
```bash
git checkout -b <new-branch-name>
```
然后设置分支的上游仓库
```bash
git branch --set-upstream-to=dev <new-branch-name>
```
5. **安装依赖**

{: .warning }
> 请确保您的Node版本>=18

```bash
npm install
```

6. **修改**

在您完成修改或添加内容之后，您需要提交一个commit

{: .note }
> 如果您使用[IntelliJ IDEA](https://www.jetbrains.com/idea/)则可以使用其左上角的图形化界面提交

```bash
git commit -m "This is a short message about the change made in this commit"
```

7. **提交**

提交您的代码
```bash
git push origin <branch-name>
```

8. **Create a pull request**

[创建您的pull request](https://help.github.com/articles/creating-a-pull-request/)，请尽量确保标题简洁易懂
