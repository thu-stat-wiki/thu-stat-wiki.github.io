!!! warning "施工中的条目"
    本版块内容仍在完善中，将在不久后形成稳定的版本。

为了方便你构思排版形式（^^如果你计划以网页方式发布的话^^），我们提供了以下快速引入来让你熟悉网页中的常用元素，以更好地呈现内容。更详细的技术内容可以参考 [Material for Mkdocs 的文档](https://squidfunk.github.io/mkdocs-material/)，排版建议可见相似网站的创作者指引，如  [OI WIki](https://oi-wiki.org/intro/format/) 和 [贵系](https://docs.net9.org/notes/editor/) 的文档。

!!! tip
    当然，必须说明的是： **^^不必太在意投稿的文档形式和格式，实用的内容才是本站的追求！^^** 我们欢迎任何形式的投稿，如果你需要的话我们也乐于为你提供内容呈现上的建议和帮助。

> 本页面中用像这样的 `引用模式` 标注的内容是提供给想要自己维护文档的创作者以及之后的 Wiki 维护者的信息，如果你只是在了解网页元素的话可以跳过。

## 页面排版元素

本节介绍一些有助于你合适地布置**单个页面**内容的排版元素，合适的版面元素能够让你<u>更好地传递自己的想法，并让帖子更利于阅读</u>。本站页面的排版结构基于对应的 markdown  `.md` 文件，其基本的文档元素，如标题、文字效果、列表、代码块、超链接、数学公式等，都与 markdown 的编辑方式相同；另外还有一些额外由主题扩展提供的文档元素也将在下面介绍，你可以简单了解后将合适的排版元素放在页面的合适位置。

如果你有一份想要变成网页内容的投稿但实在感到自己学不会或无法适应 markdown ，也可以联系我们寻求辅助（当然投稿最好别太长qwq）。

### 基础元素

这里有一些最为常用的 markdown 元素，更多基础元素可以在 [markdown 文档](https://markdown.com.cn/basic-syntax/) 查到。

-   **标题和目录**：合理地使用多级标题能够让文章层次更清晰，而且网站能够根据标题结构自动建立对应的目录，方便读者浏概览文章结构。具体实现上我们建议你使用 markdown 的 2 - 4 级标题[^二到四级标题]。

    ???+note "效果示例"

        <h2>二级标题</h2>
        <h3>三级标题</h3>

        > ```` text title="`.md` 对应代码"
        > ## 二级标题
        > ### 三级标题
        > ````
<!-- 由于只是一个示例，这里用 html 来避免生成目录 -->
-   **文字效果**：特殊文字效果能帮助你*标示重点* 或者 ~~用来抖机灵~~，一些常用的文字强调效果包括 粗体、斜体、下划线和删除线。

    ???+note "效果示例"

        **粗体** *斜体* ***粗斜体*** ^^下划线^^ ~~删除线~~

        > ```` text title="`.md` 对应代码"
        > **粗体** *斜体* ***粗斜体*** ^^下划线^^ ~~删除线~~
        > ````

-   **列表**：前面提到过，建议你使用 markdown 的 2 - 4 级标题，因为过多层级的标题反而让文章层次变得混乱，建议在合适的地方用有序列表或无序列表来列举。

    ???+note "效果示例"

        1. 京北大学
            - 数学系
            - 物理系
        2. 华清大学
            - 数学学院
            - 物理学院

        > ```` text title="`.md` 对应代码"
        > 1. 京北大学
        >     - 数学系
        >     - 物理系
        > 2. 华清大学
        >     - 数学学院
        >     - 物理学院
        > ````

-   **代码块**：代码块为你提供代码提供了良好的区域，通过设置代码块语言还能实现对应的语法高亮。

    ???+note "效果示例"
        -   行内代码块：

            灵活使用 `#!R apply()` 系列函数有助于你快速处理 `#!R data.frame` 。   
            
            > ```` text title="`.md` 对应代码"
            > 灵活使用 `#!R apply()` 系列函数有助于你快速处理 `#!R data.frame` 。
            > ````

        -   行间代码块:

            下面的代码展示了京北大学的校史：
            ``` R
            for(i in 1898:2023){
                print(paste("Kingpei Univ.", i))
            }
            ```

            > ```` text title="`.md` 对应代码"
            > 下面的代码展示了京北大学的校史：
            > ``` R
            > for(i in 1898:2023){
            >     print(paste("Kingpei Univ.", i))
            > }
            > ```
            > ````
            


- **超链接**：帮助你链接到站内其它文档（可以定位到指定章节处）或提供外部外部资源。

    ???+note "效果示例"
        欢迎 [统辅项目](http://www.stat.tsinghua.edu.cn/programs/undergraduate-programs/) 同学向我们 [投稿](../join/#_5) 。

        > ```` text title="`.md` 对应代码"
        > 欢迎 [统辅项目](http://www.stat.tsinghua.edu.cn/programs/undergraduate-programs/) 同学向我们 [投稿](../join/#_5) 。
        > ````
        > 章节位置的 hash 可以通过想要引用的章节标题右侧的 ¶ 按钮或所在的页面目录获得



- **脚注**：在你文内需要提供文献引用或是补充说明时可以使用脚注

    ???+note "效果示例"
        冷知识：华清大学的徽标是中国驰名商标[^驰名商标]

        
        > ```` text title="`.md` 对应代码"
        > 冷知识：华清大学的徽标是中国驰名商标[^驰名商标]
        > 
        > [^驰名商标]: [新闻页面存档](https://web.archive.org/web/20160407055712/http://www.tsinghua.edu.cn/publish/news/4205/2011/20110225231815390187460/20110225231815390187460_.html)
        > ````
        > 注：一般把脚注内容放在 `.md` 文件的末尾，方便维护




### 数学公式

统计很多地方都需要数学公式，markdown 中可以用 $\rm{\LaTeX}$ 语法渲染出数学公式[^数学公式渲染]，熟悉一些数学公式语法搭配上代码编辑器的自动补全能让你敲数学公式快得飞起，这项技能对于经常要和公式打交道的同学也比较实用。这里向大家提供一些学习 $\rm{\LaTeX}$ 语法的资源： [Mathjax 代码教程](https://oysz2016.github.io/post/8611e6fb.html), [LaTeX 学习文档](https://www.latexstudio.net/archives/tex-documents.html) 等。

!!! tip
    如非必要，最好不要在一个页面中包含太多数学公式，不然 MathJax 渲染会让网页变得很卡；可以将文档分拆成多个页面 [组织成多级目录](#_6) 来解决这个问题。

???+note "效果示例"
    容易得到 Score Function 具有性质 $\mathbb{E}_x[S(\theta;x )|\theta ]=0$，进一步我们可以推导 Fisher Information 的表达式：

    $$
    \begin{aligned}
        0=&\dfrac{\partial^{} }{\partial \theta'}\mathbb{E}_x[S(\theta ;x)|\theta  ]\\
        =&\int\dfrac{\partial^{} }{\partial \theta'} \left\{\dfrac{\partial^{} \ln f(\vec{x};\theta ) }{\partial \theta ^{}}  f(\vec{x};\theta )\right\}\,\mathrm{d}\vec{x}\\
        =&\int \left\{ \dfrac{\partial^{2} \ln  f(\vec{x};\theta )}{\partial \theta \partial \theta'} f(\vec{x};\theta )+\dfrac{\partial^{} \ln f(\vec{x};\theta )}{\partial \theta ^{}}   \dfrac{\partial^{}  f(\vec{x};\theta )}{\partial \theta'} \right\} \,\mathrm{d}\vec{x} \\
        =&\mathbb{E}\left( \dfrac{\partial^{2} \ln f(\vec{x};\theta )}{\partial \theta \partial \theta'}\right)+\mathbb{E}\left( \dfrac{\partial^{} \ln f(\vec{x};\theta )}{\partial \theta ^{}} \dfrac{\partial^{} \ln f(\vec{x};\theta )}{\partial \theta'} \right)\\
        \Rightarrow I(\theta )=& \mathbb{E}\left( \dfrac{\partial^{2} \ln f(\vec{x};\theta )}{\partial \theta \partial \theta'}\right)=-\mathbb{E}\left( \dfrac{\partial^{} \ln f(\vec{x};\theta )}{\partial \theta ^{}} \dfrac{\partial^{} \ln f(\vec{x};\theta )}{\partial \theta'} \right)
    \end{aligned}
    $$

    > ``` latex title="`.md` 对应代码"
    > 容易得到 Score Function 具有性质 $\mathbb{E}_x[S(\theta;x )]=0$，进一步我们可以推导 Fisher Information 的表达式：
    > 
    > $$
    > \begin{aligned}
    >     0=&\dfrac{\partial^{} }{\partial \theta'}\mathbb{E}_x[S(\theta ;x)|\theta  ]\\
    >     =&\int\dfrac{\partial^{} }{\partial \theta'} \left\{\dfrac{\partial^{} \ln f(\vec{x};\theta ) }{\partial \theta ^{}}  f(\vec{x};\theta )\right\}\,\mathrm{d}\vec{x}\\
    >     =&\int \left\{ \dfrac{\partial^{2} \ln  f(\vec{x};\theta )}{\partial \theta \partial \theta'} f(\vec{x};\theta )+\dfrac{\partial^{} \ln f(\vec{x};\theta )}{\partial \theta ^{}}   \dfrac{\partial^{}  f(\vec{x};\theta )}{\partial \theta'} \right\} \,\mathrm{d}\vec{x} \\
    >     =&\mathbb{E}\left( \dfrac{\partial^{2} \ln f(\vec{x};\theta )}{\partial \theta \partial \theta'}\right)+\mathbb{E}\left( \dfrac{\partial^{} \ln f(\vec{x};\theta )}{\partial \theta ^{}} \dfrac{\partial^{} \ln f(\vec{x};\theta )}{\partial \theta'} \right)\\
    >     \Rightarrow I(\theta )=& \mathbb{E}\left( \dfrac{\partial^{2} \ln f(\vec{x};\theta )}{\partial \theta \partial \theta'}\right)=-\mathbb{E}\left( \dfrac{\partial^{} \ln f(\vec{x};\theta )}{\partial \theta ^{}} \dfrac{\partial^{} \ln f(\vec{x};\theta )}{\partial \theta'} \right)
    > \end{aligned}
    > $$
    > ```

### 图片

用图片辅助你的行文能让文档内容更丰满或是脉络更清晰，markdown 也支持插入图片

???+note "效果示例"
    <center>
    <img src="../../assets/images/main/format/redfavicon.jpg" height="15%" width="15%">
    </center>

    > ```` text title="`.md` 对应代码"
    > <center>
    > <img src="../../assets/images/main/format/redfavicon.jpg" height="15%" width="15%">
    > </center>
    > ````
    

    > 注：markdown 有自带的图片语法 `![img-title](img-link)` ，但实际使用中为了调整适配的图片宽度，我们会用 html 标签控制

    > 注：关于文档引用的图片的路径，请存储到 `docs/assets/images` 下与文档相对 `/docs` 目录同名的文件夹中，并从本页面使用相对路径引用图片。例如本页面位置是 `/docs/main/format.md` ，上面这张图就放在了对应的 `/docs/assets/images/main/format/redfavicon.jpg` 处，在本文档中用相对路径 `../../assets/images/main/format/redfavicon.jpg` 引用。其它类型的附件也应以此方式存放。




### 折叠框

在一些你需要对正文进行补充，但又不希望打断现有行文思路的地方，可以用折叠框来插入你想补充的内容。折叠框展示有许多可选项，也支持不同属性的折叠框，可以在 [官方折叠框教程](https://squidfunk.github.io/mkdocs-material/reference/admonitions/) 中查到。

<style type="text/css">
a.pkuredlink:link{color: #94070A;}
a.pkuredlink:hover{color:#FF0000;}
</style>

???+note "效果示例"
    ???+note 
        为什么 THU Stat Wiki 的主题色不使用 <a href="https://vim.pku.edu.cn/cjwt/index.htm" class='pkuredlink' title='#94070A'>北大红</a> 呢？

    > 注：将加号 `+` 替换为空格 ` ` 可以让折叠框默认为收起状态；在 `???+note` 的 `note` 后加 `"<admonition title>"` 可以指定折叠框标题。    

    > ```` text title="`.md` 对应代码"
    > ???+note 
    >     为什么 THU Stat Wiki 的主题色不使用 <a href="https://vim.pku.edu.cn/cjwt/index.htm" class='pkuredlink' title='#94070A'>北大红</a> 呢？
    > ````
    


##  目录组织方式

如果你设想中的文档包含多个页面的话，可以将内容组织成一个多级目录，这将使得你的文档也以对应的页面集合呈现，一个目录结构的例子可以长这样：

``` yaml
./placement
└── abroad
    └── <name of your directory> # (1)!
        ├── index.md # (2)!
        ├── <your doc1>.md
        ├── <your doc2 directory> # (3)！
        │   ├── index.md
        │   ├── <your doc2-2>.md
        │   └── <your doc2-2>.md
        └── <your doc3>.md 
```


1.  从这一级开始就是你的投稿，你的文档被放置在 `./placement/abroad/` 下，对应着本站的 `保研出国-出国申请` 版块。
2.  `index.md` 对应的是你文档的封面页，你可以在里面概述你的文档内容或是做一个引子。
3.  如果确实需要的话，也可以有二级目录，但我们建议不要把文档目录搞得太复杂。


## 本地部署

如果你想在本地看看你的文档会长什么样，可以跟随以下指引或查询 [官方部署指引](https://squidfunk.github.io/mkdocs-material/getting-started/) 或 [贵系的部署指引](https://docs.net9.org/notes/editor/#_3)。

首先将 [本项目主仓库](https://github.com/thu-stat-wiki/thu-stat-wiki.github.io) 克隆到本地一个合适的地方 `<local-path>`（你也可以先将主仓库 Fork 到你的个人仓库中，然后选择从个人仓库克隆到本地）。

进入 `<local-path>` 根目录中，安装部署依赖的 `python` 库：

```
pip install mkdocs
pip install mkdocs-git-revision-date-localized-plugin
pip install mkdocs-material
```

随后运行：

```
mkdocs serve
```

然后会在命令行中看到类似输出信息：

```
INFO     -  Building documentation...
INFO     -  Cleaning site directory
INFO     -  Documentation built in 1.22 seconds
INFO     -  [02:40:01] Serving on http://127.0.0.1:8000/
```

这时网页已经在本地部署，打开浏览器，在地址栏访问 `http://127.0.0.1:8000/` 就能在本地浏览本站了。

如果想要添加自己的文档并浏览效果要注意：

- 把你的文档文件像 [目录组织方式](#_6) 一样放在正确的位置（附件存放方式在本页面前面 [图片](#_4) 部分有所说明）。
- 在 `<local-path>` 根目录下的 `mkdocs.yml` 中维护 `nav` 条目，这是网站的“地图”，决定了哪些页面以何种位置出现在站里，依葫芦画瓢在对应位置加上你的文件目录即可。

> 如果文档作者要变更文件路径，为了防止从其它地方引用（旧链接）时产生死链，需要维护 `_redirect.txt` 文件，加入 `<old-link> <new-link>` 来标示重定向关系。

然后你就可以在本地查看你的文档了！（喜）




[^驰名商标]: [华清大学徽标-新闻页面存档](https://web.archive.org/web/20160407055712/http://www.tsinghua.edu.cn/publish/news/4205/2011/20110225231815390187460/20110225231815390187460_.html) 。
[^二到四级标题]: 由于一些 remark-lint 问题，不要使用 1 级标题，而建议从 2 级开始。或者也可以说 1 级标题已经是你的页面标题了，所以它的内容当然应该从二级标题开始。
[^数学公式渲染]: 当然，markdown 中的公式渲染引擎 MathJax 与 $\rm{\LaTeX}$ 常用的引擎 xeLaTeX 或 PDFLaTeX 之类的并不一样，但基础语法是相同的。