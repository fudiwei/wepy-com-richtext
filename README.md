# wepy-com-richtext

为官方提供的 *&lt;rich-text&gt;&lt;/rich-text&gt;* 组件提供渐进式支持，并支持官方本身不支持的下划线 HTML 标签（即 *&lt;u&gt;&lt;/u&gt;*）和符合 ISO 8859 的实体符号。

此组件依赖 [wepy](https://github.com/Tencent/wepy) 1.7.0+。

---

## 用法

安装：

``` shell
npm install @step/wepy-com-richtext --save
```

引入组件：

``` html
<template>
    <ui-richtext :content.sync="html" :decode.sync="true" />
</template>
<script>
    import wepy from 'wepy';
    import UIRichText from '@step/wepy-com-richtext';

    export default class DemoPage extends wepy.page {
        components = {
            'ui-richtext': UIRichText
        };
    }
</script>
```

### 可配置项

#### 属性

| 参数项 | 说明 | 类型 | 是否必填 | 默认值 |
| :---: | :---: | :---: | :---: | :---: |
| content | HTML 源代码片段 | String | 是 | |
| decode | 是否按照富文本方式显示 | Boolean | 否 | false |

#### 方法

*无*