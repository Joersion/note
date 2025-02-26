## 一、交叉编译工具链制作

- 本文介绍了如何在虚拟机的 x86-64 环境下构建一个用于 aarch64 架构的交叉编译工具链。

### 1. 安装软件包来支持工具链

#### 安装步骤

- sudo apt-get install gawk build-essential bison flex texinfo
- sudo apt-get install libncurses5-dev libncursesw5-dev


### 2. 下载 crosstool-ng 构建工具链

#### 下载步骤

- git clone https://github.com/crosstool-ng/crosstool-ng.git
- cd crosstool-ng
- ./bootstrap
- ./configure
- make
- sudo make install


### 3. 配置 crosstool-ng 

- ct-ng menuconfig

#### 3.1 主页面

- [主页面](img/1.png)

#### 3.2 Paths and misc options
- [路径和杂项选项](img/2.png)

#### 3.3 Target options
- [目标选项](img/3.png)

#### 3.4 Toolchain options
- [工具链选项](img/4.png)

#### 3.5 Operating System
- [操作系统](img/5.png)

#### 3.6 Binary utilities
- [二进制工具](img/6.png)

#### 3.7 C-library
- [C 库](img/7.png)

#### 3.8 C compiler
- [C 编译器](img/8.png)

#### 3.9 Linkers
- [链接器](img/9.png)

#### 3.9 Debug facilities
- [调试工具](img/10.png)

#### 3.9 Companion libraries
- [三方库](img/11.png)

#### 3.9 Companion tools
- [三方工具](img/12.png)

#### 3.1 打开配置页面

## 4、Qt Quick Application与Qt Quick Application（compat）区别？

- 不需要支持老旧版本的 Qt，可以优先选择 Qt Quick Application。如果你有现有的 Qt 5 项目，并且需要继续支持老版本，使用 Qt Quick Application (compat) 更合适

## 5、Ninja功能 和 make使用场景？

- Ninja功能简单，构建速度快，如果项目小建议用make就行