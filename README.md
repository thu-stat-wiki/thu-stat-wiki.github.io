# thu-stat-wiki.github.io

Hello, World!

### 中文搜索支持

由于没钱给 material for mkdocs 加 sponsor，为了实现付费功能中文搜索不得不采用了 [四步中文搜索](https://zhuanlan.zhihu.com/p/411854801) 来支持站内中文搜索功能，开发者在本地配置编译时可以先按照 tutorial 中的方法配置本地环境再推送部署。此阉割版本的搜索会有如下一些限制：

- 每个单词只能 2 个中文字，超过两个字的词不能匹配，但是可以将多于2个字的词拆成以 2 个字为一个词的方式，多个词用空格连接进行搜索。例如，`阿里云`拆分成`阿里` `云`，这样就能够搜索到同时具备这 2 个词的段落，也能搜索到只具备`阿里`或`云`的段落。并且搜索结果会注明是同时满足还是 missing 了某个关键字
- 以段落为搜索匹配范围
- 搜索可以通过空格来连接多个中文词汇，会同时展示`and`和`or`结果