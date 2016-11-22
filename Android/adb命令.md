# Android 常用 ADB 命令

### ADB 自身管理相关命令

命令                            | 说明
-----------------------------|-----------------------------------------------------
adb kill-server 			 | 终止 ADB 服务进程
adb start-server			 | 启动或重启 ADB 服务进程
adb root			 | 以 root 权限重启 ADB 服务


### 使用 ADB 进行设置（包括模拟器）管理

命令                            | 说明
-----------------------------|-----------------------------------------------------
adb devices 			 | 查看连接到计算机上的设备
adb  get-serialno			 |  获取连接到电脑上设备的序列号，当前只能连接一台设备才能获取得到
adb  reboot 			 |  重启连接到电脑上的设备
adb reboot bootloader/recovery			 | 重启设备进入到 fastboot 模式或 recovery 模式，通常在刷机的时候用到
adb [-d/-e/-s<serialNumber>] command  | 发送指定命令给指定设备，其中serialNuber是设备号


### 获取设备硬件信息

命令                            | 说明
-----------------------------|-----------------------------------------------------
adb shell cat /sys/class/net/wlan0/address			 | 获取 wifi mac 地址
adb shell cat/proc/cpuinfo		 |  获取 cpu 序列号
adb shell cat /system/build.prop		 |  获取设备编译属性
adb shell cat /data/misc/wifi/*.conf		 | 获取设备 Wi-Fi 配置信息


### 通过设备管理 APP 应用操作

命令                            | 说明
-----------------------------|-----------------------------------------------------
adb install [-r|-s] <apkfile>			 |  安装 apk 文件
adb uninstall [-k] <packagename>			 | 卸载 APP
adb  shell top [-m <number>] 			 | 查看内存情况，如果有 number 表示查看多少条数据
adb  shell ps			 | 查看进程列表数据
adb shell kill <pid>			 | 杀死对应 pid 的进程
adb shell ps -x <pid> 		 | 查看指定 pid 进行的运行状态
adb  shell  service list  			 | 查看后台服务信息
adb  shell cat /proc/meminfo		 | 查看当前内存占用情况 
adb  shell cat /proc/iomen			 | 查看 io 内存分区情况


### 对文件进行操作的相关 adb 命令

命令                            | 说明
-----------------------------|-----------------------------------------------------
adb shell ls mnt			 | 查看所有设备中的存储设备名
adb  remount			 | 将 system 分区重新挂载为可读写分区
adb push <local> <remote>		 | 从本地复制文件到设备中 local 和 remote 分别对应本地与设备的文件
adb  pull <remote> <local>		 | 从设备复制文件到本地的操作
adb shell ls			 | 查看目录下的所有文件及文件夹
adb shell cd <folder>		 | 查看文件夹内容
adb  shell mkdir path/floldername			 | 新建文件



### 通过设备管理 APP 应用操作

命令                            | 说明
-----------------------------|-----------------------------------------------------
adb  shell input text <context>		 |  发送文件内容
adb  shell input keyevent <keycode>			 | 通过 adb 命令发送键盘事件
adb  shell wm size		 | 获取设备分辨率
adb  shell getprop <key>	 | 获取设备参数信息
adb shell setprop <key> <value>	 | 设置设备的参数信息
adb shell screencap -p <path/file>	 | 使用adb命令进行截屏操作
adb  shell screenrecord [options] <path/filename>	 | 使用 adb 命令进行视屏录制



