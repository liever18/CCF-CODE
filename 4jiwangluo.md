#操作系统原理
##第1章 操作系统概论
- 批处理操作系统的优点是作业流程**自动化较高**，**资源利用率较高**，**作业吞吐量大**，从而**提高了整个系统效率**；批处理操作系统的的缺点是**用户不能直接与计算机交互**，不合适调试程序。

- 常见的操作系统体系结构有**整体式结构**、**层次式结构**和**微内核（客户机/服务器）结构**等。所以在在操作系统的结构设计中，微内核结构表示的是客户机/服务器结构。

- 操作系统的功能主要可以分为**进程管理**（处理器管理）、**存储管理**、**文件管理**、**作业管理**和**设备管理**。

- 操作系统是计算机系统中的一个系统软件，它是这样一些程序模块的集合——它们能有效地组织和管理计算机系统中的硬件和软件资源，合理地组织计算机的工作流程，控制程序的执行，并向用户提供各种服务功能，使用户能够灵活、方便、有效地使用计算机，并使整个计算机系统能高效地运行。

- 硬盘是共享设备，可以被共享。磁带机、投影仪和扫描仪都是独占设备，无法被共享。

- 从**计算机应用**角度来看，操作系统的主要作用是提供**人机交互接口**

- 从**软件设计和开发**角度来看，操作系统是**软件开发基础平台**，屏蔽了管理和控制计算机硬件与软件资源的底层操作，并提供了高层次软件调用的接口。

- 在黑客和网络攻击者看来，操作系统是他们要攻破的第一道防线。所以从**计算机安全保护**角度来看，操作系统的主要作用是提供**第一道安全防线**。

- 从**计算机系统发展**的角度来看的，操作系统是在原来计算机（裸机）扩充成为功能强、使用方便的计算机系统，这种计算机系统称为虚拟计算机。(提供虚拟机、扩展机)

- 操作系统作为系统软件，位于软件系统的硬件之上和**支撑软件之下**的层面。

- 操作系统是计算机系统中的一个系统软件，能有效地组织和管理计算机系统中的硬件和软件资源，合理地组织计算机工作流程，控制程序的执行，并向用户提供各种服务功能，使得用户能够灵活、方便、有效地使用计算机。**“合理”**是指操作系统要**“公平”对待**不同的用户程序，保证系统不发生**“死锁”和“饥饿”**的现象。

- 站在资源管理的观点看，操作系统就是负责记录谁在使用什么样的资源，系统中还有哪些资源空闲，当前响应了谁对资源的要求，以及回收哪些不再使用的资源等，从而对这些资源进行有效的组织和管理，而记录这些信息是通过各种数据结构来实现的

- 操作系统的运行是在一种随机的环境下进行的。这种随机环境的含义是，操作系统不能对所运行的程序的行为以及硬件设备的情况作出任何事先的假定。一般来说，操作系统正处于什么样的状态之中是无法确切知道的，这就是随机性的含义。所以**操作系统内核进行进程切换这一现象具有随机性**

- 在下面列出的计算机操作中，只能在**操作系统内核态**下运行的是(**屏蔽中断**)  
**特权指令**包括输入**输出指令、停机指令**等，只有在监控程序才能执行特权指令，只能在内核态下运行；用户只能执行一般指令，在用户态下运行。屏蔽中断属于特权指令，只能是在系统内核态下运行。

- 用户程序不能直接使用特权指令。如果用户程序在用户态下执行了特权指令，则引起**访管中断**，这也是CPU由用户态向核心态转换的方法。

- 内核提供所有操作系统基本都具有的那些操作，如线程调度、虚拟存储、消息传递、设备驱动以及内核原语操作集和中断处理等。而**用户应用程序**属于**操作系统用户程序**，不属于操作系统内核程序。

- 进程管理实质是对中央处理器进行管理。进程管理主要包括进程控制、进程同步、进程通信和进程调度。其中进程控制的主要任务是创建进程、撤销结束的进程以及控制进程运行时候的各种状态转换；进程同步主要处理进程之间的关系，包括进程的同步和互斥；进程间通信主要处理相互协作进程之间信息的交换问题；而进程调度则是按照一定的算法从就绪队列中挑选一个进程在处理器中真正执行它。**中断服务程序是固定在某个地址的代码段，没有进程的概念。**

- 若**用户编程需要打印输出**，他可使用下列操作系统提供的哪一种系统调用（**write()**）。write()会把参数buf所指的内存写入count个字节到参数fd所指的文件内。当然，文件读写位置也会随之移动。若用户编程需要打印输出，需要系统调用write()。

- 从用户的观点看，操作系统是用户与计算机系统之间的接口，提供给用户的接口是**命令输入**和**系统调用**。

- 当用户程序需要调用操作系统所提供的文件读写功能时，该功能首先执行的指令是（**访管指令**）。

- 内核态和用户态是用于操作系统运行安全而设置的一种状态标志，其含义是指（**CPU在运行时所处的状态**）。

- 系统中还有一类资源，它们在同一时间段可以被多个程序同时访问。一个典型的可以同时共享的资源就是硬盘，当然，那些可以**重入的操作系统代码**也是可以被**同时共享**的。**临界区、中断服务程序和内核调度模块**都是属于**互斥共享**。

- 共享性是操作系统的特征之一，下列哪种软件资源不可以同时共享（  **内存分配模块** ）。

- **中央处理器**以及**存储器**的所有进程都是允许不同程序交替轮流占用它，可**互斥共享**的。

- **并发性**是操作系统的特征之一。下列描述的四种现象中，哪一种具有“并发性”（ **单CPU系统交替运行积分计算和磁盘读写的进程** ）。    
“并发性”是指计算机系统中同时存在若干个运行着的程序，也就是说指两个或者多个事件在同一时间的间隔内发生。

- 下列哪一个状态位不包含在程序状态字（PSW）中（**驻留位（A）**）。  
用一个专门的寄存器来指示处理器状态称为程序状态字（PSW），其包括的状态位有**进位标志位（CF）**、结果为**零标志位（ZF）**、**符号标志位（SF）**、**溢出标志位（OF）**、**陷阱标志位（TF）**、**中断使能（中断屏蔽）标志位（IF）**、**虚拟中断标志位（VIF）**、**虚拟中断待决标志位（VIP）**、**IO特权级别（IOPL）**。

- 用户编写程序时调用**fork()**创建进程，其使用的是操作系统提供给用户的什么接口（**系统调用**）。

- 下列哪一个标志位或状态码不包含在程序状态字（PSW）中（ **修改位（M）** ）。

- 操作系统作为**系统软件**，集中了**资源管理功能**和**控制程序执行功能**

- 分布式操作系统的特点是（ **ABCDE** ）。  
A. 系统内所有主机使用同一个操作系统  
B. 系统内资源深度共享  
C. 用户无需了解系统内本地主机或异地主机的差异，具有透明性  
D. 系统内各主机处于同等地位，不分主次  
E. 系统具有较高的可靠性

- 操作系统的主要功能可以分为处理器管理、存储管理、文件管理、设备管理和用户接口。下列哪些工作属于存储管理范畴（ **ABCDE** ）。  
A. 完成虚拟地址到物理地址的转换  
B. 管理内存分配表  
C. 检查进程地址空间是否出现地址越界问题  
D. 将磁盘上的代码调入内存  
E. 内存扩充

- 存储管理的任务是管理计算机内存的资源。存储管理有三个方面的功能。第一内存的分配与回收：操作系统要为每个进程所占据的内存空间，在分配的过程中，还要尽可能提高内存资源的使用效能。第二存储保护：必须考虑程序可能发生越界的情况，保护整个用户及计算机系统的程序运行。第三内存扩充：借助于虚拟技术在逻辑上增加进程运行空间的大小，这个大小比实际的物理内存大得多。操作系统把正在使用的页面保持在内存中即将使用的页面调入到内存中，用户就感受不到空间使用的限制。

- 操作系统的主要功能可以分为处理器管理、存储管理、文件管理、设备管理和用户接口。下列哪些工作属于文件管理范畴（**BCDE**）。
A. 将磁盘上的代码调入内存
B. 管理磁盘空间
C. 磁盘碎片整理
D. 建立文件目录
E. 设置文件的存取权限

- 文件管理的任务是有效的支持文件的存储、检索和修改等操作，解决文件的共享、保密和保护问题，以使用户方便、安全地访问文件，主要涉及3个方面：文件存储空间的管理、目录管理、文件系统的安全性。其中，管理磁盘空间和磁盘碎片整理都属于文件存储空间的管理；目录管理的主要任务就是给出组织文件的方法，为每个文件建立目录项，并对众多的目录项加以有效的组织，以便为用户提供方便的按名存取；安全性包括文件的读写权限以及存取控制。

