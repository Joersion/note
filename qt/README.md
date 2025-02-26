# Linux 安装 Qt 和创建第一个 Qt 程序

本文介绍了在 Linux 系统上安装 Qt 以及如何创建第一个 Qt 程序的步骤。

## 1. 安装 Qt

参考：[CSDN文章](https://download.csdn.net/blog/column/9267924/132507400) 从清华源下载在线安装程序。

## 2. 创建首个 Qt 程序

### 配置 Kits 套件

- 配置 `Kits` 套件时，如果出现无法配置的情况，说明组件安装不全，需要重新安装。

### 创建 Qt Quick Application

- 选择 `Qt Quick Application`，如果 Qt 程序创建后 CMake 报错，说明可能存在缺少库的问题。

### 安装 OpenGL 依赖库：

- sudo apt-get install libgl1-mesa-dev
- sudo apt-get install libglu1-mesa-dev


### 安装 XKB 依赖库：

- sudo apt-get install libxkbcommon-dev
- 程序还是无法构建，cmake配置不要用Ninja 构建工具，用make作为构建工具

## 3、为什么Qt Quick Application需要依赖openGL?

- 创建 Qt Quick Application 项目时，Qt 自动会将其依赖项设置为 OpenGL 相关的库，以确保能够进行图形渲染和硬件加速。

## 4、Qt Quick Application与Qt Quick Application（compat）区别？

- 不需要支持老旧版本的 Qt，可以优先选择 Qt Quick Application。如果你有现有的 Qt 5 项目，并且需要继续支持老版本，使用 Qt Quick Application (compat) 更合适

## 5、Ninja功能 和 make使用场景？

- Ninja功能简单，构建速度快，如果项目小建议用make就行