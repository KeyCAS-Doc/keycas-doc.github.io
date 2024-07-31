---
layout: default
title: 编辑网站
nav_order: 3
---


## 创建网站

你可以选择从头开始，或者选择一个模版。

### 从头开始

从空白画布开始的就不多说了，应该都明白

{: .note }
>但是你，对就是你，写文档的时候可还是要写这一步的哦

### 选择模版

要选择模版的话，访问 https://gitlab.com/，使用你登录Silex所使用的账号登录。假设你希望使用[这个模版](https://gitlab.com/JeremyZXi/silex_JeremyZXi.gitlab.io)，你则需要访问https://gitlab.com/JeremyZXi/silex_JeremyZXi.gitlab.io 或搜索这个模版的名字`silex_JeremyZXi.gitlab.io`。进入这个库的首页然后点击右上角的`fork`。之后你可以选择将其设置为private或public

{: .important }
>可以随便修改名字，但是务必要确保其是以`silex_`开始。silex会且只会自动识别以`silex_`开始的库

成功后进入你的[KeyCAS editor](https://edit.keycas.cn/en/)应该就能看到你选择的模版显示在dashboard中了


## 发布网站

编辑完成后在编辑界面点publish。这时silex会报错（因为你的账号没有验证银行卡），不用担心，你的内容大概了已经成功的推送到gitlab仓库了

之后访问netlify，使用gitlab账户登录，选择对应gitlab仓库。记得在`Build setting`中把`Base directory`设置为public，否则netlify不会成功读取你的网站

{: .warning }
>如果你使用了gmail绑定到gitlab或者其他类似的东西，你的账户可能会被suspend。