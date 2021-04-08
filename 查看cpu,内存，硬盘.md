一、查看CPU
1.1 查看CPU个数
# cat /proc/cpuinfo | grep "physical id" | uniq | wc -l
2 **uniq命令：删除重复行;wc –l命令：统计行数**
1.2 查看CPU核数
# cat /proc/cpuinfo | grep "cpu cores" | uniq
cpu cores : 4
1.3 查看CPU型号
# cat /proc/cpuinfo | grep 'model name' |uniq
model name : Intel(R) Xeon(R) CPU E5630 @ 2.53GHz
总结：该服务器有2个4核CPU，型号Intel(R) Xeon(R) CPU E5630 @ 2.53GHz
二、查看内存
2.1 查看内存总数
#cat /proc/meminfo | grep MemTotal
MemTotal: 32941268 kB //内存32G
2.2 查看内存条数
三、查看硬盘
3.1 查看硬盘大小
# fdisk -l | grep Disk
Disk /dev/cciss/c0d0: 146.7 GB, 146778685440 bytes
总结：硬盘大小146.7G，即厂商标称的160G
