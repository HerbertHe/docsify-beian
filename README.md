# docsify-beian

<p align="center">
  <img src="https://docsify.js.org/_media/icon.svg" />
  <br />
  <code>docsify-beian</code>
</p>

[![jsdelivr](https://data.jsdelivr.com/v1/package/npm/docsify-beian/badge)](https://www.jsdelivr.com/package/npm/docsify-beian)

docsify之备案插件 docsify plugin for Chinese Beian

## Usage

添加依赖 Add script

```html
<script src="https://cdn.jsdelivr.net/npm/docsify-beian@latest/dist/beian.min.js"></script>
```

添加配置 Add settings

```js
window.$docsify = {
  beian: {
        ICP: "",
        NISMSP: {
            number: "",
            url: "",
            id: ""
        },
    },
}
```

| 属性名称        | 属性解释                                                                       | 默认值 |
| --------------- | ------------------------------------------------------------------------------ | ------ |
| `ICP`           | 工信部ICP备案号                                                                | ""     |
| `NISMSP`        | 全国互联网安全管理服务平台备案（公安部备案）                                   | {}     |
| `NISMSP.number` | 公安部备案号（没有留空）                                                       | ""     |
| `NISMSP.url`    | 公安部备案链接（没有留空）                                                     | ""     |
| `NISMSP.id`     | 公安部备案号的数字部分（没有留空，优先级比`NISMSP.url`更高，用于生成跳转链接） | ""     |

> 现在公安部备案url的格式为 `http://www.beian.gov.cn/portal/registerSystemInfo?recordcode=` 加上你的备案号的数字部分
