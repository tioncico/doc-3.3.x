## LinuxDash
linuxDash封装了很多直接获取linux信息的命令.
组件源码地址:https://github.com/easy-swoole/linux-dash  
安装:  
```bash
composer require easyswoole/linux-dash 
```  


## 示例
```php

$run = new \Swoole\Coroutine\Scheduler();
$run->add(function () {
    //获取ip地址网卡缓冲信息
    $data = LinuxDash::arpCache();
    var_dump($data);
    //获取当前带宽数据
    $data = LinuxDash::bandWidth();
    var_dump($data);
    //获取cpu进程占用排行信息
    $data = LinuxDash::cpuIntensiveProcesses();
    var_dump($data);
    //获取磁盘分区信息
    $data = LinuxDash::diskPartitions();
    var_dump($data);
    //获取当前内存使用信息
    $data = LinuxDash::currentRam();
    var_dump($data);
    //获取cpu信息
    $data = LinuxDash::cpuInfo();
    var_dump($data);
    //获取当前系统信息
    $data = LinuxDash::generalInfo();
    var_dump($data);
    //获取当前磁盘io统计
    $data = LinuxDash::ioStats();
    var_dump($data);
    //获取ip地址
    $data = LinuxDash::ipAddresses();
    var_dump($data);
    //CPU负载信息
    $data = LinuxDash::loadAvg();
    var_dump($data);
    //获取内存详细信息
    $data = LinuxDash::memoryInfo();
    var_dump($data);
    //获取进程占用内存排行信息
    $data = LinuxDash::ramIntensiveProcesses();
    var_dump($data);
    //获取swap交换空间信息
    $data = LinuxDash::swap();
    var_dump($data);
    //获取当前用户名信息
    $data = LinuxDash::userAccounts();
    var_dump($data);

});
$run->start();
```

> 注意，mac环境不兼容。但是可以用docker测试
