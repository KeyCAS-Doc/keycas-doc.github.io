---
layout: default
title: 发布网站
nav_order: 7
---


## 发布网站

编辑完成后在编辑界面点publish。这时silex会报错（因为你的账号没有验证银行卡），不用担心，你的内容大概了已经成功的推送到gitlab仓库了

之后访问netlify，使用gitlab账户登录，选择对应gitlab仓库。记得在`Build setting`中把`Base directory`设置为public，否则netlify不会成功读取你的网站

{: .warning }
>如果你使用了gmail绑定到gitlab或者其他类似的东西，你的账户可能会被suspend。