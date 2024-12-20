# Linux 常用命令

| **命令** | **用途** | **使用格式** | **备注** |
| --- | --- | --- | --- |
| **`echo`** | 在终端输出字符串或变量提取后的值 | echo [字符串 | $变量] |  |
| **`date`** | 显示及设置系统的时间或日期 | date [选项] [+指定的格式] |  |
| **`reboot`** | 重启系统（需要管理员权限） | reboot | sudo reboot |
| **`~~poweroff~~`** | ~~关闭系统（需要管理员权限）~~ | ~~poweroff~~ | ~~mac无~~ |
| [**`wget`**](https://bytedance.feishu.cn/wiki/wikcnxhwckqaTUxeitAxLDQ9SPd#TQPRc2) | 在终端中下载网络文件 | wget [参数] 下载地址 | mac需单独安装 |
| **`ps`** | 查看系统中的进程状态 | ps [参数] | mac与Linux不同 |
| **`top`** | 动态地监视进程活动与系统负载等信息 | top |  |
| **`pidof`** | 查询某个指定服务进程的PID值 | pidof [参数] [服务名称] | mac只能用ps |
| **`kill`** | 终止某个指定**PID**的服务进程 | kill [参数] [进程PID] |  |
| **`killall`** | 终止某个指定**名称**的服务所对应的全部进程 | killall [参数] [服务名称] |  |
| **`ifconfig`** | 获取网卡配置与网络状态等信息 | ifconfig |  |
| **`uname`** | 查看系统内核与系统版本等信息 | uname [-a] | 固定搭配上-a参数来完整地查看当前系统的内核名称、主机名、内核发行版本、节点名、系统时间、硬件名称、硬件平台、处理器类型以及操作系统名称等信息。 |
| **`uptime`** | 查看系统的负载信息 | uptime | 显示当前系统时间、系统已运行时间、启用终端数量以及平均负载值等信息。平均负载值指的是系统在最近1分钟、5分钟、15分钟内的压力情况。j |
| **`~~free~~`** | ~~显示当前系统中内存的使用量信息~~ | ~~free [-h]~~ | ~~mac无~~ |
| **`who`** | 查看当前登入主机的用户终端信息 | who |  |
| **`last`** | 查看所有系统的登录记录 | last |  |
| **`history`** | 显示历史执行过的命令 | history [-c] | 使用-c参数则会清空所有的命令历史记录。
history后有命令记录前有数字，使用“!编码数字”的方式来重复执行某一次的命令。 |
| **`~~sosreport~~`** | ~~收集系统配置及架构信息并输出诊断文档~~ | ~~sosreport~~ | ~~mac无~~ |
| **`pwd`** | 显示用户当前所处的工作目录 | pwd |  |
| **`cd`** | 切换工作路径 | cd [目录名称] |  |
| **`ls`** | 显示目录中的文件信息 | ls [选项] [文件] |  |
| [**`cat`**](https://bytedance.feishu.cn/wiki/wikcnxhwckqaTUxeitAxLDQ9SPd#1JxiNF) | 查看纯文本文件（内容较少的） | cat [选项] [文件] | cat是一次性显示整个文件的内容，还可以将多个文件连接起来显示，它常与[重定向](https://so.csdn.net/so/search?q=%E9%87%8D%E5%AE%9A%E5%90%91&spm=1001.2101.3001.7020)符号配合使用，适用于文件内容少的情况； |
| **`more`** | 查看纯文本文件（内容较多的） | more [选项] [文件] | 使用空格键或回车键向下翻页，more命令会在最下面使用百分比的形式来提示您已经阅读了多少内容。用空格显示下一页，按键b显示上一页。输入q退出。 |
| **`less`** | 查看纯文本文件（内容较多的） | less [选项] [文件] | less比more更强大，提供翻页，跳转，查找等命令。 |
| **`head`** | 查看纯文本文档的前N行 | head [选项] [文件] |  |
| **`tail`** | 查看纯文本文档的后N行或持续刷新内容 | tail [选项] [文件] | 当想要实时查看最新日志文件时，使用“tail -f 文件名” |
| **`tr`** | 替换文本文件中的字符 | tr [原始字符] [目标字符] | 例如，把某个文本内容中的英文全部替换为大写：
cat [文件] | tr [a-z] [A-Z] |
| **`wc`** | 统计指定文本的行数、字数、字节数 | wc [参数] 文本 | 在Linux系统中，passwd是用于保存系统账户信息的文件，要统计当前系统中有多少个用户:
wc -l /etc/passwd |
| **`stat`** | 查看文件的具体存储信息和时间等信息 | stat 文件名称 | mac与Linux实现不同 |
| **`cut`** | 按“列”提取文本字符 | cut [参数] 文本 | 使用-f参数来设置需要看的列数，使用-d参数来设置间隔符号。
passwd在保存用户数据信息时，用户信息的每一项值之间是采用冒号来间隔的，提取以冒号（：）为间隔符号的第一列内容：
cut -d: -f1 /etc/passwd |
| **`diff`** | 比较多个文本文件的差异 | diff [参数] 文件 | diff --brief命令显示比较后的结果（differ表示不同）
使用-c参数来描述文件内容具体的不同 |
| [**`touch`**](https://bytedance.feishu.cn/wiki/wikcnxhwckqaTUxeitAxLDQ9SPd#c0pMY9) | 创建空白文件或设置文件的时间 | touch [选项] [文件] | 黑客可能会用来修改文件时间 |
| **`mkdir`** | 创建空白cd的目录 | mkdir [选项] 目录 | -p参数来递归创建出具有嵌套叠层关系的文件目录 |
| [**`cp`**](https://bytedance.feishu.cn/wiki/wikcnxhwckqaTUxeitAxLDQ9SPd#BPbzIV) | 复制文件或目录 | cp [选项] 源文件 目标文件 |  |
| **`mv`** | 剪切文件或将文件重命名 | mv [选项] 源文件 [目标路径|目标文件名] | 剪切操作不同于复制操作，因为它会默认把源文件删除掉，只保留剪切后的文件。如果在同一个目录中对一个文件进行剪切操作，其实也就是对其进行重命名。 |
| **`rm`** | 删除文件或目录 | rm [选项] 文件 | -f参数来强制删除（删除目录时必须有）
mac不会进行询问，会直接删除。 |
| **`dd`** | 按照指定大小和个数的数据块来复制文件或转换文件 | dd [参数] | 可以用来拷贝镜像 |
| **`file`** | 查看文件的类型 | file [文件] | 在Linux系统中，由于文本、目录、设备等所有这些一切都统称为文件，不能单凭后缀就知道具体的文件类型，这时就需要使用file命令来查看文件类型。 |
| [**`tar`**](https://bytedance.feishu.cn/wiki/wikcnxhwckqaTUxeitAxLDQ9SPd#eMyWLm) | e对文件进行打包压缩或解压 | tar [选项] [文件] | 把指定的文件进行打包压缩：
tar -czvf 压缩包名称.tar.gz 要打包的目录
把指定的压缩包进行解压：
tar xzvf 压缩包名称.tar.gz -C 要解压的目录 |
| [**`grep`**](https://bytedance.feishu.cn/wiki/wikcnxhwckqaTUxeitAxLDQ9SPd#POWiD6) | 在文本中执行关键词搜索，并显示匹配结果 | grep [选项][关键词] [文件] |  |
| **`find`** | 按照指定条件来查找文件 | find [查找路径] 寻找条件 操作 |  |
| [**`export`**](https://bytedance.feishu.cn/wiki/wikcnxhwckqaTUxeitAxLDQ9SPd#3mjXv1) | 设置或显示环境变量 | export [-fnp][变量名称]=[变量设置值] |  |
| **`vim`** | 新建并编辑文件 | vim [文件] | Linux的内置文本编辑器工具 |
| **`man`** | 查看命令说明（用户手册） | man [参数][要查询的命令] |  |
| **`tldr`** | 查看简洁的命令说明 | tldr [要查询的命令] | mac需安装 |
| **`ccat`** | cat命令的升级版 | 同cat | mac需安装 |
| **`fuck`** | 修正刚才手误的命令 | fuck | 在输错命令后紧跟输一个fuck，mac需安装thefuck |