- 操作系统的主要功能可以分为处理器管理、存储管理、文件管理、设备管理和用户接口。下列哪些工作属于设备管理和用户接口范畴（**ABCD**）。
A. 为用户程序提供系统调用接口
B. 提供缓冲技术
C. 管理通道、网卡等相关的数据结构
D. 提供虚设备技术
E. 管理磁盘空间

- 设备管理是指计算机系统中除了CPU和内存以外的所有输入、输出设备的管理。由操作系统的设备管理功能负责外部设备的分配，启动和故障处理。在操作系统中，为了提高设备的使用效率和整个系统的运行速度，需要采用一系列的技术，包括中断技术、通道技术、虚拟设备技术和缓冲技术等，尽可能发挥设备和主机的并行工作能力。接口管理的任务是为用户提供一个使用系统良好环境，为用户程序提供系统调用接口。

- 共享性是操作系统的特征之一，所谓“共享性”是指（ **在一定的策略控制下，按不同资源类型共同占有使用**  ）。

- Linux/ **BSD**/DOS均是**操作系统**

- 下列哪些术语是指某一种操作系统的类型（**ABCE**）。  
A. 批处理batch  
B. 交互式interactive  
C. 实时realtime  
D. 多用户multi-user  
E. 分布式distributed

- 当前Android操作系统应用广泛，它具有下列哪些特性（**BC**）。  
A. 批处理  
B. 移动应用  
C. 支持网络  
D. 分布式  
E. 兼容性

- 研究操作系统的观点有多种，它们分别是（ **ABCDE** ）。  
A. 软件的观点  
B. 资源管理的观点  
C. 进程的观点  
D. 虚拟机的观点  
E. 服务提供者的观点

- 操作系统的种类相当多，可分为批处理系统、分时操作系统、实时操作系统、嵌入式操作系统、个人计算机操作系统、网络操作系统等。没有工业操作系统。

- 微内核（客户/服务器）结构的操作系统具有下列哪些优点（ **ABC**  ）。  
A. 高可靠性  
B. 高灵活性  
C. 适合分布式处理  
D. 便捷的通信  
E. 较高的效率

- 分时操作系统的特点是（ **ABCD**  ）。  
A. 多个用户在线同时使用计算机  
B. 便于调试程序  
C. 能够对用户输入的信息及时响应  
D. 用户使用计算机时感觉不到计算机同时在为别人服务  
E. 系统资源利用率较高  
分时操作系统具有**多路性、交互性、独占性和及时性**的特点：  
多路性：多个用户同时使用一台计算机；  
交互性：用户根据系统响应的结果提出下一个请求，方便调试程序；  
独占性：每个用户感觉不到计算机系统为其他人服务，好像整个系统为他个人所独占一样  
及时性：系统能够对用户提出的请求作出及时的响应  

- 实时操作系统的特点是（ **ABC**  ）。  
A. 具有较高的可靠性  
B. 在严格的时间范围内，实时响应用户的请求  
C. 具有较好的过载防护能力  
D. 系统资源的利用率较高  
E. 运行的成本较低

- 批处理操作系统的特点是（ **ABC**  ）。  
A. 成批处理用户提交的作业  
B. 用户无法干预作业的运行  
C. 系统资源利用率较高  
D. 运行的速度快  
E. 运行的成本低

- 在UNIX系统中，若文件File4的权限是736，则表示（ **ABCDE**  ）。  
A. 文件属主可执行File4  
B. 文件属主可读File4  
C. 同组用户可写File4  
D. 同组用户可执行File4  
E. 其他用户可读File4  
在UNIX系统中，若文件File4的权限是736，用二进制表示为111011110，得出文件属主可读写执行File4、同组用户可写执行File4、其他用户可读写File4。

- 操作系统在进行设备分配时根据算法需要查找相应的数据结构，该数据结构包括的主要内容为下列哪几项（ **ABCD**  ）。  
A. 系统设备表  
B. 设备控制表  
C. 控制器控制表  
D. 通道控制表  
E. 设备分配表

##第2章 操作系统运行机制
- 下列各种事件中，不属于I/O中断的事件是（**C**）。  
A. 数据传送完毕  
B. 设备出错  
C. 指令错  
D. 键盘输入  
 I/O中断一般由I/O设备的控制器或者通道发出。I/O中断通常可分为两大类：I/O操作正常结束以及I/O异常。数据传送完毕、设备出错和键盘输入均产生I/O中断。**指令出错属于程序性中断**。

- 机器处于核心态是可以执行硬件所提供的全部指令，包括特权指令和非特权指令，在核心态时可利用特权指令**修改程序状态字**转换为用户态。而用户态转换为核心态**唯一的途径是访管中断**。

- 在操作系统中，既可以在内核态下运行又可以在用户态下运行的指令是（ **D** ）。  
A. 置程序计数器  
B. 清指令寄存器  
C. 清溢出标志  
D. 置移位方向标志

- 处理器一般包括两类寄存器：一类称为用户可见寄存器；第二类称为控制和状态寄存器。**用户可见寄存器**通常所有程序都是可用的，由机器语言直接使用。它一般包括**数据寄存器（又称为通用寄存器）**、**地址寄存器**以及**条件码寄存器**。**对用户不可见的寄存器**有**程序计数寄存器**，它一般由特权指令代码使用。**指令寄存器（IR）**包含了最近取出的指令，属于控制和状态寄存器，**对用户不可见**。

- 中断是由外部事件引发的，而异常则是由正在执行的指令引发的。

- **系统调用**是操作系统提供给**编程人员的唯一接口**。

- 关于操作系统的结构，下列特性中，哪一个不是微内核结构的特点（**A**）。  
A. 清晰的单向依赖和单向调用性  
B. 较高的灵活性和可扩充性  
C. 提高了操作系统的可靠性  
D. 更适合于分布式系统  
**微内核结构的特点：①提高了系统的可扩展性；②增强了系统的可靠性；③可移植性；④适用于对分布式处理的计算环境；⑤融入了面向对象技术。**

- 作系统的主要功能是为管理硬件资源和为应用程序开发人员提供良好的环境来使应用程序具有更好的兼容性，为了达到这个目的，内核提供一系列具备预定功能的多内核函数，通过一组称为系统调用。动态请求和释放系统资源属于操作系统的职责，可以通过系统调用进行。

- 对于函数open()，它属于哪一类系统调用（**A**）。  
A. 文件操作类  
B. 进程控制类  
C. 信息维护类  
D. 通信传输类

- 下列哪一种中断与当前运行的进程有关（ **D** ）。  
A. 故障性中断  //由掉电、存储器校验错等硬件故障引起  
B. 时钟中断  
C. I/O中断  
D. 程序性中断  //由指令执行结果产生，与当前运行的进行有关系

- 中断和异常都是将正常执行的程序打断，完成相应处理后再恢复执行，但是二者是有区别的。下列各种事件中，哪一项属于中断（**A**）。  
A. 网卡上数据缓冲区满  
B. 算术溢出  
C. 内存保护出错  
D. 目态程序试图执行特权指令  

- 系统调用扩充了机器指令，增强了系统功能，方便了用户使用。下列哪一项不属于系统调用（**A**）。  
A. 将一个整型变量转换为浮点数变量  
B. 用户程序需要将本进程休眠  
C. 在硬盘上创建一个公共目录  
D. 进程通过共享内存交换数据  
对于一般通用的操作系统而言，可将其所提供的系统调用分为以下几个方面。  
①**进程控制类**系统调用：这类系统调用主要是用于对进程的控制，如创建和终止进程的系统调用、获得和设置进程属性的系统调用等。  
②**文件操作类**系统调用：对文件进行操纵的系统调用数量较多，有创建文件、打开文件、关闭文件、读文件、写文件、创建一个目录、建立目录、移动文件的读/写指针、改变文件的属性等。  
③**进程通信类**系统调用：该类系统调用被用在进程之间传递消息和信号。  
④**设备管理类**系统调用：该类系统调用被用来请求和释放有关设备，以及启动设备间操作等。  
⑤**信息维护类**系统调用：用户可利用这类系统调用用来获得当前时间和日期。

- **多道程序设计**，就是允许多个程序同时进入内存并运行。引入多道程序设计后，提高了设备资源利用率，使系统中各种设备经常处于忙碌状态，提高了内存资源利用率；同时进入系统中的多个程序可以保存于内存的不同区域中，提高了处理机资源利用率。

- **程序并发执行**是指两个或两个以上程序在计算机系统中同处于已开始执行且尚未结束的状态。程序并发执行产生了一些和程序顺序执行时不同的特性：**①并发程序在执行期间具有相互制约关系；②程序与计算不在一一对应；③并发程序执行结果不可再现。**

