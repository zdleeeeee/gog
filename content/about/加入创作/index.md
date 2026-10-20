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

修改文章内容后，网站会重新部署，需要两三分钟后才能看到更新，请耐心等待。

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

#### 加粗、斜体、删除线、高亮

```markdown
这是**加粗**；这是*斜体*；~~这是删除线~~；这是==高亮==
```

{{< collapse summary="点击查看效果" >}}

这是**加粗**；这是*斜体*；~~这是删除线~~；这是==高亮==

{{< /collapse >}}

#### 链接

```markdown
这是一条链接：[bilibili](https://www.bilibili.com/ "这是title，鼠标悬停在链接时会显示，注意连接开头必须写清除协议，也就是https://")

这是一条相对链接：[博拉迪亚](/lore/westnor/博拉迪亚 "这是title")
```

{{< collapse summary="点击查看效果" >}}

这是一条链接：[bilibili](https://www.bilibili.com/ "这是alt，鼠标悬停在链接时会显示，注意连接开头必须写清除协议，也就是https://")

这是一条相对链接：[博拉迪亚](/gog/lore/westnor/博拉迪亚 "这是alt")

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

> 这是一条引用。
>
> 引用中也可以换行，但每行开头都需要“> ”

```markdown
{{</* quote source="——Zed Lee[《加入创作》](/about/加入创作/)" */>}}

这是Shortcode版引用，source指定引用出处。

{{</* /quote */>}}
```

效果：

{{< quote source="——Zed Lee[《加入创作》](/about/加入创作/)" >}}

这是Shortcode版引用，source指定引用出处。

{{< /quote >}}

#### 图片

**上传图片与填写路径**

在后台媒体库中先进入/创建当前文章的图片文件夹，再上传图片。比如本文的图片放在 `关于 → 加入创作` 中；优玛的图片放在 `设定 → westnor → 优玛` 中。不要直接上传到栏目根目录，以免不同文章的图片混在一起。

本地编辑时，直接把图片放到文章的 `index.md` 同目录即可。例如：

```text
content/about/加入创作/
├─ index.md
├─ create-token.jpg
└─ get-token.jpg
```

同目录图片可以直接写文件名，比如 `create-token.jpg`。

==**注意：图片名只能使用英文字符，不要使用中文！**==

**Markdown 图片**

图片的写法比普通链接多一个开头的感叹号：

```markdown
![GitHub 创建 Token 的设置页面](create-token.jpg)

![GitHub 创建 Token 的设置页面](create-token.jpg "创建前请检查仓库权限")
```

方括号里的文字是 `alt`，即图片的替代文字，用来描述画面内容，供屏幕阅读器读取，也可在图片加载失败时提供说明。它不是图片下方的说明文字。圆括号中可选的引号文字是 `title`，通常在鼠标悬停时显示，触屏设备上不方便查看，所以重要说明请直接写在正文中。

{{< collapse summary="点击查看图片效果" >}}

![GitHub 创建 Token 的设置页面](create-token.jpg "创建前请检查仓库权限")

{{< /collapse >}}

使用外部图片时，填写完整地址：

```markdown
![图片内容的描述](https://example.com/image.jpg)
```

上面的地址仅用于说明写法，请替换成实际图片地址。长期使用的插图建议上传到文章目录，避免原网站删除图片后失效。

**设置宽度、居中和图片说明**

需要指定宽度、居中，或在图片下面显示标题与来源时，可以使用 `figure`：

```markdown
{{</* figure
  src="create-token.jpg"
  alt="GitHub 创建 Token 的设置页面"
  width="320"
  align="center"
  title="创建 Token"
  caption="填写前请确认仓库和权限选项。"
  link="create-token.jpg"
*/>}}
```

效果：

{{< figure src="create-token.jpg" alt="GitHub 创建 Token 的设置页面" width="320" align="center" title="创建 Token" caption="填写前请确认仓库和权限选项。" link="create-token.jpg" >}}

| 参数 | 作用 |
| --- | --- |
| `src` | 图片路径，必填。 |
| `alt` | 描述图片内容的替代文字。 |
| `width` | 目标宽度，单位为像素，只写数字。容器不够宽时，图片会按比例缩小。 |
| `align="center"` | 图片居中。 |
| `title` | 在本主题的 `figure` 中，是图片下方的可见标题，不是鼠标悬停提示。 |
| `caption` | 图片下方的说明，支持 Markdown。 |
| `link` | 点击图片时打开的地址；与 `src` 相同即可查看原图。 |

只需填写用到的参数，其余可以省略。通常设置 `width` 即可，高度会自动按图片比例调整。`figure` 是单独使用的 shortcode，不需要再写结束标签。

**标注图片作者或来源**

`attr` 用于写作者或来源，`attrlink` 为这段署名添加外部链接：

```markdown
{{</* figure src="插图.jpg" alt="插图内容的描述" attr="作者名字" attrlink="https://example.com/" */>}}
```

如果要链接本站的作者团队页，使用 `attrref`，它会自动处理本地与远程部署路径：

```markdown
{{</* figure src="插图.jpg" alt="插图内容的描述" attr="Zed Lee" attrref="/about/作者团队/#zed-lee" */>}}
```

这里的 `插图.jpg` 是示例文件名，请替换为已上传的图片。`attrref` 已经负责解析站内引用。若同时写 `caption` 和 `attr`，可以在 `caption` 末尾加一个空格，让说明和署名之间留有间隔。

#### 对话气泡

`message` 可以把一段文字显示成聊天气泡，适合人物对话、书信片段或创作说明。正文仍按 Markdown 书写，可以加粗、分段或使用列表。

```markdown
{{</* message name="创作者" */>}}
我想写一个发生在优玛的故事。  
少年采诗官陆轲来到蒙特利亚完成他的壮游仪式。
{{</* /message */>}}

{{</* message name="Zed Lee" align="right" */>}}
期待ing！
{{</* /message */>}}
```

{{< collapse summary="点击查看对话气泡效果" >}}

{{< message name="创作者" >}}
我想写一个发生在优玛的故事。  
少年采诗官陆轲来到蒙特利亚完成他的壮游仪式。
{{< /message >}}

{{< message name="Zed Lee" align="right" >}}
期待ing！
{{< /message >}}

{{< /collapse >}}

每条消息需要自己的开始标签和结束标签 `{{</* /message */>}}`。默认靠左，`align="right"` 会让整条消息靠右。

**头像与颜色**

所有参数都可以省略。不填头像就只显示气泡，不填名字就不显示姓名。默认颜色会跟随主题的深浅色模式，通常不需要手动设置。

| 参数 | 作用 |
| --- | --- |
| `name` | 显示的说话者姓名。 |
| `avatar` | 头像图片地址；同目录图片直接填写文件名。 |
| `align="right"` | 将头像和气泡放到右侧；省略时靠左。 |
| `nameColor` | 姓名颜色，默认使用 `var(--secondary)`。 |
| `background` | 气泡背景色，默认使用 `var(--code-bg)`。collapse组件内默认使用`var(--entry)` |
| `textColor` | 正文颜色，默认使用 `var(--content)`。 |

如果需要自定义，可以这样写：

```markdown
{{</* message name="旅人" avatar="Traveller.jpg" align="left" nameColor="#34a458" background="#b2b2b240" textColor="var(--content)" */>}}
今晚的渡船还会来吗？
{{</* /message */>}}
```

这里的 `avatar.jpg` 是示例文件名，使用前请先上传自己的头像图片，或直接省略 `avatar`。参数名区分大小写，`nameColor` 和 `textColor` 要按示例书写。自定义颜色后，建议分别在浅色和深色模式下检查文字是否清晰。

{{< message name="旅人" avatar="Traveller.jpg" align="left" nameColor="#34a458" background="#b2b2b240" textColor="var(--content)" >}}

今晚的渡船还会来吗？

{{< /message >}}

颜色代码查询网站：[HTML Color Codes](https://htmlcolorcodes.com/)
