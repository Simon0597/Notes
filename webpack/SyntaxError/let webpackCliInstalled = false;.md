```
[root@FreeServer ~]# webpack -v
/usr/local/node-v4.4.7-linux-x64/lib/node_modules/webpack/bin/webpack.js:3
let webpackCliInstalled = false;
^^^

SyntaxError: Block-scoped declarations (let, const, function, class) not yet supported outside strict mode
    at exports.runInThisContext (vm.js:53:16)
    at Module._compile (module.js:373:25)
    at Object.Module._extensions..js (module.js:416:10)
    at Module.load (module.js:343:32)
    at Function.Module._load (module.js:300:12)
    at Function.Module.runMain (module.js:441:10)
    at startup (node.js:139:18)
    at node.js:968:3
 ```
## 这是因为nodejs版本太低，或者说webpack版本太高，我这里用的nodejs版本是4.4.7，默认安装的webpack版本是4.3.0，所以不兼容。然后我把webpack卸载掉，重新安装了2.6.1版本的webpack，问题解决：
```
[root@FreeServer ~]# npm uninstall webpack -g
unbuild webpack@4.3.0
[root@FreeServer ~]# npm install webpack@2.6.1 -g --registry=https://registry.npm.taobao.org
[root@FreeServer ~]# webpack -v
2.6.1
[root@FreeServer ~]#
```