- 进程有3种基本状态，在允许抢占的系统中，一个进程从运行状态转换为就绪状态的可能事件是（**A**）。  
A. 分配给该进程的时间片用完  
B. 该进程等待从硬盘上读取文件数据  
C. 该进程等待的数据已经进入内存并准备就绪  
D. 该进程创建完成等待调度  
正在运行的进程由于规定的运行时间片用完而使系统发出超时中断请求，超时中断处理程序把该进程的状态修改为就绪状态。在允许抢占的系统中，一个进程从运行状态转换为就绪状态的可能事件是分配给该进程的时间片用完。

- 系统调用传递参数方法有**陷入指令自带**、**通用寄存器参与**、**专用堆栈区**3种；一般来说，系统子程序所访问的地址空间与用户子程序所访问的地址空间不一样，所以系统子程序访问不了用户提供的变量，也就无法通过用户提供的变量获取参数。

- 系统调用是应用程序请求操作系统核心完成某一特定功能的一种过程调用，与一般调用的最大区别就是**调用程序运行在用户态**，而**被调用程序则运行在核心态**。

- 系统调用与一般过程调用是不同的，下列对被调用程序嵌套使用的描述中，哪一个是正确的（**B**）。  
A. 过程调用和系统调用均不可以嵌套使用  
B. 过程调用和系统调用均可以嵌套使用  
C. 过程调用可以嵌套使用，系统调用不可以嵌套使用  
D. 过程调用不可以嵌套使用，系统调用可以嵌套使用  
系统调用与一般过程调用是不同的，区别主要在于：运行在不同的系统状态，状态的转换，返回问题。但是嵌套使用系统调用与一般过程调用都是允许的，一般情况下，每个系统对嵌套使用的深度都有一定的限制。

- 一般过程调用在被调用过程执行完后，直接返回到调用程序；而系统调用在被调用过程执行完后，系统会对所有要求运行的进程进行优先级分析，若调用进程不具有最高优先级，则会引起重新调度，以便让优先级最高的进程优先执行，即系统会运行调度程序。

- 操作系统的主要功能可以分为处理器管理、存储管理、文件管理、设备管理和用户接口。下列哪些工作属于处理器管理范畴（ **ABCD**）。  
A. 为进程分派CPU  
B. 提供加锁和解锁原语  
C. 管理进程的数据结构  
D. 完成进程上下文切换  
E. 检查进程空间是否有地址越界问题  
**处理器管理**又称为**进程管理**，主要内容是**进程控制、进程同步、进程间通信、调度**。A选项为进程分派CPU属于进程控制；B选项提供加锁和解锁原语属于进程同步；C选项管理进程的数据结构属于进程间通信；D选项完成进程上下文切换属于调度；E选项检查进程空间是否有地址越界问题属于存储管理功能。

- 系统调用由于调用程序和被调用程序运行在不同的系统状态，所以需要通过**软中断机制**，即**陷入机制**，从调用程序所在的用户态转到被调用程序的核心态。

- 进程控制块（PCB）所包含的主要内容有（**ABCD**）。  
A. 进程名  
B. 优先级  
C. 当前状态  
D. 资源清单  
E. 动态链接库  
进程控制块（PCB）的内容可以分成调度信息和现场信息两大部分，调度信息包括进程名、进程号、存储信息、优先级、当前状态、资源清单、"家族"关系、消息队列指针、进程队列指针和当前打开文件等；现场信息只记录哪些可能会被其他进程改变的寄存器，如程序状态字、时钟、界地址寄存器等。

- 下列各类调度算法中，哪些调度算法适用于**交互式**操作系统（ **ADE** ）。  
A. 多级反馈队列  
B. 短作业优先  
C. 最高响应比优先  
D. 时间片轮转  
E. 高优先级优先  
交互式操作系统是指用户交互式地向系统提出命令请求，系统接受每个用户的命令，采用时间片轮转方式处理服务请求，并通过交互方式在终端上向用户显示结果。**多级反馈队列**、**时间片轮转**和**高优先级优先**适用于交互式操作系统。

- 不同的应用领域（以及不同的操作系统）有不同的目标，所以，不同的环境需要不同的调度算法。那么，操作系统通常分为哪几类环境（ **ABC** ）。  
A. 批处理环境  
B. 交互式环境  
C. 实时环境  
D. 顺序环境  
E. 并发环境  
不同的应用领域中，可以将系统分为三类环境：**批处理环境**、**交互式环境**和**实时环境**。

- 在**批处理**操作系统中，可以采用的作业调度算法有哪几种（ **ABC** ）。  
A. 先来先服务  
B. 高响应比优先  
C. 高优先级优先  
D. 时间片轮转  
E. 多级反馈队列算法  
批处理系统常用的调度算法有：**先来先服务**、**最短作业优先**、**最短剩余时间优先**、**响应比最高者优先**。

- 一般系统中产生的事件分为中断和异常两类。下列哪些事件属于中断事件（ **ABCD** ）。  
A. 时钟中断  
B. 输入/输出中断  
C. 控制台中断  
D. 硬件故障中断  
E. 用户程序执行了特权指令  
中断是指CPU对系统中或系统外发生的异步事件的响应，典型的中断包括：**时钟中断**、**输入输出（I/O）中断**、**控制台中断**和**硬件故障中断**。异常则是由正在执行的指令引发的，典型的异常包括：**程序性中断**和**访管指令异常**。

- 对于**交互式系统**，特别是分时系统和服务器，则有不同的指标，最重要的是**响应时间**，即从发出命令到得到响应之间的时间，响应时间越快越好。另外一个是**较均衡的性能**。

##第3章 进程线程模型

##第6章 文件管理
- 文件的存取方式依赖于 （ **D** ）。  
Ⅰ.文件的物理结构  
Ⅱ.文件的逻辑结构  
Ⅲ.存放文件的设备的物理特性   
A. 仅Ⅰ  
B. 仅Ⅱ  
C. 仅Ⅰ和Ⅱ  
D. 仅Ⅰ和Ⅲ  

- 外存储器是属于块设备，**分配空间时常以物理块来分配**，因此为方便与其他设备传输数据文件也是按块进行划分的，称为**数据块**。

- **文件系统的一个特点是“按名存取”**，即用户只要给出文件的符号名就能方便地存取在外存空间的该文件信息而不必了解和处理文件的具体物理地址。因此对于用户而言，**文件名犹为重要**。从**用户角度**来看，**实现按名存取是文件系统的主要目标**。

- **顺序结构的缺点**是随着文件不停地被分配和被删除，空闲空间逐渐被分隔为很小的部分，最终导致**出现存储碎片**，需要**采用不连续分配**来解决小碎片无法分配的问题。

- 建立**树型目录结构**主要有3个优点：**层次清楚**、**解决文件重名问题**和**查找搜索速度快**。从**用户角度**来看，最主要体现出的目标就是**解决文件重名问题**。

- 链接结构的存储方式是一个文件的信息存放在若干不连续的物理块中，各块之间通过指针连接，前一个物理块指向下一个物理块。**链接结构的主要缺点是：存取速度慢，不适于随机存取。**

- 下列关于文件系统中文件的描述中，哪一个是正确的（ **A** ）。  
A. **构成文件内容的基本单位称为信息项**  
B. 文件的内容没有顺序关系  
C. 文件内容都是由操作系统解释并使用的  
D. 用户需要关注文件在磁盘上的存储位置  
文件可以被解释为一组带标识的、在逻辑上有完整意义的信息项的序列。这个标识为文件名，信息项构成了文件内容的基本单位。这些信息项是一组有序序列，它们之间具有一定的顺序关系。从操作系统的角度看文件系统需要关注文件存储位置。

- 下列关于文件系统中文件的描述中，哪一个是错误的（ **C** ）。  
A. 特殊文件通常与设备驱动程序紧密关联  
B. 对于系统文件，只允许用户通过系统调用对它们进行访问  
C. Linux 的 EXT2 文件系统不**区分**文件名的大小写  
D. 目录文件属于系统文件

- 下列关于文件系统中文件的描述中，哪一个是错误的（ **C** ）。  
A. **UNIX 操作系统中将 I/O 设备看作是特殊文件**  
B. **从使用角度关注文件的组织形式称为文件的逻辑结构**  
C. 从查找文件角度关注文件的组织方式称为文件的物理结构  
D. **保存在永久性存储介质上以备查证和恢复时使用的文件称为档案文件**

- 下列哪一种方法不能用于**提高文件目录检索效率**（ **A** ）。  
A. 限制子目录个数  
B. **引入当前目录**  
C. **采用相对路径文件名**  
D. **将目录项分解**

