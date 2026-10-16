# Nand2tetris

[Nand2tetris](https://www.nand2tetris.org/) 官方课程骨架的存档仓库。

> **完成度说明（重要）**：本仓库**不是**一个已完成的项目。它基本是官方课程练习骨架的原样上传，
> 我实际写过的代码只有 **Project 1 的 `And` 门**（`projects/01/And.hdl`），其余练习全部保持官方模板的
> 未填写状态。放在这里仅作学习起点的存档。

## 课程是什么

Nand2tetris（配套教材 *The Elements of Computing Systems*，Nisan & Schocken，MIT Press）
是一门「从第一性原理构建现代计算机」的课程：从一个 NAND 逻辑门出发，逐层搭建出一台完整的计算机。
课程分为 12 个项目，横跨硬件与软件两条线：

| 阶段 | 项目 | 内容 |
| --- | --- | --- |
| 硬件 | 01 | 从 Nand 门构建基本逻辑门（Not / And / Or / Xor / Mux / DMux 及 16 位版本） |
| 硬件 | 02 | 算术逻辑单元（HalfAdder / FullAdder / Add16 / Inc16 / ALU） |
| 硬件 | 03 | 时序逻辑（Bit / Register / RAM / PC） |
| 硬件 | 04 | 机器语言编程（Hack 汇编练习 Mult / Fill） |
| 硬件 | 05 | 搭建完整的 Hack 计算机（CPU / Memory / Computer） |
| 软件 | 06 | 编写汇编器 |
| 软件 | 07–08 | 编写虚拟机翻译器（算术/内存访问 → 控制流/函数调用） |
| 软件 | 09 | 用 Jack 语言写一个小程序 |
| 软件 | 10–11 | 编写 Jack 编译器（语法分析 → 代码生成） |
| 软件 | 12 | 编写 Jack 操作系统（内存管理、字符串、数组、数学库、I/O） |
| 软件 | 13 | 课程总结 |

## 仓库结构

```
projects/          官方练习骨架
├── 00/            课程热身（提交 project0.zip）
├── 01/ – 13/      12 个项目的练习文件（.hdl / .asm / .vm / .jack 及对应 .tst / .cmp 测试）
└── demo/          官方示例（Xor.hdl，已随骨架提供实现）

tools/             官方模拟器与编译器全套
├── HardwareSimulator   硬件模拟器（运行 .hdl）
├── CPUEmulator         CPU 模拟器（运行 .hack）
├── VMEmulator          虚拟机模拟器（运行 .vm）
├── JackCompiler        Jack 编译器
├── Assembler           汇编器
├── TextComparer        测试结果比对工具
├── builtInChips/       内置芯片实现
├── builtInVMCode/      内置 VM 代码
└── OS/                 Jack OS 参考实现
```

## 当前完成进度

- ✅ **Project 1 / `And.hdl`** —— 唯一自己写的实现，用 `Nand` + `Not` 拼出 `And`：

  ```hdl
  PARTS:
  Nand(a=a, b=b, out=c);  // use Nand and Not can make And
  Not(in=c, out=out);
  ```

- ⬜ **其余全部未开始** —— `projects/01` 的其他门电路以及 `projects/02`–`13` 的所有 `.hdl` / `.asm` /
  `.vm` / `.jack` 文件都仍是官方模板里的 `// Put your code here:` 占位符，没有填写。
- `projects/demo/Xor.hdl` 是官方随骨架提供的示例，不是我的实现。

## 关于仓库内的教材 PDF

仓库根目录提交了课程教材的 PDF 副本（中文扫描版、英文第二版，以及 `app 2.pdf`、`app 4.pdf` 两个附录）。
**版权归原作者 Noam Nisan、Shimon Schocken 及 MIT Press 所有**，此处仅为个人学习留存。
建议通过官方渠道获取教材：https://mitpress.mit.edu/ 。

## 参考链接

- 课程官网：https://www.nand2tetris.org/
- 官方课程骨架下载：https://www.nand2tetris.org/software
