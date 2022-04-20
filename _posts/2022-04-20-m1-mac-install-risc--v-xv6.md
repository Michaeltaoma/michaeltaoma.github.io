---
layout: post
title: M1 Mac Install risc-v, qemu and xv6
updated: 2022-04-20 13:33
description: risc-v, xv6, mit
---

为了尝试做<a href="https://pdos.csail.mit.edu/6.S081/2020/">6.S081 (Introduction to Operating Systems)</a>的lab, 需要配置<code>risc-v, qemu, xv6</code>.

#### 我的电脑配置
- MacBook Pro (16-inch, 2021)
- macOS Monterey, version = 12.3.1

#### 配置全指南
- 在开始之前，先检查一下自己的<code>~/.bash_profile, ~/.zshrc</code>等配置文件有没有export一些奇奇怪怪的flag，如果有的话请尽快删除以免影响配置
- 很多人已经写出了很全面的教程，这里只是为了address一些貌似只有我遇到过的问题，需要完整的配置教程的话，点开[参考](#参考)下的文章（按照"于我"有用的程度从上到下排序）
#### Steps
##### Risc-V toolchain
- 如果不想自己编译/编译<code>risc-v</code>出bug的话，可以直接从别人那里下载编译好的版本，见[参考](#参考)
- 我用的是<a href="https://cloud.tencent.com/developer/article/1939023">MIT 6.S081/Fall 2020 搭建risc-v与xv6开发调试环境</a>的预编译版本，直接再设置个link就可以了
- Test: `riscv64-unknown-elf-gcc -v`
###### riscv64-unknown-elf-gdb
- **注意**：在`riscv64-unknown-elf-gcc -v`能用，`qemu`配置完成（能在xv6的路径下`make qemu`）之前都不要看这个，这一步是为了测试使用`qemu-gdb`对`xv6`进行调试的可行性
- 需要注意的是，这个预编译版本下的`riscv64-unknown-elf-gdb`不work，报一个类似`an incompatible architecture (have '', need 'arm64e')`的错误，应该是版本兼容的问题。
- 所以我只能下载<a href="https://zhayujie.com/mit6828-env.html#comment-187">MIT6.828准备 — risc-v和xv6环境搭建</a>下的`riscv64-unknown-elf-gdb == 8.3.0`预编译版本，提高权限，打开权限，这时报了另一个错
    ```
    Could not load the Python gdb module from 
    /usr/local/opt/riscv-gnu-toolchain/share/gdb/python'
    ```
- 所以只能尝试把别的gdb distribution下的python复制过来，比如可以把brew的gdb下的python挪过来:
    ```
    cp -R /usr/local/Cellar/gdb/10.1/share/gdb/python /usr/local/opt/riscv-gnu-toolchain/share/gdb/python/
    ```
  这时执行`souce .gdbinit`可能会有两种可能：
  - 配置成功！(显示`0x0000000000001000 in ?? ()`)
    - 配置失败 (不显示以上内容，或者直接报错):
      - 失败的原因千千万，对我而言是这样：
      ```
      Python Exception <type 'exceptions.NameError'> Installation error: gdb.execute_unwinders function is missing:
      ```
      明白了，放进去的python并不是`riscv64-unknown-elf-gdb == 8.3.0`想要的python，那就换一个python的版本测试下，对我而言能用的版本是<code>RISC-V toolchain == 10.2.0</code>的`intel`预编译版本的python:
        ```
        riscv-gnu-toolchain/share/gdb/python
        ```

##### QEMU
- 我参考的是<a href="https://github.com/BASARANOMO/xv6-labs-2020/issues/1">Install riscv-tools and qemu on Apple Silicon M1 mac \#1</a>，在打补丁的时候，我使用的是`git apply *.patch`而不是`patch -p1 *.patch`.

##### XV6
- 具体就看你想要的是哪个版本的课了，我用的是2022版本的
- `git clone https://github.com/mit-pdos/xv6-riscv.git`

##### 参考

###### <a href="https://zhayujie.com/mit6828-env.html#comment-187">MIT6.828准备 — risc-v和xv6环境搭建</a>
- 包含<code>RISC-V toolchain == 9.2.0</code>的源码，需要自己编译，详情看帖子
- 包含`riscv64-unknown-elf-gdb == 8.3.0`的版本，需要自己提高权限+开启权限, 详情看帖子


###### <a href="https://cloud.tencent.com/developer/article/1939023">MIT 6.S081/Fall 2020 搭建risc-v与xv6开发调试环境</a>
- 包含<code>RISC-V toolchain == 10.2.0</code>的`intel`和`m1`的预编译，可以直接使用，详情看帖子

###### <a href="https://github.com/BASARANOMO/xv6-labs-2020/issues/1">Install riscv-tools and qemu on Apple Silicon M1 mac \#1</a>
- 包含需要打在`qemu`上的两个补丁，先打补丁，再`configure`，再`make`，再`make install`





