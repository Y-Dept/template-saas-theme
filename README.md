# template-saas-theme

for override ant-design theme

Install
-----

```javascript

npm install --save template-saas-theme

```


Usage
-----

in webpack.config.js file:

```javascript

const theme = require('template-saas-theme').red;

...

{
  test: /\.less$/,
  use: ExtractTextPlugin.extract({
    fallback: 'style-loader',
    use: [{
      loader: 'css-loader',
      options: {
        minimize: (isProd || isTest),
        sourceMap: !isProd
      }
    }, 'postcss-loader', {
      loader: 'less-loader',
      options: {
        "modifyVars": theme
      }
    }]
  }),
  exclude: /.m.less$/
}

```
