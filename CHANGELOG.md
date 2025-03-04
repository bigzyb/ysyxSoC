## 2022.10.7
1. 生成memtest版本的sdram测试程序。
2. 重构仿真程序的实现，将hpp的定义和实现分离。
3. 支持自动化生成所有的测试程序。
4. 支持SDRAM的0xFC000000的读写回环测试。
5. 添加VGA的rtl模块和测试程序。
6. 添加帧缓存的verialtor实现。
7. 添加abstract-machine到utils目录中。

## 2022.10.1
1. 添加键盘测试的图片输出支持。
2. 重构了仿真程序下sdl2的初始化设置。
3. 添加了screen外设模拟模块。
4. 修复了verilator下的c++源文件的引入warning。
5. 优化了sdl2的video显示功能。

## 2022.9.28
1. 支持在命令行中对不同信息显示不同颜色。
2. 添加sdram控制器和外设模拟模块。
3. 添加sdram和vga的wrapper模块并更新soc顶层。
4. 添加rtthread线程切换的源码和可执行程序。
5. 修改了chisel下进行寄存器复位检查的命令。
6. 修改了可执行程序的生成脚本以支持rtthread。

## 2022.9.23
1. 修改了文档的多处表述。
2. 修复了提交脚本的语句对齐的bug。
3. 修复了ps模块中读指针的初始化bug。
4. 添加了ps2模拟外设的实现并添加了键盘测试的代码。 

## 2022.9.18
1. 在soc测试单个程序时，添加波形生成代码并更新了readme相关说明。
2. 删除了代码提交部分difftest回归测试的截图要求。

## 2022.9.17
1. 修改多处文档表述。
2. 经过同学提醒，修改了SRAM接口说明部分中有歧义的部分。
3. 添加了verilator报组合逻辑环warning的介绍和处理方法。
4. 添加了AXI4总线实现上需要注意的地方。
>第4项需要大家特别注意，和我们提前对接的同学在跑VCS测试时发现了AXI4总线不要只用ready作为切换状态的信号，因为在VCS上进行仿真的SoC默认ready是一直拉高的，可能会导致同学们的核在VCS仿真下出现AXI4握手和状态机切换问题。

