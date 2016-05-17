boi-cli
=======

boi is short for bolshoi

基于webpack的前端工程构建工具，文档[document]()。

### 安装

```
npm install boi-cli -g
```

### 编译项目文件

1.	在项目根目录下创建文件`boi-conf.js`;
2.	编辑`boi-conf.js`中的配置项，比如js文件的编译配置如下：

```
boi.spec('js', {
    extType: 'js',
    srcType: ['es2015'],
    files: {
        vendor: ['vue']
    },
    srcDir: 'js',
    destDir: 'js'
});
```

在项目根目录下执行`boi build`

### 使用插件

编辑`boi-conf.js`，使用API `boi.use`引入插件，比如：

```
boi.use('boi-plugin-loader-vue');
```

boi会判断用户是否已安装此插件，如果没有，则boi会自动安装此插件。

> 建议自行安装插件，boi使用npm安装插件，由于一些*原因*可能会安装失败

如果npm被墙，请尝试以下*任意一种方案：

1.	挂VPN；
2.	修改npm仓库到淘宝镜像`npm config set registry https://registry.npm.taobao.org`;
3.	安装cnpm。

> 如果安装cnpm，请务必自行安装插件
