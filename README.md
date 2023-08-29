# vuepress-plugin-rpurl

## install
```bash
yarn add liyao/vuepress-plugin-repalceUrl -D
```

## Use
### Default
```js
// .vuepress/config.js
// or
// .vuepress/theme/index.js

module.exports = {
  plugins: ['repalceUrl']
}
```

The Default configuration is for vuepress-plugin-autobar, it clean the cumbersome parameter.

Default Rule: `[[/nav[\.\-_]*\d*[\.\-_]*/gi, ''], [/\d+[\.\-_]*/gi, '']]`

* before use:
`/nav.10.js/10-core/mian-xiang-dui-xiang/mian-xiang-dui-xiang.html`

* after use:
`/js/core/mian-xiang-dui-xiang/mian-xiang-dui-xiang.html`

### Customize
You can customize your replace rules. Example:

```js
// .vuepress/config.js
// or
// .vuepress/theme/index.js

module.exports = {
  plugins: ['repalceUrl', [/regex/i, 'new world']]
  // or multiple rules
  // plugins: ['repalceUrl', [[/regex1/, 'world'], [/regex2/gi, 'world2']]]
}
```

