# Ean-ui

## 使用教程

#### 执行命令

```
yarn add ean-ui

yarn add babel-plugin-import -D
```

#### 在 `.babelrc.js` 或 `babel.config.js` 下引入：

```js
module.exports = {
  presets: ["@vue/app"],
  plugins: [
    [
      "import",
      {
        libraryName: "ean-ui",
        camel2DashComponentName: false,
        camel2UnderlineComponentName: false,
        style: (name) => {
          const cssName = name.split("/")[2];
          return `ean-ui/lib/style/${cssName}.css`;
        },
      },
    ],
  ],
};
```

#### 使用

```js
<template>
<ColorTitle title='EanUI'/>
</template>

import { ColorTitle } from "ean-ui";
<script>
export default {
    components: { ColorTitle }
}
</script>
```