- 在文件系统中，必须为每个文件建立一个至少包含文件名和文件物理存储地址的数据结构，称为（**A**）。  
A. **文件控制块**  
B. 文件分配表  
C. 索引节点  
D. 文件描述符

- 可以把文件划分成3类**逻辑结构**：**无结构的字符流式文件、定长记录文件和不定长记录文件构成的记录树**。

- 常用的文件**物理结构**有**顺序结构、链接结构、索引结构和I节点结构**。

- 下列文件物理结构中，**适合随机访问且易于文件扩展**的是（ **B** ）。  
A. 连续结构  
B. **索引结构**  
C. 链式结构且磁盘块定长  
D. 链式结构且磁盘块变长  
索引结构的文件把每个物理盘块的指针字集中存放在被称为索引表的数据结构中的内存索引表中。**索引结构文件既适于顺序存取，也适于随机存取。索引文件可以满足文件动态增长的要求，也满足了文件插入、删除的要求**。

- **文件控制块**（FCB）。FCB一般应包括下列的文件属性信息：**文件标志和控制信息、文件逻辑结构信息、文件物理结构信息、文件使用信息和文件管理信息**。  

- 文件控制块FCB是系统为管理文件而设置的一个数据结构，它记录了系统管理文件所需要的全部信息，包括：**文件名、文件号、用户名、文件长度、文件类型、文件属性、共享计数、文件的建立日期、保存期限、最后修改日期、最后访问日期、口令**等。
-对需要经常进行访问的文件，下列各选项中，哪一类文件最适合连续存取（ **A** ）。  
A. **顺序文件**  
B. 链接文件  
C. 记录式文件  
D. 索引文件  
顺序文件是指：将一个文件中逻辑上连续的信息存放到存储介质的依次相邻的块上便形成顺序结构，这类文件叫连续文件，又称顺序文件。**顺序结构支持连续存取和随机存取**。

- 下列哪一项是执行打开文件操作时由操作系统返回的（ **C** ）。  
A. 文件名  
B. 文件号  
C. **文件描述符**  
D. 文件物理位置  

- 下列哪一个属性是执行创建文件操作时不需要设置的（ **C** ）。  
A. 文件名  
B. 文件号   
C. **文件描述符**  
D. 文件长度

- 下列关于文件的各种属性信息中，哪一项不是位于文件控制块(FCB)中的（**D**）。  
A. 文件用户名  
B. 文件访问口令  
C. 文件修改日期  
D. **文件分配表**

- 下列关于文件的各种属性信息中，哪一项不是位于文件控制块(FCB)中的（**D**）。  
A. 文件共享计数  
B. 文件类型  
C. 文件创建日期  
D. **用户打开文件列表**

- 通常**二进制可执行文件**采用下列哪一种文件的逻辑结构（**A**）。  
A. **流式结构**  
B. 定长记录结构  
C. 不定长记录结构  
D. 索引顺序结构

- 使用文件前要先打开文件。在成功执行打开文件系统调用后，系统会返回给用户一个（ **C** ）。  
A. 文件长度  
B. 内存地址  
C. **文件描述符**  
D. 文件打开方式

- 下列哪一项**不是**打开文件时所做的工作（ **A** ）。  
A. **填写文件控制块中的文件读写方式**  
B. 检查文件名所对应的文件控制块是否已调入内存  
C. 检查操作的合法性  
D. 返回给用户一个文件描述符  
打开文件时，系统主要完成以下工作：①根据文件路径名查目录，找到FCB主部；②根据打开方式，共享说明和用户身份检查访问合法性；③根据文件号查系统打开文件表，看文件是否已被打开；④在用户打开文件表中取一空表项，填写打开方式等，并指向系统打开文件表对应表项。系统返回用户文件描述符fd，用于以后读写文件。

- 使用文件系统时，通常要显式地进行**open()操作**，这样做的目的是（ **A** ）。  
A. **将文件控制块（FCB）读入内存**  
B. 将文件控制块（FCB）写入磁盘或缓存  
C. 将文件内容读入内存  
D. 将文件内容写入磁盘或缓存

- 使用文件系统时，通常要显式地进行close()操作，这样做的目的是（ **B** ）。  
A. 文件控制块读入内存  
B. **将文件控制块写入磁盘或缓存**  
C. 将文件内容读入内存  
D. 将文件内容写入磁盘或缓存  
执行“关闭”操作时，文件系统主要完成如下工作：①将活动文件表中该文件的“当前使用用户数”减1；若此值为0，则撤销此表目，并保存文件控制块写入磁盘或者缓存；②若活动文件表目内容已被改过，则表目信息应复制到文件存储器上相应表目中，以使文件目录保持最新状态；③卷定位工作，一个关闭后的文件不能再使用，若要再使用，则必须再次执行“打开”操作。

- 操作系统中，**文件的逻辑块号到磁盘块号的转换**是由下列哪一项决定的（ **B** ）。  
A. 逻辑结构  
B. **物理结构**  
C. 目录结构  
D. 调度算法

- 下列对文件的描述中，哪一项与文件的物理结构相关（ **B** ）。
A. 文件长度  
B. **用户对文件的存取方式**  
C. 文件中记录的个数  
D. 文件目录的结构

- 访问磁盘时间分为3部分：寻道时间Ts，旋转延时时间Tr和传输时间Tt，其中，**寻道时间是机械动作的时间，因而所花费的时间最长，最短的是传输时间**。

- **外存储设备存取的过程**大致是：**读状态→置数据→置地址→置控制→**读状态...，如此重复。

- 下列关于实现创建文件操作的描述中，哪一个是**错误**的（ **D** ）。  
A. 创建文件操作完成后，该文件得到一个新的文件控制块（FCB  
B. 创建文件操作完成后，操作系统给该文件分配一定的存储空间  
C. 实现创建文件操作时，需要检查文件名的合法性  
D. **实现创建文件操作时，需要检查文件的存取权限是否合法**

- 下列关于用户打开文件表的叙述中，哪一个是**错误**的（ **A** ）。  
A. **整个系统设置一张用户打开文件表**  
B. 该表中记录了打开文件时系统返回的文件描述符  
C. 该表中应包含指向系统打开文件表的指针  
D. 该表中记录了本次文件被打开的方式

- 下列关于系统打开文件表的叙述中，哪一个是**错误**的（ **D** ）。  
A. 该表是操作系统为每一个打开的文件保存的一个数据结构  
B. 该表保存了文件控制块中的信息  
C. 该表中必须记录是否有多个进程打开了同一个文件  
D. **该表中表项的内容不允许被修改**

- 进程在**打开一个文件**的过程中，下列哪一个操作顺序是正确的（ **B** ）。  
A. 检查打开方式 → 检查用户身份 → 查找FCB主部 → 填写进程打开文件表  
B. **查找FCB主部 → 检查打开方式 → 检查用户身份 → 填写进程打开文件表**  
C. 检查用户身份 → 检查打开方式 → 查找FCB主部 → 填写进程打开文件表  
D. 检查打开方式 → 查找FCB主部 → 检查用户身份 → 填写进程打开文件表

- 进程在**创建文件的过程**中，下列哪一个操作顺序是正确的（ **A** ）。  
A. **检查参数合法性 → 检查重名 → 查找FCB空闲位置 → 填写FCB**  
B. 查找FCB空闲位置 → 检查参数合法性 → 检查重名 → 填写FCB  
C. 检查参数合法性 → 查找FCB空闲位置 → 检查重名 → 填写FCB  
D. 检查重名 → 查找FCB空闲位置 → 检查参数合法性 → 填写FCB

- 某进程在运行过程中**修改了打开文件的内容，当进程关闭该文件时，下列哪一个操作顺序是正确的**（**C**）。  
A. 修改FCB相关内容 → 查找文件 → 置FCB为“非活跃” → 写回磁盘  
B. 查找文件 → 置FCB为“非活跃”→ 修改FCB相关内容 → 写回磁盘  
C. **查找文件 → 修改FCB相关内容 → 置FCB为“非活跃” → 写回磁盘**  
D. 置FCB为“非活跃” → 查找文件 → 修改FCB相关内容 → 写回磁盘

- 进程在**删除**一个文件的过程中，下列哪一个操作顺序是正确的（**C**）。  
A. 检查删除合法性 → 收回FCB资源 → 查找文件 → 收回文件存储空间  
B. 查找文件 → 删除对应FCB资源 → 收回FCB资源 → 收回文件存储空间  
C. **查找文件 → 检查删除合法性 → 收回FCB资源 → 收回文件存储空间**  
D. 检查删除合法性 → 查找文件 → 收回FCB资源 → 收回文件存储空间

