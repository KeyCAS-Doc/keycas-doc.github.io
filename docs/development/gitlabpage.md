---
layout: default
title: 发布至Gitlab Page
parent: 开发者
nav_order: 4
---
# 编辑器
{: .no_toc }

一键发布至Gitlab page
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

{: .important }
> 哈哈嘿，全体目光向我看齐！我宣布个事儿！我是**！


## 发布至Gitlab Page

实际上这东西简单的出奇，编辑完成网站之后只需要点击publish，silex就会自动在把`website.json`里那一堆牛鬼蛇神的玩意转换成网站目录的同时自动给你生成一个Gitlab page。当然，前提是你的CI/CD可以用。对于官方的Gitlab.com来说，CI/CD必须要在完成支付和电话认证之后才能使用。这也就解释了为啥我一直没发现。

{: .warning }
> [CI/CD Pipelines](https://docs.gitlab.com/ee/ci/pipelines/) must be enabled to ensure the success of this operation

![GitlabPage](/assets/images/publish2gitlabpage.png)



## Demo site

https://silex-jeremyzxi-gitlab-io-jeremyzxi-fc87b9939fa889abe744b4d4292.gitlab.io/#