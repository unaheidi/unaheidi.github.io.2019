---
layout: post
---

## Linux运维常见命令（赞）

###  最近修改了哪些文件？

背景：有时候多人维护一个服务的测试环境，前一天同事在测试环境修改了一些配置，我想知道做了哪些变更。同事很忙不便打扰，我想自己把变更的文件查找出来。

```
 find ./ !  -name '*log' !  -path 'log'   -mtime 0;
 
```

### 哪些文件包含特定的文字？

```
 grep -rnw '/path/to/somewhere/' -e 'pattern'
 grep --exclude=*.log*  -rnw '.' -e '10.18.5.110'
 grep --exclude-dir=node_modules  -rnw '.' -e 'database'
 
```

