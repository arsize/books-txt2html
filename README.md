## books-txt2html

在线 txt 文件转 html，无须 fork 仓库，无须本地操作，通过 get 接口拼接参数即可对 txt 文件进行排版、美化、章节分割、生成目录，并返回适合阅读的 html 页面。

---

## 使用方式

1.GET

```bash
get url http://api/path/index?url=http://books/xxx.txt
```

2.POST

参数说明:

| 参数 | 描述         | 默认值           |
| ---- | ------------ | ---------------- |
| url  | txt 文件链接 | 必选             |
| rule | 章节切分规则 | 默认:h1 h2 h3 h4 |
| name | 书籍名称     | 默认截取文件名   |

## 搭配 notion+七牛云 oss

可以用[Notion](https://www.notion.so/)生成 Read list 模版，进行书籍清单维护，txt 资源放在七牛云 oss（10G 免费空间），生成外链后，将它作为 url 参数拼接在 api 后面，填写到对应书籍的链接栏，即可点击进行阅读。

![](https://raw.githubusercontent.com/arsize/pic-bed/ec4309c57ccf78c810aec0d10dcba7e1f8bcbb4f/obsidian/202211271516559.png)

## 计划支持的功能

1. 根据 txt 书名+豆瓣 api 获取图书封面及详情、评分
2. 本地缓存链接及进度，方便支持下次继续阅读
3. 支持简单的字体大小，背景颜色、行距调整
4. 支持 PDF、epub

### 最后

该项目不存储任何数据，只是提供一个 txt-html 的在线处理工具，对传入的 txt 文件进行处理、优化排版并返回展示，不涉及任何书籍版权问题。
