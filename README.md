[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/VsbltiDW)

# CICV-R4L-3-XForceVESA

## Synopsis

The homeworks are in the directory `docs`.

The following content is in Chinese.

- 这是[作业链接](https://docs.qq.com/doc/DSk5xTHRJY1FZVUdK)
- [学习记录与感言](./docs/07-notes.md)

### 作业1：编译Linux内核

- [文档在此](docs/01-busybox-kernel.md)
- 完成情况：已经成功安装和配置了BusyBox，并编译和加载了自定义的Linux内核，能够熟练地使用BusyBox命令，并理解了内核模块的基本操作。

### 作业2：对Linux内核进行一些配置

- [文档在此](docs/02-linux-network.md)
- 完成情况：网络接口配置、路由与转发、驱动构建等任务已经全部完成。掌握了Linux系统中网络配置的基本技能，并能够解决一些常见的网络问题。

### 作业3：使用rust编写一个简单的内核模块并运行

- [文档在此](docs/03-hacking-kernel.md)
- 完成情况：编写了一个简单的内核模块，能够在系统启动时打印一段信息，并在日志中打印一些信息。掌握了Rust语言的基本语法，并能够熟练地使用Rust进行系统编程。

### 作业4：为e1000网卡驱动添加remove代码
- [文档在此](docs/04-remove-module.md)
- 完成情况：为Rust驱动模块添加了drop方法，以便于模块销毁时释放资源。掌握了Rust的生命周期管理机制，并能够熟练地编写驱动模块。

### 作业5：注册字符设备
- [文档在此](docs/05-char-device.md)
- 完成情况：编写了一个字符设备驱动，能够接收输入，并将其打印到控制台。掌握了Linux字符设备驱动的基本知识，并能够熟练地编写驱动模块。

### 项目小试验
- [文档在此](docs/06-linux-network-exmeriments.md)
- 完成情况：
  1. 环境配置：环境搭建成功，根据文档撰写了一个[自动化构建脚本](./r4l_experiment/build.sh)，可自动化构建，并在脚本中启用了NFS与TCP/Telnet，启动时可挂载。
  2. 实战要求：实现了[002_completion](./r4l_experiment/driver/002_completion/)的Rust重构版，位置在[此处](./r4l_experiment/driver/003_completion_rust/)，可`make`构建，并加载，完成类似功能。
