袁乙钧 \<bbbush@163.com\> 提供了`bash 2` `man`的[中文翻译](http://ahei.info/chinese-bash-man.htm)，感谢袁乙钧的精致和辛勤的翻译工作。

本翻译以上面为基础，所做如下：

1. 更新内容到`bash 3`版本，这是目前生产环境中主流使用的`bash`版本。   
`bash`的各个版本及其发布时间可以从[`bash`下载页面](http://ftp.gnu.org/gnu/bash/?C=M;O=A)确认。
1. 加上内部引用的链接
1. 使用`markdown`排版。优先格式方便查看。
1. 审校翻译。合理地中文化，不在影响理解的情况下尽量减少英文原文。

[自己](http://weibo.com/oldratlee)理解粗浅，翻译中不足和不对之处，欢迎建议（[提交Issue](https://github.com/quickhack/translations/issues)）和指正（[Fork后提交代码](https://github.com/quickhack/translations/fork)）！

Bash man
===============================

![bash](images/bash.png "bash")[.](https://www.behance.net/gallery/7384837/DJ-BASH-Logo-Design)

目录
-------------

1. [名称（NAME）](overview.md#名称（NAME）)
1. [概要（SYNOPSIS）](overview.md#概要（SYNOPSIS）)
1. [版权所有（COPYRIGHT）](overview.md#版权所有（COPYRIGHT）)
1. [描述（DESCRIPTION）](overview.md#描述（DESCRIPTION）)
1. [选项（OPTIONS）](overview.md#选项（OPTIONS）)
1. [参数（ARGUMENTS）](overview.md#参数（ARGUMENTS）)
1. [启动（INVOCATION）](overview.md#启动（INVOCATION）)
1. [定义（DEFINITIONS）](overview.md#定义（DEFINITIONS）)
1. [保留字（RESERVED WORDS）](overview.md#保留字（RESERVED WORDS）)
1. [`shell`语法](#shell语法)
    - [Simple Commands 简单命令](#lbAL)
    - [Pipelines 管道](#lbAM)
    - [Lists 序列](#lbAN)
    - [Compound Commands 复合命令](#lbAO)
1. [注释(COMMENTS)](#lbAP)
1. [引用(QUOTING)](#lbAQ)
1. [参数(PARAMETERS)](#lbAR)
    - [Positional Parameters 位置参数](#lbAS)
    - [Special Parameters 特殊参数](#lbAT)
    - [Shell Variables 变量](#lbAU)
    - [Arrays](#lbAV)
1. [扩展(EXPANSION)](#lbAW)
    - [Brace Expansion](#lbAX)
    - [Tilde Expansion](#lbAY)
    - [Parameter Expansion](#lbAZ)
    - [Command Substitution](#lbBA)
    - [Arithmetic Expansion](#lbBB)
    - [Process Substitution](#lbBC)
    - [Word Splitting](#lbBD)
    - [Pathname Expansion](#lbBE)
    - [Quote Removal](#lbBF)
1. [重定向(REDIRECTION)](#lbBG)
    - [Redirecting Input](#lbBH)
    - [Redirecting Output](#lbBI)
    - [Appending Redirected Output (添加到重定向后的输出尾部)](#lbBJ)
    - [Redirecting Standard Output and Standard Error](#lbBK)
    - [Here Documents](#lbBL)
    - [Here Strings](#lbBM)
    - [Duplicating File Descriptors (复制文件描述符)](#lbBN)
    - [Moving File Descriptors](#lbBO)
    - [Opening File Descriptors for Reading and Writing](#lbBP)
1. [别名(ALIASES)](#lbBQ)
1. [函数(FUNCTIONS)](#lbBR)
1. [算术求值(ARITHMETIC EVALUATION)](#lbBS)
1. [条件表达式(CONDITIONAL EXPRESSIONS)](#lbBT)
1. [简单命令扩展(SIMPLE COMMAND EXPANSION)](#lbBU)
1. [命令执行(COMMAND EXECUTION)](#lbBV)
1. [命令执行环境(COMMAND EXECUTION ENVIRONMENT)](#lbBW)
1. [环境(ENVIRONMENT)](#lbBX)
1. [退出状态(EXIT STATUS)](#lbBY)
1. [信号(SIGNALS)](#lbBZ)
1. [作业控制(JOB CONTROL)](#lbCA)
1. [提示符(PROMPTING)](#lbCB)
1. [readline库(READLINE)](#lbCC)
    - [Readline Notation](#lbCD)
    - [Readline Initialization 初始化](#lbCE)
    - [Readline Key Bindings](#lbCF)
    - [Readline Variables](#lbCG)
    - [Readline Conditional Constructs](#lbCH)
    - [Searching](#lbCI)
    - [Readline Command Names](#lbCJ)
    - [Commands for Moving 移动](#lbCK)
    - [Commands for Manipulating the History 操纵历史行](#lbCL)
    - [Commands for Changing Text 改变文本](#lbCM)
    - [Killing and Yanking 剪切和粘贴](#lbCN)
    - [Numeric Arguments 数值参数](#lbCO)
    - [Completing 补全](#lbCP)
    - [Keyboard Macros 宏](#lbCQ)
    - [Miscellaneous](#lbCR)
    - [Programmable Completion 可编程补全](#lbCS)
1. [历史(HISTORY)](#lbCT)
1. [历史扩展(HISTORY EXPANSION)](#lbCU)
    - [Event Designators](#lbCV)
    - [Word Designators](#lbCW)
    - [修饰符 (Modifiers)](#lbCX)
1. [`shell`内建命令（SHELL BUILTIN COMMANDS）](buildin-command.md#shell内建命令（SHELL BUILTIN COMMANDS）)
1. [受限的shell(RESTRICTED SHELL)](#lbCZ)
1. [参见(SEE ALSO)](#lbDA)
1. [文件(FILES)](#lbDB)
1. [作者(AUTHORS)](#lbDC)
1. [报告BUGS (BUG REPORTS)](#lbDD)
1. [已知`Bug`](#lbDE)