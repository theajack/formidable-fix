<!--
 * @Author: chenzhongsheng
 * @Date: 2023-03-05 23:21:25
 * @Description: Coding something
-->
Revised version of [formidable](https://github.com/node-formidable/formidable)


The following code will report an error that the plugins file cannot be found in the packaging situation, because the file directory has changed due to packaging

```js
  this.options.enabledPlugins.forEach((pluginName) => {
    const plgName = pluginName.toLowerCase();
    // eslint-disable-next-line import/no-dynamic-require, global-require
    this.use(require(path.join(__dirname, 'plugins', `${plgName}.js`)));
  });
```