+++
title = "加入创作"
date = 2026-10-20T00:30:00.000
draft = false
summary = "本文说明加入创作的基本流程。"
ShowToc = true
ShowBreadCrumbs = true

[[author]]
name = "Zed Lee"
url = "/about/作者团队/#zed-lee"
+++

本文将说明加入创作的基本流程。



## 注册 GitHub 账号

使用邮箱注册 GitHub 账号即可，略。



## 加入成为仓库合作者

向 Zed Lee 发送您用于注册 GitHub 的邮箱，Zed Lee 将会向您发送合作者邀请，请在 GitHub 通知里即时接受邀请。



## 添加token

进入 GitHub 的 **Settings → Developer settings → Personal access tokens → Fine-grained tokens**，点击“Generate new token”。

![](create-token.jpg)

按以下配置填写：

- **Token name**：随便填，比如 `gog`
- **Expiration**：建议选 90 天，到期后重新生成一个替换即可（嫌麻烦也可以选择`No expiration`永不过期）
- **Repository access**：选 **Only select repositories**，然后选中 `gog`
- **Permissions**：点 **Add permissions**，找到 **Contents**，设为 **Read and write**

点击生成后，**立刻复制**那串以 `github_pat_` 开头的 token。页面关掉后就再也看不到了。

![](get-token.jpg)



## 登录

访问[摆烂诸神](https://zdleeeeee.github.io/gog/)，点击右上角“登录”。画面会提示登录方式，选择 `Sign In Using Access Token` 登录，然后粘贴刚才的 token 登录即可。

修改文章内容后，网站重新部署会需要等待两三分钟的时间才能看到更新，请耐心等待。

## 编辑教程

正文请使用 Markdown 语法书写，除此以外，您还可以使用一些 ZedPaper 实现的 Hugo Shortcodes。

### Markdown 语法教程

#### 开启下一个段落

开启下一个段落需要换行两次，比如：

```markdown
这是第一段。

这是第二段。

如果只换行一次，渲染出来的两段会合为一段。
比如这样。

段落内换行需要在换行前输入两个空格。  
比如这样。
```

{{< collapse summary="点击查看效果" >}}

这是第一段。

这是第二段。

如果只换行一次，渲染出来的两段会合为一段。
比如这样。

段落内换行需要在换行前输入两个空格。  
比如这样。

{{< /collapse >}}

#### 标题

```markdown
# 一级标题

（建议不要用一级标题，因为一级标题字号和文章标题一样大，会有些奇怪）

## 二级标题

同理你可以以此类推到六级标题，但建议只使用二级到四级标题。
```

#### 加粗、斜体、删除线、链接

```markdown
这是**加粗**；这是*斜体*；~~这是删除线~~

这是一条链接：[bilibili](www.bilibili.com "这是alt，鼠标悬停在链接时会显示")

这是一条相对链接：[博拉迪亚]({{%/* relref "/lore/westnor/博拉迪亚" */%}} "这是alt")
```

{{< collapse summary="点击查看效果" >}}

这是**加粗**；这是*斜体*；~~这是删除线~~

这是一条链接：[bilibili](www.bilibili.com "这是alt，鼠标悬停在链接时会显示")

这是一条相对链接：[博拉迪亚]({{%/* relref "/lore/westnor/博拉迪亚" */%}} "这是alt")

{{< /collapse >}}

#### 列表

```markdown
无序列表：

- 表项1
- 表项2
- 表项3

有序列表：

1. 表项1
2. 表项2
3. 表项3
```

{{< collapse summary="点击查看效果" >}}

无序列表：

- 表项1
- 表项2
- 表项3

有序列表：

1. 表项1
2. 表项2
3. 表项3

{{< /collapse >}}

#### 引用

```markdown
> 这是一条引用。
>
> 引用中也可以换行，但每行开头都需要“> ”
```

{{< collapse summary="点击查看效果" >}}

> 这是一条引用。
>
> 引用中也可以换行，但每行开头都需要“> ”

{{< /collapse >}}

```markdown
{{</* quote source="——Zed Lee[《加入创作》](/gog/about/加入创作)" */>}}

这是Shortcode版引用，source指定引用出处。

{{</* /quote */>}}
```

效果：

{{< quote source="——Zed Lee[《加入创作》](/gog/about/加入创作)" >}}

这是Shortcode版引用，source指定引用出处。

{{< /quote >}}