- 下列选项中，哪一项不是构成文件目录的必需信息（**C**）。  
A. 文件存取控制信息  
B. 文件结构信息  
C. **文件路径信息**  
D. 文件管理信息

- 第58题





##第7章 I/O设备管理
- 为了实现设备的独立性，系统必须设置一张逻辑设备表，用于将应用程序中所用的逻辑设备名映射为物理设备名。在该表每个表目中有三项：逻辑设备名、物理设备名和设备驱动程序入口地址。系统设备表SDT，在SDT中每个接入系统中的设备都有一个表目项。登录了设备的名称，标识设备控制表DCT的入口地址等相关信息。全面反映了系统中的外设资源的情况，**逻辑设备与物理设备之间对应关系**等。

- 按信息组织形式来划分设备，可以把I/O设备划分为字符设备和块设备。键盘、终端、打印机等以字符为单位组织和处理信息的设备被称为字符设备；而磁盘、磁带等以数据块为单位组织和处理信息的设备被称为块设备。

- I/O设备的控制方式有程序直接控制方式、中断控制方式、DMA方式和通道控制方式。其中，DMA方式一般用于高速传送组成的数据，优点是操作均由硬件电路实现，传输速度快。磁盘的I/O控制主要采用的是DMA方式。

- 设备管理是操作系统的主要功能之一，其主要目的是要建立一个通用的、一致的设备访问接口，使用户和应用程序开发人员能够**方便地使用**输入/输出设备。

- 设备管理的主要任务有：**缓冲区管理**、**设备分配**、**设备处理**、**虚拟设备**以及**实现设备独立性**。其中，缓冲管理功能就是通过缓冲技术匹配高、低速设备交换数据的。通过**虚拟技术**将一台独占设备虚拟成多台逻辑设备，供多个用户进程同时使用，提高**设备并发度**。其中，缓冲池属于操作系统空间，用户程序不能直接对其进行操作，只能通过系统调用进入操作间接使用它们。

- 设备管理的任务主要表现在以下方面：  
①操作系统主要通过缓冲技术、中断技术和虚拟技术来解决I/O设备系统的性能；  
②操作系统需要在设备管理和系统的其他部分之间提供简单而易于使用的接口；  
③对于设备拥有着而言，多用户多任务环境中的设备使用应该通过协调避免冲突，设备不能被破坏。  

- 与**设备无关的系统软件**的作用是为用户进程提供一个管理I/O功能的接口。该层将经过设备驱动程序所抽象的设备看做逻辑资源进行管理，通过该层用户根据设备标识符和诸如打开、读、写和关闭等逻辑操作所提供的统一接口来处理设备，**提供一致的系统调用**。该层实现了与具体I/O设备无关的功能。

- 设备管理的任务主要表现是  
①I/O设备的性能经常成为系统性能的瓶颈。CPU性能越高，I/O设备性能同CPU性能不匹配的反差也越大。操作系统主要是通过缓冲技术、中断技术、和虚拟技术解决这个问题；  
②为了实现对I/O设备统一的管理，操作系统需要在设备管理和系统的其他部分之间提供**简单而易于使用的接口**，这个接口对所有设备都是相同的；  
③用户对I/O设备的使用都必须是**安全**的。

- **缓冲技术**是计算机系统中常用的技术。一般，凡是数据到达速度和离去速度不匹配 的地方都可以通过设置缓冲区，以**缓解处理机与设备之间速度不匹配的矛盾**，**并减少对CPU的I/O中断次数从而提供资源利用率和系统效率**。

- 在操作系统的I/O管理中，**缓冲池管理**中着重考虑的是**实现进程访问缓冲区的同步**。

- **设备独立层**：用于**实现用户程序与设备驱动器的统一接口、设备命令、设备保护、以及设备分配与释放**等，同时为设备管理和数据传送提供必要的存储空间。

- 在设备分配算法中，常采用的数据结构主要含4张表，即**系统设备表SDT→设备控制表DCT→控制器控制表COCT→通道控制表CHCT**。

- 程序直接控制方式，利用输入/输出指令或询问指令测试一台设备的忙/闲标志位，根据设备当前的忙或闲的状态,决定是继续询问设备状态还是由主存储器和外围设备交换一个宇符或一个字。

- CPU与外设在大部分时间内并行工作。当CPU启动外设后，不需要去查询其工作状态，可继续执行主程序，该I/O设备控制方式称为（ **B** ）。  
A. 程序直接控制方式  
B. 中断控制方式  
C. DMA方式  
D. 通道控制方式  

- 系统引入一个**不同于CPU的特殊功能处理单元，它有自己的指令和程序，可以实现对外围设备的统一管理和外围设备与内存之间的数据传送**，该I/O设备控制方式称为（ **D** ）。  
A. 程序直接控制方式  
B. 中断控制方式  
C. DMA方式  
D. 通道控制方式

- 通道是一个独立于CPU的专门I/O控制的处理机，控制设备与内存直接进行数据交换。通道按照信息交换方式通常设立3种类型的通道：**字节多路通道、数据选择通道和数组多路通道**。（无顺序通道一说）

- 在I/O软件的层次中，设备无关软件层实现的主要功能是（ **B** ）。  
A. 保存和记录设备的物理名称  
B. 提供与设备无关的逻辑块  
C. 为设备提供缓冲区空间  
D. 对用户屏蔽出错来源  
与设备无关的系统软件主要功能是（**1）统一命名（2）设备保护（3）提供与设备无关的逻辑块（4）缓冲（5）存储设备的块分配（6）独占设备的分配和释放（7）出错处理。**其中在软件层实现的功能有2、3、6，物理层实现的主要功能有1、4、5、7。？？？数字错了吧？？？

- 设备无关软件层实现的功能有：**设备驱动程序的同一接口、设备命名、设备保护、提供一个与设备无关的逻辑快、缓冲、存储设备的块分配、独占设备的分配和释放、出错处理**。

- 下面列出的各种方法中，哪一项可以提高I/O性能（**A**）。  
A. 应用缓冲技术以减少或缓解不同设备之间传输速度的差距  
B. 应用多核技术使多个进程与I/O同时工作  
C. 应用多级存储架构以提高I/O设备的性价比  
D. 通过设备独立软件提供多种设备的接口

- **进程饥饿**，指当等待时间给进程推进和响应带来明显影响称为进程饥饿。当饥饿到一定程度的进程在等待到即使完成也无实际意义的时候称为饥饿死亡。而进程的**优先级**决定了进程进入运行状态的先后。

- **SPOOLing技术**实际上是一种**外围设备同时联机操作技术**，又称为**排队转储技术**。它在输入和输出之间增加了“输入井”和“输出井”的排队转储环节。  

- 不同的I/O设备可以并行工作。

- 当用户使用外部设备时，其**控制设备的命令传递**途径依次为：**用户应用层→设备独立层→设备驱动层→设备硬件**。

- **高速缓存不是缓冲**，在计算机存储系统的层次结构中，介于中央处理器和主存储器之间的**高速小容量存储器**。它和主存储器一起构成一级的存储器。高速缓冲存储器和主存储器之间信息的调度和传送是**由硬件自动进行的**。

- 在I/O设备管理中，设立设备独立层的主要目的是（ **D** ）。  
A. 将独占设备转换为共享设备，提高了设备利用率  
B. 增加了设备的并行性，简化了设备分配  
C. 避免进程因竞争设备而产生死锁  
D. 屏蔽了I/O设备驱动的多样性，便于用户使用  
设立设备独立层的主要目的是用于**实现用户程序与设备驱动器的统一接口、设备命令、设备保护、以及设备分配与释放等，同时为设备管理和数据传送提供必要的存储空间**。

- 计算机系统中拥有各种软硬件资源，内存是属于（ **A** ）。  
A. 可重用资源  
B. 不可重用资源  
C. 临界资源  
D. 共享资源

- 计算机系统中拥有各种软硬件资源，时钟中断是属于（ **B** ）。  
A. 可重用资源  
B. 不可重用资源  
C. 临界资源  
D. 共享资源

- 下列描述的现象中，对应死锁的四个必要条件中的**“请求和保持”**条件的是（ **B** ）。  
A. 没有采用SPOOLing技术的系统中，进程P1和P2同时申请使用同一台打印机  
B. 进程P1拥有打印机并申请扫描仪  
C. 进程P1额外申请内存不成功，则持有原有的内存进入阻塞状态  
D. 进程P1等待P2完成视频解压缩的信号，P2正等待P1发来的解压数据  
**产生死锁的四个必要条件：互斥条件、请求与保持条件、不剥夺条件、循环等待条件。**“请求和保持”条件又称部分分配或占有申请。进程每次申请它所需要的一部分资源，在申请新的资源的同时，继续占用已分配的资源。进程P1和P2同时申请使用同一台打印机属于互斥条件，进程P1拥有打印机并申请扫描仪属于请求与保持条件，进程P1额外申请内存不成功，则持有原有的内存进入阻塞状态是不剥夺条件，进程P1等待P2完成视频解压缩的信号，P2正等待P1发来的解压数据发生死锁。

