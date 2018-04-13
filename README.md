### postcss-px2rem-eliminate
    
依赖于postcss-px2rem，由于webpack编译时对注释的不友好，以及不想对某些三方依赖组件的px转换，更改了部分源码。

#### 使用

    module.exports = {
      "plugins": {
        // 因为 webpack 压缩的问题 https://github.com/songsiqi/px2rem/issues/2 占时启用 自己修改后的插件
        "postcss-px2rem-eliminate": {
          baseDpr: 2,
          remUnit: 37.5,
          exclude: /node_modules/
        }
      }
    }
