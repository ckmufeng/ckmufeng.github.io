# cmp-dictionary 踩坑
现象为选择单词的时候报错，
```
system.lua: ... No such file or directory
```

查询后为需要安装 wordnet 

下载编译安装踩坑：
不要使用 conda 中的 tcl 包。使用系统安装的 tcl/tk 包，同时安装 devel 包。
第二个坑
编译时，报 
```
error: ‘Tcl_Interp’ has no member named ‘result’
```
原因为， tcl 8.6.14 升级了对应接口
需要使用 `Tcl_SetResult` 接口来修改 result。
