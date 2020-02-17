# 前言
仅用于技术交流，请勿用于非法用途

这个插件没有什么技术含量，旨在用于快速生成免杀的可执行文件，目前仅支持exe文件格式。需要安装go环境，因为是用`go build`生成的

免杀效果如下图：

[http://r.virscan.org/language/zh-cn/report/7e2b37c3f31d65c953f0d9401024d1e6](http://r.virscan.org/language/zh-cn/report/7e2b37c3f31d65c953f0d9401024d1e6)

![img](./img/1.png)

![img](./img/2.png)

用法：导入之后，位置在：`attack` -> `BypassAV`，快捷键：`Ctrl+G`

![img](./img/3.gif)

如果你生成的马被杀了，可以重新生成一个，因为key是随机的或者你改一下代码把key改为你想要的也可以。

因为Sleep貌似不能获取和设置环境变量，所以如果是linux和Mac OS的同学请自行编译，生成之后到cs的目录下编译 /捂脸

```sh
export GOOS=windows
export GOARCH=amd64
go build temp.go
```

**注：** 用go打包体积可能会有点大（1.2M左右），可以用upx压缩一下，大概能压缩到600kb左右那样子