- 下列描述的现象中，对应死锁的四个必要条件中的**“循环等待”**条件的是（**D**）。  
A. 没有采用SPOOLing技术的系统中，进程P1和P2同时申请使用同一台打印机  
B. 进程P1拥有打印机并申请扫描仪  
C. 进程P1额外申请内存不成功，则持有原有的内存进入阻塞状态  
D. 进程P1等待P2完成视频解压缩的信号，P2正等待P1发来的解压数据  
循环等待又称环路等待。在发生死锁时，必然存在一个进程等待队列{P1，P2，……，Pn}，其中P1等待P2占有的资源，P2等待P3占有的资源，……，Pn等待P1占有的资源，形成一个进程等待的环路。环路中每一个进程已占有的资源同时被另一个进程所申请，即前一个进程占有后一个进程所请求的资源。

- 下面列出的各种方法中，哪一项可用于死锁检测与恢复（**D**）。  
A. 使用银行家算法  
B. 按序分配资源  
C. 一次性分配所需要的资源  
D. 定时为进程设置还原点，若运行受阻则退回还原点

- 根据进程对设备使用的申请，适用于设备分配的算法主要包括（ **AB** ）。  
A. 先来先服务  
B. 高优先级优先  
C. 时间片轮转  
D. 共享设备优先  
E. 独占设备优先  
I/O设备分配算法有两种：先来先服务算法和最优先级优先（Priority）算法。

- I/O设备数据传送控制方式中，实现中断控制方式需要下列哪些关键部件（ **ABC** ）。  
A. **中断控制器**  
B. **地址总线和数据总线**   
C. **设备控制器**  
D. 设备数据缓冲区  
E. 设备状态寄存器

- I/O设备数据传送控制方式中，实现程序直接控制方式需要下列哪些关键部件（ **ABCDE** ）。  
A. **设备状态寄存器**  
B. **地址总线和数据总线**  
C. **设备控制寄存器**  
D. **设备数据缓冲区**  
E. **地址译码器**  

- I/O设备数据传送控制方式中，实现DMA控制方式需要下列哪些关键部件（**AB**）。  
A. **DMA控制器**  
B. **地址总线和数据总线**  
C. 设备控制器  
D. 设备数据缓冲区  
E. 设备状态寄存器

- I/O设备数据传送控制方式中，**实现通道控制方式**需要下列哪些关键的软硬件部件（**ABCD**）。  
A. **通道控制器**  
B. **地址总线和数据总线**  
C. **设备控制器**  
D. **通道程序代码**  
E. 设备状态寄存器

- 一个典型的计算机I/O系统中，外存设备控制器可以连接下列哪些设备（**ABC**）。  
A. **光盘驱动器**  
B. **磁带驱动器**  
C. **磁盘驱动器**  
D. 激光打印机  
E. 数据通信设备 

- 利用**虚拟技术**进行设备管理的主要目的是（ **A** ）。  
A. **提高设备并发度**  
B. 加速数据传输  
C. 预防死锁发生  
D. 连接不同种类的设备  
一般计算机系统中的独占设备是有限的，往往不能满足诸多进程的要求，因而会引起大量进程由于等待某个独占设备而阻塞，成为系统的瓶颈，另外申请到独占设备的进程在其整个运行期间虽然占有设备，利用率却很低，设备还经常处于空闲状态，为了解决这种矛盾，引入虚拟技术，利用虚拟技术进行设备管理，是通过虚拟技术把独占设备改造成可由多个进程共享的设备，从而提高设备的并发度，提供设备的利用率。

- 设备与CPU之间数据传送和控制方式有多种，它们是（**ACDE**）。  
A. **程序直接控制方式**  
B. 设备控制方式  
C. **中断控制方式**  
D. **DMA方式**  
E. **通道控制方式**

- I/O设备管理中，I/O软件的层次结构有（ **ABCD** ）。  
A. **用户应用层**  
B. **设备独立层**  
C. **设备驱动层**  
D. **中断处理层**  
E. 设备执行层

- 在程序控制I/O方式中，若输出设备向处理机返回“准备就绪”信号，则表示（**AE**）。  
A. **输出缓冲区已空**  
B. 输出缓冲区已存满数据  
C. 输出设备已开始工作  
D. 输出设备已工作完毕  
E. **可以向输出缓冲区写数据**

- 在进行**设备分配**时应该考虑下列哪些因素（ **ABCD** ）。  
A. **设备固有属性**  
B. **设备分配算法**  
C. **设备分配的安全性**  
D. **设备独立性**  
E. 设备分配的及时性

- 下列各项中，哪些是**通道类型**（ **ABC** ）。  
A. **字节多路通道**  
B.** 数据选择通道**  
C. **数组多路通道**  
D. 菊花链通道  
E. 令牌通道

- **SPOOLing系统**的主要组成部分是（ **ABC** ）。  
A. **输入井和输出井**  
B. **输入缓冲区和输出缓冲区**  
C. **输入进程和输出进程**  
D. 输入控制器和输出控制器  
E. 输入分配器和互斥分配器

- 计算机**I/O系统的硬件结构**主要包含（ **BCD** ）。  
A. 中央处理器CPU  
B. **适配器和接口部件**  
C. **设备控制器**  
D. **设备硬件**  
E. 主存储器  

- 计算机**I/O系统的软件部分**主要包含下列哪些项（ **ABCD** ）。  
A. **中断处理程序**  
B. **设备驱动程序**  
C. **与设备无关的操作系统软件**  
D. **用户级软件**  
E. 硬件描述层软件

- 为了提高设备和CPU的利用率，操作系统在I/O管理中采用了多种技术，其中典型的**I/O技术**包括（ **ABCD** ）。  
A. **缓冲技术**  
B. **设备分配技术**  
C. **SPOOLing技术**  
D. **DMA与通道技术**  
E. 级联及堆叠技术

- 按设备的共享属性分类，属于独占设备的是（ **ABC** ）。  
A. **打印机**  
B. **扫描仪**  
C. **时钟发生器**  
D. 串行通信端口  
E. 硬盘

- 采用通道技术的计算机系统中，**通道的功能**包括（ **ABCDE** ）。  
A. **接受CPU的指令，按指令要求与指定的外部设备进行通信**  
B. **从内存读取该通道指令并执行，向设备发送各种命令**  
C. **组织外部设备和内存之间进行数据传送**  
D. **从外部设备得到设备的状态信息，供CPU使用**  
E. **将外部设备的中断请求和通道本身的中断请求，按序及时报告CPU**

- 按信息组织形式来划分设备，可以把I/O设备划分为字符设备和块设备。**键盘、终端、打印机**等以字符为单位组织和处理信息的设备被称为**字符设备**；而**磁盘、磁带**等以数据块为单位组织和处理信息的设备被称为**块设备**。

##第8章 死锁
- 下列描述的现象中，属于活锁的是（ **C** ）。  
A. 相关进程进入阻塞状态，且无法唤醒  
B. 相关进程没有阻塞，但是调度被无限推后  
C. **相关进程没有阻塞，可被调度，但是没有进展**  
D. 相关进程进入阻塞状态，且可以唤醒  
活锁指的是任务或者执行者**没有被阻塞**，由于某些条件没有满足，导致一直重复尝试，失败，尝试，失败。活锁和死锁的区别在于活锁的实体是在不断的改变状态，活锁有可能自行解开，死锁则不能。

- 下列描述的现象中，属于"饥饿"的是（ **C** ）。  
A. 相关进程进入阻塞状态，且无法唤醒  
B. 相关进程没有阻塞，可被调度，但是没有进展  
C. **相关进程没有阻塞，但是调度被无限推后**  
D. 相关进程进入阻塞状态，且可以唤醒  

- 下列描述的现象中，哪一个是由于进程 P1、P2 因**申请不同类资源**而产生死锁的现象（ **D** ）。  
A. P1申请一页内存，P2申请一页内存；P1释放一页内存，P2释放一页内存
B. P1和P2先进行同步信号量P操作，再进行互斥信号量P操作  
C. P1等待接收P2发来的信件Q后向P2发送信件R；P2等待接收P1发来的信件R后向P1发送信件Q后向P1发送信件Q  
D. **P1拥有设备A，请求设备B；P2拥有设备B，请求设备A**

