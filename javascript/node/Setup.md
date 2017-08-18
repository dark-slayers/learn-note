# Node.js安装说明
1. 下载Node.js的Windows安装版,
2. 安装到指定路径：D:\DK\Node\
3. CMD下输入:	node –v，显示版本号说明安装成功
4. CMD下输入:	npm -v，显示版本号说明安装成功
5. 验证node.js:	CMD输入node，光标变为>，输入: console.log('hello world')
6. 配置npm的全局模块路径和cache路径，在D:\DK\Node\文件夹下建立"node_global"及"node_cache"两个文件夹
7. CMD输入：	npm config set prefix "D:\DK\Node\node_global"										npm config set cache "D:\DK\Node\node_cache"
8. 安装验证npm:CMD输入：npm install express –g，安装过程结束后，会提示“express”装在了哪、版本还有它的目录结构是怎样。
9. 设置环境变量：在系统变量下新建"NODE_PATH"，输入D:\DK\Node\node_global\node_modules。
10. 环境变量：系统变量：Path添加：D:\DK\Node\node_global\
11. 验证：CMD输入：node，进入node，输入require('express')来测试下node的模块全局路径是否配置正确了。正确的话cmd会列出express的相关信息。
12. 定位npm服务器至淘宝服务器：
13. npm install -g cnpm --registry=https://registry.npm.taobao.org
14. 使用cnpm代替npm
---
# 使用webpack编译React项目
1. 安装node.js,npm.
2. 安装全局工具
cnpm install webpack -g
cnpm install webpack-dev-server -g
3. 安装项目工具
cnpm init
初始化项目为npm项目	非必须

cnpm install --save-dev react react-dom jquery
安装REACT核心库和jquery

cnpm install --save-dev babel-loader babel-core babel-cli
安装babel核心库

cnpm install --save-dev babel-preset-es2015 babel-preset-react babel-preset-stage-0
cnpm install --save-dev babel-plugin-syntax-dynamic-import
安装ES6翻译器，react翻译器,ES7支持


cnpm install --save-dev style-loader css-loader 	安装CSS加载器
cnpm install --save-dev url-loader 		
安装加载器

cnpm install --save-dev babel-plugin-transform-es3-member-expression-literals
cnpm install --save-dev babel-plugin-transform-es3-property-literals
ES3插件

cnpm install --save-dev es5-shim
低版本的浏览器（IE8）支持ES5的库

cnpm install --save-dev es6-shim
低版本的浏览器（IE8）支持ES6的库

4. 创建、配置相关文件
创建配置文件webpack.config.js
样例文件：
<pre>
<code>
`var config = {
  entry: './index.js',
    output: {
     path:'./',
     filename: 'bundle.js',
  },
  module: {
     loaders: [ {
        test: /\.jsx?$/,
        exclude: /node_modules/,
        loader: 'babel',
        query: {
           presets: ['es2015', 'react']
        }
     }]
  }
 }
module.exports = config;`
</code>
</pre>


5. 测试文件
创建文件：index.html
<pre>
<code>
`<!DOCTYPE html>
<html>
   <head>
      <meta charset = "UTF-8">
      <title>React App - Webpack测试</title>
   </head>
   <body>
      <div id = "app"></div>
      <script src = "bundle.js"></script>
   </body>
</html>`
</code>
</pre>


创建文件：App.jsx
<pre>
<code>
`import React from 'react';
class App extends React.Component {
   render() {
      return (
         <div>
            Hello React!!!<br />
            React组件运行成功！！！
         </div>
      );
   }
}
export default App;`
</code>
</pre>


创建文件：index.js
<pre>
<code>
`import React from 'react';
import ReactDOM from 'react-dom';
import App from './App.jsx';
ReactDOM.render(<App />, document.getElementById('app'));`
</code>
</pre>


6. 运行:webpack，如果index.html能够正常运行，说明配置正确
