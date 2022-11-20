# A.1 调度算法一览

## [一、进程调度](../di-er-zhang-jin-cheng-guan-li/2.2-chu-li-ji-tiao-du#2.2.4-dian-xing-de-tiao-du-suan-fa)

- **先来先服务**（FCFS）
- **短作业优先**（SJF）
- **高响应比优先**：（等待时间+需求时间）/需求时间
- **时间片轮转调度**（RR）
- **优先级调度**
- **多级队列调度**
- **多级反馈队列调度**：从一个队列出来之后进另一个队列等待调度



## [二、内存连续分配](../di-san-zhang-nei-cun-guan-li/3.1-nei-cun-guan-li-gai-nian#3.1.3-lian-xu-fen-pei-guan-li-fang-shi)

- **单一连续分配**：只有用户区合系统区，只有一个用户进程
- **固定分区分配**：用户区分成固定大小，每个区一个进程
- [**动态分区分配**](../di-san-zhang-nei-cun-guan-li/3.1-nei-cun-guan-li-gai-nian#4-dong-tai-fen-qu-fen-pei-suan-fa)
  - **首次适应**
    - 以地址递增存储
    - 找到的第一个能用的
  - **最佳适应**：先用小的
    - 以容量递增存储
    - 产生外部碎片
  - **最坏适应**：先用大的
    - 以容量递减存储
  - **临近适应**
    - 容量递增存储
    - 从上次结束的地方继续找



## [三、cache替换算法](https://aye10032.gitbook.io/computerorganizationnote/di-san-zhang-cun-chu-xi-tong/3.6-gao-su-huan-chong-cun-chu-qi#3.6.4-cache-ti-huan-suan-fa)

- **随机（RAND）**
- **先进先出（FIFO）**
- **最近最少使用（LRU）**
  - cache增设计数器，记录存在时间
  - 替换计数器最大的
- **最近不经常使用（LFU）**
  - cache增设计数器，记录访问次数
  - 替换计数器最小的



## [四、页面置换算法](../di-san-zhang-nei-cun-guan-li/3.2-xu-ni-nei-cun-ji-shu#3.2.3-ye-mian-zhi-huan-suan-fa)

- **最佳置换（OPT）**：淘汰以后用不使用的，实际无法实现
- **先进先出（FIFO）**
  - 会产生belady异常
- **最近最久未使用（LRU）**
  - 表项中存放上次访问时间
  - 替换最大的
- **时钟（CLOCK）**
  - 设置访问位
  - 两轮扫描，第一轮将访问位置1
  - 淘汰为0的
- **改进型时钟**
  - 设置访问位、修改位
  - 四轮扫描，修改访问位
  - 优先级为修改>访问



## [五、磁盘调度算法](../di-si-zhang-wen-jian-guan-li/4.3-ci-pan-de-zu-zhi-yu-guan-li#4.3.2-ci-pan-tiao-du-suan-fa)

- **先来先服务**
- **最短寻找时间优先**
- **SCAN**：只有到头了才能返回
- **LOOK**：前面没有了可以立刻掉头
- **C-SCAN**：只有单方向处理请求，反方向直接回起点
- **C-LOOK**：单方向处理，没有了立刻掉头，回到最小的访问点



