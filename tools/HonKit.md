# HonKit

>[HonKit官方文档](https://honkit.netlify.app/)

▶Install HonKit
>安装HonKit之前需要Node.js环境 ▶[Install Node.js](Node.js.md)

```
npm install honkit --save-dev
```

▶define init and show command in package.json

```json
//package.json
{
  "devDependencies": {
    "honkit": "^3.7.4"
  },
  "scripts": {
    "init": "honkit init",
    "show": "honkit serve"
  }
}

```

▶Build EPUB

```
npm run init
```

▶Show EPUB

```
npm run show
```

▶Directory Structure/目录结构

```
--------.
  '    |-- book.json',
  '    |-- package.json',
  '    |-- docs',
  '    |   |-- cover.jpg',
  '    |   |-- GLOSSARY.md',
  '    |   |-- LANGS.md',
  '    |   |-- README.md',
  '    |   |-- SUMMARY.md',
  '    |-- export',
  '    |-- _book',
  
```


|File|Description|
|---|---|
|book.js|存放书籍配置数据的Json文件|
|docs|存储项目文档的文件夹|
|README.md|书籍前言|
|SUMMARY.md|书籍目录|
|GLOSSARY.md|词典，术语列表|
|export|输出电子书的文件夹|
|cover.jpg|书籍页面图片|


▶Config book.json

>[官方配置介绍](https://honkit.netlify.app/config.html)

```
//book.json
{
  "root": "./docs",
  "title": "mybook",
  "language": "en"
}
```

▶其他
- [01_设置目录](https://honkit.netlify.app/pages.html)
- [02_Markdown语法](https://honkit.netlify.app/syntax/markdown.html)

▶Export EPUB

- Install Calibre
  
  [Calibre官方下载地址](https://calibre-ebook.com/download)

- 配置环境与关机重启

  1.找到ebook-convert所在的文件夹路径，我的是C:\Program Files\Calibre2，**把ebook-convert所在的文件夹路径添加到电脑系统环境变量。**

  2.添加完ebook-convert的环境变量可能不会立刻生效，建议**重启电脑。**


+ ▶**OK！开始输出epub/pdf/mobi电子书吧**

  1.Define epub and pdf command in package.json
    ```json
            {
          "devDependencies": {
            "honkit": "^3.7.4"
          },
          "scripts": {
            "init": "honkit init",
            "show": "honkit serve",
            "epub": "honkit epub",
            "pdf": "honkit pdf"
          }
        }
    ```

  2.输出EPUB
    ```
    npm run epub .\ .\export\mybook.epub
    ```
  3.输出PDF
    ```
    npm run pdf .\ .\export\mybook.pdf
    ```