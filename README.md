一、项目简介
1、项目名称：计算机网络课程设计--基于gh0st的远程控制主机软件
2、制作时间：2015/12
3、工程目录：以上全部

二、开发思路:  在开源gh0st远程控制软件框架下进行编程，详细分析gh0st3.6源码，去掉硬盘锁等代码，完善视频传输、远程关机功能，扩展非法内容访问控制功能，删减和简化其他无关功能。
编译环境为windows xp sp3，VC6.0，Platform SDK, Windows DDK, WinPcap_4_1_3。

三、总结和感想
一周的网络课程设计，选择了第一个远程控制题目，感觉难度适中，但没有把握好时间，导致最后一部分任务没有完成，选题难度适中，但选择了一个gh0st的开源控制软件进行编写，开始时没有什么，但写着写着觉得难度就比较大了，掌控不好整体的工程，原作者的工程十分浩大（可能是自己平时编写代码较少，以后会努力多读多写一些好代码），比较难理解。
但通过这次课程设计，也让我深入了解了ICOP模型，使用的重叠I/O与完成端口，实现了高性能服务器的能力，另外这次保活机制，相互探测，若掉线则在下一次数据传输中通知对方，也实际的让我看到应用层实现传输层的一些控制的实际例子；仅仅是向被控端准备发送标志数据包Send(pContext, NULL, 0);，实现了的重传机制，这都让我对TCP/UDP的机制有了更好的理解。对图像传输，刷新控制等有了更多的认识，修正了之前作者对win7系统图像监控失效的问题，增加了软件的可用性。使用了winpcap套件编程，亲手实现了抓包分析过程，也让我对各种抓包软件的底层实现有了更好的理解。
因为时间缘故，没有将非法网址监控过滤功能加入MFC当中，仅在命令行下实现了部分功能，另外，原作者除了在网络方面使用IOCP模型、心跳包防止掉线、使用了zlib进行压缩、CManager类的继承、回调函数NotifyProc井井有条这些特色外，主控端的稳定性，即以svchost系统服务启动这个特色，对系统进程启动这个底层实现，没有进行完整的分析，涉及到较多的汇编及c语言内容，以后有机会会对此进行深入的分析，即木马程序的隐藏技术。以后会多多努力！