- 下列描述的现象中，哪一个是由于进程P1、P2 因**使用临时性资源**产生死锁的现象（ **D** ）。  
A. P1 拥有设备 A，请求设备 B；P2 拥有设备 B，请求设备 A  
B. P1 申请一页内存，P2 申请一页内存；P1 释放一页内存，P2 释放一页内存  
C. P1 和 P2 先进行同步信号量 P 操作，再进行互斥信号量 P 操作  
D. **P1 等待接收 P2 发来的信件 Q 后向 P2 发送信件 R，P2 等待接收 P1 发来的信件 R 后向 P1 发送信件 Q**

- 下列描述的现象中，哪一个是由于进程 P1、P2因**同步互斥机制使用不当**而产生死锁的现象（ **C** ）。  
A. P1拥有设备 A，请求设备 B；P2 拥有设备 B，请求设备 A  
B. P1 申请一页内存，P2 申请一页内存；P1 释放一页内存，P2 释放一页内存  
**C. P1 和 P2 先进行互斥信号量 P 操作，再进行同步信号量 P 操作**  
D. P1 等待接收 P2 发来的信件 Q 后向 P2 发送信件 R，P2 等待接收 P1 发来的信件 R 后向 P1 发送信件 Q

- 下列描述的现象中，对应死锁的四个必要条件中的“互斥”条件的是（ **A** ）。  
A. **没有采用SPOOLing技术的系统中，进程P1和P2同时申请使用同一台打印机**  
B. 进程P1拥有打印机并申请扫描仪  
C. 进程P1额外申请内存不成功，则持有原有的内存进入阻塞状态  
D. 进程P1等待P2完成视频解压缩的信号，P2正等待P1发来的解压数据  
打印机是临界资源，一段时间内只能被一个进程占用，所以P1、P2必须互斥使用打印机，属于“互斥”条件。进程P1拥有打印机并申请扫描仪，属于**“请求和保持”**条件。进程P1额外申请内存不成功，则持有原有的内存进入阻塞状态，属于**“不可抢占”**条件。进程P1等待P2完成视频解压缩的信号，P2正等待P1发来的解压数据，属于**“环路等待”**条件。

- 下列关于死锁与安全状态的叙述中，哪一个是正确的（ **A** ）。  
A. **死锁状态一定是不安全状态**  
B. 从安全状态有可能进入死锁状态  
C. 不安全状态就是死锁状态  
D. 死锁状态有可能是安全状态  
安全状态是指如果存在一个由系统中所有进程构成的安全序列{P1……Pn}，则系统处于安全状态；如果不存在任何一个安全序列，则系统处于不安全状态。系统处于安全状态则不会发生死锁，不安全状态一定导致死锁，但不安全状态不一定是死锁状态。

- **银行家算法**是一种最有代表性的**避免死锁**的算法，又被称为**“资源分配拒绝”**法。在避免死锁方法中允许进程动态地申请资源，但系统在进行资源分配之前，应先计算此次分配资源的安全性，若分配不会导致系统进入不安全状态，则分配，否则等待。

- 解决死锁问题有多种方法，其中**资源有序分配法**属于（ **B** ）。  
A. 死锁避免  
B. **死锁预防**  
C. 死锁解除  
D. 死锁检测

- 某系统中，进程A正在使用打印机，同时又要申请绘图机；而进程B正在使用绘图机，同时又要申请打印机，在这种情况下（ **A** ）。  
A. **进程A和进程B可能会死锁**  
B. 死锁是不可能发生的  
C. 进程A和进程B必定会死锁  
D. 系统中已经发生了死锁  
进程A与B逆序申请资源，容易导致死锁。

- 系统允许部分进程发生死锁，通过定时运行资源分析程序并报告是否已有死锁的方法称为（ **C** ）。  
A. 死锁预防  
B. 死锁避免  
C. **死锁检测**  
D. 死锁解除

- 系统允许发生部分死锁，一旦发现有死锁进程，则通过杀死死锁进程来解决死锁问题的方法称为（ **D** ）。  
A. 死锁预防  
B. 死锁避免  
C. 死锁检测  
D. **死锁解除**  
死锁解除法可归纳为两大类：①剥夺资源：使用挂起/激活机制挂起一些进程，剥夺它们占有的资源给死锁进程，以解除死锁。经常使用的方法有还原算法和建立检查点。②撤销进程：撤销死锁进程，将它们占有的资源分配给另一些死锁进程，直到死锁解除为止。

- 为了预防死锁，可以在路口使用**交通红绿灯**。那么，该方法使得死锁的哪一个必要条件不成立（ **C** ）。  
A. 互斥条件  
B. 不可剥夺条件  
C. **请求和保持条件**  
D. 循环等待条件  
十字路口不能同时被横向和纵向的车辆使用，所以满足互斥条件；车辆行驶在路口上不能被抢占，所以满足不可剥夺条件；横向车辆申请向前通行，纵向车辆也申请向前通行，所以满足循环等待条件；但是十字路口的路面不是可以部分分配或占有申请的，某一段时间内只能由横向或者纵向单独使用，所以不满足请求和保持条件。

- 为了预防死锁，可以在路口设置了**黄色网格缓冲区**，车辆可以倒车退出路口。那么，该方法使得死锁的哪一个必要条件不成立（ **B** ）。  
A. 互斥条件  
B. **不可剥夺条件**  
C. 请求和保持条件  
D. 循环等待条件

- 为了预防死锁，可以将路口某一方向（南北或东西方向）道路实行**单向行驶**。那么，该方法使得死锁的哪一个必要条件不成立（ **D** ）。  
A. 互斥条件  
B. 不可剥夺条件  
C. 请求和保持条件  
D. **循环等待条件**

- 图示的经典的**哲学家进餐**场景有可能出现死锁。下列哪一种方法能够**预防死锁**（ **B** ）。  
A. 银行家算法  
B. **仅当某哲学家左右两边的筷子都可用时，才允许他取筷子**  
C. 减少1个哲学家和相应的筷子  
D. 规定每个哲学家先取左边筷子，再取右边筷子

- 下列图示的经典的哲学家进餐场景有可能出现死锁。下列哪一种方法能够预防死锁（ **A** ）。  
A. **最多允许4个哲学家可以同时申请进餐**  
B. 银行家算法  
C. 减少1个哲学家和相应的筷子  
D. 规定每个哲学家先取左边筷子，再取右边筷子

- 图示的经典的哲学家进餐场景有可能出现死锁。下列哪一种方法能够预防死锁（**C**）。  
A. 减少1个哲学家和相应的筷子  
B. 银行家算法  
C. **奇数号的哲学家先取左边的筷子，偶数的则先取右边的筷子**  
D. 规定每个哲学家先取左边筷子，再取右边筷子

- 图示的经典的哲学家进餐场景有可能出现死锁。下列哪一种方法能够预防死锁（**C**）。  
A. 规定每个哲学家先取左边筷子，再取右边筷子  
B. 银行家算法  
C. **给其中某一个哲学家增配1只筷子**  
D. 减少1个哲学家和相应的筷子

- 死锁定理的描述是（ **C** ）。  
A. 当且仅当当前状态的资源分配图是可完全化简的  
B. 当且仅当当前状态的状态转换图是不可完全化简的  
C. **当且仅当当前状态的资源分配图是不可完全化简的**  
D. 当且仅当当前状态的状态转换图是可完全化简的  
可以利用简化资源分配图的方法，来检测系统是否为死锁状态。所谓简化，是指若一个进程的所有资源请求均能被满足的话，可以设想该进程得到其所需的全部资源，最终完成任务，运行完毕，并释放所占有的全部资源。假如一个资源分配图可被其所有进程简化，那么称该图是可简化的，否则称该图是不可简化的。系统处于死锁状态的充分条件是当且仅当该系统的资源分配图是不可完成简化的。

- 下图所示为交叉路口发生死锁的情况。为了预防死锁，可以在交叉路口建设立交桥。那么，该方法使得死锁的哪一个必要条件不成立（ **A** ）。  
A. **互斥条件**  
B. 不可剥夺条件  
C. 请求和保持条件  
D. 循环等待条件  

- 当检测到系统发生死锁之后，解除死锁的方法是（**ACE**）。  
A. **剥夺某些进程所占有的资源**  
B. 修改注册表  
C. **撤消某些进程**  
D. 进入安全模式  
E. **重新启动系统**

- 计算机系统产生死锁的原因是（ **CD** ）。  
A. 系统总资源不足  
B. 系统发生重大故障  
C. **进程资源分配不当**  
D. **并发进程推进顺序不当**  
E. 资源互斥使用

- 在设备分配中，预防死锁的策略包括（**ABCD**）。  
A. **建立SPOOLing系统**  
B. **一次分配所有资源**  
C. **有序分配资源**  
D. **剥夺其他进程的资源**  
E. 设备处于安全状态即可分配

