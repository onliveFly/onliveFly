# onliveFly.io
“自动下载更新脚本”更新之后需要手动关闭AutoJS
否则新的dex没法覆盖加载。
具体操作以MIUI为例，上划打开后台 长按AutoJS，
设置 选择结束运行，而不仅仅是滑动关闭。
理论上Pro版已经支持覆盖加载，免费版不支持。
但是为了保险起见都进行一遍强制停止。

可以手动修改第23行 
将解压路径修改为你喜欢的文件夹
let targetOutputDir = files.cwd()
比如修改为如下
let targetOutputDir = '/storage/0/脚本/你喜欢的路径'
下载完成后新代码就会到
'/storage/0/脚本/你喜欢的路径'里面

执行完毕后需要在 targetOutputDir中下拉刷新，否则看不到


本 “自动下载更新脚本” 同样适用于
所有github/releases发布的最新脚本
仅仅需要修改21行 
let apiUrl = "目标脚本更新API"
"目标脚本更新API" 需要自己去获取
格式如下：
'https://api.github.com/repos/${github用户名}/${github仓库名}/releases/latest'
当然如果没有发布releases 下载也是无效的
