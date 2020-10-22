# Vue Split Pane

Split-Pane-Pixel component built with vue2.0, can be split vertically or horizontally.

Fork from https://github.com/PanJiaChen/vue-split-pane

Split-Pane-Pixel only support set pixel value.

## [Try the demo](http://panjiachen.github.io/split-pane/demo/index.html)

### How to use?

```bash
npm install vue-splitpane-pixel

#import
import splitPane from 'vue-splitpane-pixel'

# use as global component
Vue.component('split-pane', splitPane);
```

### Example

```html
<split-pane
  v-on:resize="resize"
  :min-size="120"
  :default-size="300"
  :max-size="1000"
  split="vertical"
>
  <template slot="paneL"> A </template>
  <template slot="paneR"> B </template>
</split-pane>
```

```html
//nested
<split-pane
  v-on:resize="resize"
  :min-size="120"
  :default-size="300"
  :max-size="1000"
  split="vertical"
>
  <template slot="paneL"> A </template>
  <template slot="paneR">
    <split-pane split="horizontal">
      <template slot="paneL"> B </template>
      <template slot="paneR"> C </template>
    </split-pane>
  </template>
</split-pane>
```

### Options

| Property     | Description        |             type             |       default        |
| ------------ | ------------------ | :--------------------------: | :------------------: |
| split        | the split type     | String [horizontal,vertical] | must choose one type |
| min-size     | paneL min-size     |            Number            |         100          |
| max-size     | paneL max-size     |            Number            |     0 (not set)      |
| default-size | paneL default size |            Number            |         250          |

# License

MIT