- 下列哪些措施能够恢复或解除死锁（ **AB **）。  
A. **撤销已陷入死锁的进程**  
B. **强制剥夺其他进程的资源并分配给死锁进程**  
C. 按顺序分配资源  
D. 一次性分配全部资源  
E. 采用鸵鸟算法

- 在计算机系统中，形成死锁的必要条件是（ **ABCD** ）。  
A. **资源互斥使用**  
B. **部分分配资源**  
C. **已分配资源不可剥夺**  
D. **资源申请形成环路**  
E. 系统资源不足

- 下列关于死锁的叙述中，哪些是正确的（ **ABC** ）。  
A. **死锁产生的原因是进程推进顺序不当**    
B. **环路是死锁产生的必要条件**  
C. **采用银行家算法能有效地实现死锁避免**  
D. 当系统中只有一个进程时也可能会产生死锁  
E. 系统出现死锁是因为进程调度不当  

- **进程 资源分配图**
















#计算机网络
##第1章 网络技术基础
- Unix操作系统是一种典型的操作系统，不同的公司和研究机构推出了不同的版本，其第一个版本用**汇编语言**编写。最初，贝尔实验室公开Unix系统的源代码，允许其他厂商与研究人员在此基础上进行新的开发，这也导致Unix版本过多且不能兼容，所以Unix操作系统**并不是完全开放源代码**的Unix，**具有良好的图形用户界面**

- 国际标准化组织ISO发布了著名的ISO/IEC 7498标准，又称为X.200建议。这个体系结构定义了网络互联7层框架，即开放系统互联（OSI）参考模型。

- TCP/IP参考模型可以分为4个层次：**应用层**、**传输层**、**互联层**与**主机-网络层**。互联层的功能主要表现在：处理来自传输层的分组发送请求；处理接受到的数据报；处理互联的路径、流量与拥塞控制问题。传输层的主要功能是不同应用进程之间的端-端通信，向用户提供可靠的端到端服务，以便透明地传输报文。**应用层**对应于OSI参考模型的**（应用+表示+会话）层**，**传输层**对应于OSI参考模型的**传输层**，**互联层**对应于OSI参考模型的**网络层**，**接入层**与OSI参考模型中的**物理层和数据链路层**相对应。

- 广域网又称为远程网，所覆盖的地理范围从几十公里到几千公里；局域网一般属于一个单位所有，覆盖有限的地理范围；宽带城域网可以满足几十公里范围内的大量企业、机关、公司的多个局域网互联需求，而个人区域网覆盖的地理范围是最小的（通常为10m以内）。

- Linux是一套免费使用和自由传播的**类Unix操作系统**，是一个基于**POSIX**和**UNIX**的**多用户、多任务、支持多线程和多CPU**的操作系统。发行版本有Mankdrake SUSE TurboLinux Caldera Ubuntu Debian、RedHat、Slackware以及国内的蓝点、红旗Linux等。

- 各个公司的UNIX操作系统主要包括：IBM公司的AIX系统、Sun公司的Solaris系统、HP公司的HP-UX等，Vista是Windows操作系统产品。

- **城域网**是在一个城市范围内所建立的计算机通信网，简称**MAN**，属于**宽带局域网**。MAN的一个重要用途是**用作骨干网**，通过它将位于**同一城市内不同地点的主机、数据库，以及LAN等互相联接起来**，这与WAN的作用有相似之处，但**两者在实现方法与性能上有很大差别**。

- 无线传感器网（WSN）就是由部署在监测区域内大量的廉价微型传感器结点组成，通过无线通信方式形成的一个多跳的自组织的网络系统。  
无线传感器网络拓扑控制由两部分组成，即拓扑构建和拓扑维护。一旦建立起最初的网络优化拓扑，网络开始执行它所指定的任务。随着时间的推移，当前的网络拓扑不再处于最优运行状态，需要对其进行维护使其重新保持最优或接近最优状态。

- **传输层**是OSI参考模型中重要的一层，是唯一负责总体的数据传输和数据控制的一层，提供端到端的交换数据的机制，而该层主要目的是**实现分布式进程通信**。

- **Ad hoc网**是一种**不需要基站**的**“对等结构”**移动通信模式。它的特征是**“多跳的、无中心的、自组织无线网络”**，又称为多跳网、无基础设施网或自组织网。

- **无线自组网**简称为**WAN**，它采用一种**不需要基站**的**“对等结构”**移动通信网络，目前该种技术在**军事领域**获得广泛应用。

- **WMN**是移动Ad Hoc网络的一种**特殊形态**，它的早期研究均源于移动Ad Hoc网络的研究与开发。它是一种**高容量、高速率**的**分布式网络**，不同于传统的无线网络，可以看成是一种**WLAN和Ad Hoc网络的融合**，且发挥了两者的优势，作为一种可以解决**"最后一公里"**瓶颈问题的新型网络结构。

- OSI参考模型是**国际标准化组织**（International Standardization Organization，简称**ISO**）制定的。**中国互联网络信息中心**(China Internet Network Information Center，简称**CNNIC**)，**欧洲核子研究委员会**（Conseil Europeen pour la Recherche Nucleaire，简称**CERN**），**美国远景研究规划局** (Advanced research project agency，简称**ARPA**)。 

- Unix操作系统是一种典型的操作系统，最早由1969年在**AT&T的贝尔实验室**开发，**原本开发的是针对小型机环境开发的操作系统**，采用的是**集中式、分时、多用户**的系统结构。

- **无线个人域网（WPAN）**是为了实现活动半径小（10m以内）、业务类型丰富、面向特定群体、无线无缝的连接而提出的新兴无线通信网络技术。  
WLAN（无线局域网）是一种利用红外、扩频和微波技术进行据传输的系统，该技术的出现绝不是用来取代有线局域网络，而是用来弥补有线局域网络之不足，以达到网络延伸之目的，使得无线局域网络能利用简单的存取架构让用户透过它，实现无网线、无距离限制的通畅网络。利用扩频技术实现的无线局域网最大工作范围在240m左右。  
**WMN（无线网格网）**是移动Ad Hoc网络的一种特殊形态，它的早期研究均源于移动Ad Hoc网络的研究与开发。它是一种高容量高速率的分布式网络，不同于传统的无线网络，可以看成是一种WLAN和Ad Hoc网络的融合，且发挥了两者的优势，作为一种可以解决“最后一公里”瓶颈问题的新型网络结构。WMN被写入了IEEE 802.16无线城域网标准中。WMN的显著特点就是可以在大范围内实现高速通信，可看作“因特网的无线版”。  
WAN（Wide Area Network，广域网）它的作用范围最大，一般可以从几十公里至几万公里。一个国家或国际间建立的网络都是广域网。

- 跳频扩频通信是扩频技术中常用的一种方法，其主要技术特点为将可利用的频带划分为多个子频带，子频带称为信道；每个信道带宽相同，**中心频率由伪随机数发生器决定**，变化的频率称为跳跃系列；发送端和接收端采用相同的跳跃系列；IEEE 802.11规定跳频通信使用**2.4GHz的ISM频段**，频段范围在2.400~2.4835GHz。跳频扩频通信的**传输速率为1Mbps或2Mbps**。

- TCP/IP协议参考模型是由**美国国防部指定使用**的协议。

- **个人区域网**的英文缩写为**PAN**

- **Windows for Workgroup操作系统**是一种**对等式结构**的操作系统，但是它并没有摆脱DOS束缚，严格来说并不是一种操作系统。**Windows NT**采用**客户机/服务器**的工作模式。

- 对ARPANET发展具有重要意义的是它利用了无限分组交换网与卫星通信网。

##第3章 Internet基础
- **记录路由**选项可以判断IP数据报传输过程中所经过的路径，通常用于测试互联网中路由器配置是否正确。**时间戳**选项提供了IP数据报传输中的时域参数，用于分析网络吞吐率、拥塞情况、负载情况等。**严格源路由选项**规定IP数据报要经过路径上的每一个路由器，相邻路由器之间不得有中间路由器，并且所经过路由器的顺序不可更改。**松散源路由选项**只是给出IP数据报必须经过的一些“要点”，并不给出一条完备的路径，无直接连接的路由器之间的路由尚需IP软件的寻址功能补充。

- **IEEE 802.3**规定的**Ethernet帧**的**最小长度为64B**，**最大长度1518B**。

- 关于以太网帧结构的描述中，错误的是（**B**）。  
A. 帧前定界符可用于接收同步  
B. 前导码表示网络层协议类型  **同步**  
C. 地址字段只能使用MAC地址  
D. 数据部分最小长度为46字节
