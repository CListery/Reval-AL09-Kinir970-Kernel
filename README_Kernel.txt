################################################################################

1. How to Build
- get Toolchain
From android git server, codesourcery and etc ..
- aarch64-linux-android-4.9

- edit Makefile
edit CROSS_COMPILE to right toolchain path(You downloaded).
Ex)   export PATH=$PATH:$(android platform directory you download)/prebuilts/gcc/linux-x86/aarch64/aarch64-linux-android-4.9/bin
Ex)   export CROSS_COMPILE=aarch64-linux-android-

$ mkdir ../out
$ make ARCH=arm64 O=../out merge_kirin970_defconfig
$ make ARCH=arm64 O=../out -j8

2. Output files
- Kernel : out/arch/arm64/boot/Image.gz
- module : out/drivers/*/*.ko

3. How to Clean
$ make ARCH=arm64 distclean
$ rm -rf out
################################################################################


################################################################################

1. 如何编译
- 获取工具链
从 Android git 服务器、CodeSourcery 等来源获取
- aarch64-linux-android-4.9

- 编辑 Makefile
将 CROSS_COMPILE 修改为正确的工具链路径（您下载的路径）。
例如：   export PATH=$PATH:$(您下载的 Android 平台目录)/prebuilts/gcc/linux-x86/aarch64/aarch64-linux-android-4.9/bin
例如：   export CROSS_COMPILE=aarch64-linux-android-

$ mkdir ../out
$ make ARCH=arm64 O=../out merge_kirin970_defconfig
$ make ARCH=arm64 O=../out -j8

2. 输出文件
- 内核：out/arch/arm64/boot/Image.gz
- 模块：out/drivers/*/*.ko

3. 如何清理
$ make ARCH=arm64 distclean
$ rm -rf out
################################################################################