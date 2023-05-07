#  一、基本概念和术语

![image-20230228102653440](C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230228102653440.png)

## 1、数据

**是能输入计算机且能被计算机处理的各种符号的集合**

①信息的载体

②是对客观事物符号化的表示

③能够被计算机识别、加工和储存

## 包括：

①数值型的数据：整数、实数等

②非数值型的数据：文字、图像、图形、声音等

## 2、数据元素和数据项

### a、数据元素

①是**数据的基本单位**，在计算机程序中通常作为一个整体进行考虑和处理。

②也称为元素，或称为记录、节点或顶点。

③一个**数据元素**可由若干个**数据项**组成。

### b、数据项

**①构成数据元素的不可分割的最小单位。**

![image-20230227212914697](C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230227212914697.png)

**②数据、数据元素、数据项三者之间的关系。**

数据>数据元素>数据项

列：学生表>个人记录>学号>姓名

### c、数据对象

**①是性质相同的数据元素的集合**，是数据的一个*子集*。



数据元素——组成数据的基本单位

数据对象——性质相同的数据元素的集合



## 3、数据结构

①数据元素不是孤立存在的，他们之间存在着某种关系，**数据元素相互之间的关系称为结构。**

②是指**相互之间存在一种或多种特定关系**的数据元素集合。

③或者说：数据结构是**带结构的数据元素**的集合。



### a、逻辑结构

**数据元素之间的逻辑关系。**

①描述数据元素之间的逻辑关系

②与数据的存储无关，独立于计算机

③是从具体问题抽象出来的数学模型



#### 逻辑结构的种类

#### ~划分方式一

**(1）集合结构：**

结构中的数据元素之间除了同属于一个集合的关系外，无任何其它关系。

**(2）线性结构:**

结构中的数据元素之间存在着一对一的线性关系。

**(3）树形结构:**

结构中的数据元素之间存在着一对多的层次关系。

**(4）图状结构或网状结构:**

结构中的数据元素之间存在着多对多的任意关系。



#### ~划分方式二

**(1）线性结构**

有且**仅有一个开始和一个终端结点**，并且**所有结点都最多只有一个直接前趋和一个直接后继**。

例如:线性表、栈、队列、串

**(2）非线性结构**

一个结点可能有**多个直接前趋和直接后继**

例如:树、图



### b、存储结构

**数据元素及其关系在计算机内存中的表示，称为数据的物理结构或数据的存储结构。**

①数据元素及其关系在计算机存储器中的结构(存储方式)。

②是数据结构在许算机中的表示。

#### 四种基本的存储结构:

#### （1）顺序存储结构

①用一组**连续**的存储单击依**次存**储数据元素，数据元素之间的逻辑关系由元素的**存储位置**来表示。

②C语言中用数组来实现顺序存储结构

#### （2）链式存储结构

①用一组**任意**的存储单元存储数据元素，数据元素之间的逻辑关系用**指针**来表示。

②C语言中用指针来实现链式存储结构

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230227223157254.png" alt="image-20230227223157254" style="zoom:25%;" />

#### （3）索引存储结构



### c、运算和实现

**对数据元素可以施加的操作以及这些操作在相应的存储结构上的实现。**

①存储结构是逻辑关系的映象与元素本身的映象。

②逻辑结构是数据结构的抽象，存储结构是数据结构的实现。

③两者综合起来建立数据元素之间的结构关系。



## 4、数据类型和抽像数据类型

### 1、数据类型(Data Type)

**定义**:数据类型是一组性质相同的值的集合以及定义于这个值集合上的一组操作的总称。

数据类型=值的集合+值集合上的一组操作



### 2、抽象数据类型(ADT) 

**是指一个数学模型以及定义在此数学模型上的一组操作。**

由用户定义,从问题抽象出数据模型（逻辑结构)

还包括定义在数据模型上的一组抽象运算(相关操作)。

不考虑计算机内的具体存储结构与运算的具体实现算法



#### a、抽象数据类型的形式定义

**抽象数据类型可用(D，S，P)三元组表示。**

其中:

D是数据对象;

S是D上的关系集;

P是对D的基本操作集。

**（1）一个抽象数据类型的定义格式如下:**

**ADT抽象数据类型名**

**{**

​	数据对象：<数据对象的定义>

​	数据关系：<数据关系的定义>

​	基本操作：<基本操作的定义>

**}ADT抽象数据类型名**



其中:

**①数据对象、数据关系的**

定义用**伪代码描述**

**②基本操作的定义**格式为

**~基本操作名(参数表)**

参数表：赋值参数只为操作提供输入值。

**引用参数以&打头**，除可提供输入值外，还将返回操作结果。



**~初始条件:<初始条件描述>**

初始条件：描述操作执行之前数据结构和参数应满足的条件，若不满足区则操作失败，并返回相应出错信息。若初始条件为空，则省略之。



**~操作结果:<操作结果描述>**

操作结果︰说明操作正常完成之后，数据结构的变化状况和应返回的结果。

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230228101547459.png" alt="image-20230228101547459" style="zoom: 50%;" />

------



# 二、算法和算法分析

## 1、算法

### a、基本内容

**（1）定义：**对特定问题求解方法和步骤的一种描述，它是指令的有限序列。其中每个指令表示一个或多个操作。

**也就是解决问题的方法和步骤。**

**（2）描述：**

①自然语言：英语，中文

②流程图：传统流程图、ns流程图

③伪代码：类语言（类c语言）



**（3）程序=数据结构＋算法**

①数据结构通过算法实现操作

②算法根据数据结构设计程序

### b、算法特性

（1）**有穷性：**一个算法必须总是在执行有穷步之后结束，且每一步都在有穷时间内完成。

（2）**确定性：**算法中的每一条指令必须有确切的含义，没有二义性，在任何条件下，只有唯一的一条执行路径，即对于相同的输入只能得到相同的输出。

（3）**可行性：**算法是可执行的，算法描述的操作可以通过已经实现的基本操作执行有限次来实现。

（4）**输入：**一个算法有零个或多个输入。

（5）**输出：**―一个算法有一个或多个输出。

### c、算法设计要求

（1）**正确性**:算法满足问题要求，能正确解决问题算法转化为程序后要注意:

①程序中不含语法错误;

②程序对于几组输入数据能够得出满足要求的结果;

③程序对于精心选择的、典型、苛刻且带有刁难性的几组输入数据能够得出满足要求的结果;

④程序对于一切合法的输入数据都能得出满足要求的结果。

通常以第三层意义上的正确性作为衡量一个算法是否合格的标准

（2）**可读性:**

①算法主要是为了人的阅读和交流，其次才是为计算机执行，因此**算法应该易于人的理解**;

②另一方面，晦涩难读的算法易于隐藏较多错误而难以调试。

（3）**健壮性:**

①指当输入非法数据时，算法恰当的做出反应或进行相应处理，而不是产生莫名其妙的输出结果。 

②处理出错的方法，不应是中断程序的执行，而应是返回一个表示错误或错误性质的值，以便在更高的抽象层次上进行处理

（4）**高效性**

## 2、算法分析

**算法分析的考虑方面：**

**1．时间效率:**指的是算法所耗费的时间;

**2．空间效率:**指的是算法执行过程中所耗费的存储空间。

​		**时间效率和空间效率有时候是矛盾的**

### a、算法时间效率的度量

（1）算法时间效率可以用依据该算法编制的程序在计算机上执行**所消耗时间来度量**。

（2）两种度量方法

**①事后统计：**

将算法实现，测算其时间和空间开销。

**缺点**:编写程序实现算法将花费较多的时间和精力;所得实验结果依赖于计算机的软硬件等环境因素，掩盖算法本身的优劣

**②事前分析：**

对算法所消耗资源的一种估第方法。



### b、事前分析方法:

（1）一个算法的运行时间是指一个算法在计算机上运行所耗费的时间大致可以等于计算机执行一种简单的操作(如赋值、比较、移动等)所需的**时间**与算法中进行的简单操作**次数乘积**。

**算法运行时间 = 一个简单操作所需的时间 × 简单操作次数**



（2）也即算法中每条语句的执行时间之和

**算法运行时间 = ∑每条语句的执行次数（语句频度） × 该语句执行一次所需的时间**



（3）**定理：**<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230301163804636.png" alt="image-20230301163804636" style="zoom:67%;" />

**忽略所有低次幂项和最高次幂系数，体现出增长率的含义**



（4）**方法：**

找出语句频度最大的那条语句作为基本语句

**计算基本语句的频度得到问题规模n的某个函数f(n)**

c、取其数量级用符号“O”表示

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230301164914670.png" alt="image-20230301164914670" style="zoom:67%;" />

 **时间复杂度是由嵌套最深层的语句的频度决定**



#### 列子：

**关键是要找出来执行次数x与n的关系，并表示成n的函数。**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230301170940936.png" alt="image-20230301170940936" style="zoom: 50%;" />

若循环执行1次:  i=1*2=2,

若循环执行2次:  i=2*2=2^2，

若循环执行3次:  i=2*2=2^3，   ……，

若循环执行x次:  i=2^x

**设语句②执行次数为x次，由循环条件**

**i<=n ,  ∴2^x<=n   ∴x<=log₂n**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230301171617536.png" alt="image-20230301171617536" style="zoom:33%;" />

即f(n)≤log₂n，取最大值f(n)=log₂n

所以该程序段的时间复杂度T(n)=O( log₂n)

#### 法则：

对于复杂的算法，可以将它分成几个容易估算的部分，然后利用人U加法法则和乘法法则，计算算法的时间复杂度:

**（a）加法规则**

T(n) = T1(n)+T2(n) = O(f(n))+ O(g(n)) = O（max(f(n),g(n))）

**（b）乘法规则**

T(n) = T1(n)xT2(n) = O(（f(n)) x O(g(n)） = O(f(n) x g(n))



# ~补充：类c语言的有关操作

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230307195759614.png" alt="image-20230307195759614" style="zoom: 67%;" />

```c
1、ElemType data[MaxSize]：定义一个数组 —int arr[100];
2、ElemType *data：定义一个数组（定义一个指针变量用于存放数组首元素地址）— int *data=&arr[100];
3、ElemType data：表数据类型（如int、float、long）;

4、内存动态分配(头文件<stdlib.h>);
SqList L;
//sizeof(ElemType)乘MaxSize
L.data=(ElemType*)malloc(sizeof(ElemType)*MaxSize)
    
    a、malloc(m)函数，开辟m字节长度的地址空间，并返回这段空间的首地址.
    b、sizeof(x)运算，计算变量x的长度.
    c、free(p)函数，释放指针p所指变量的存储空间，即彻底删除	一个变量.
```

### 1、线性表中用到的基本操作：

```c
（1）lnitList(&L)			//初始化操作，建立一个空的线性表L

（2）DestroyList(&L)		//销毁已存在的线性表L

（3）ClearList(&L)		//将线性表清空

（4）ListDelete(&L, i, &e)//在线性表L中第i个位置插入新元素e

（5)lsEmpty(L)			 //删除线性表L中第i个位置元素，用e返回。

（6）ListLength(L)		//若线性表为空，返回true，否则false。

（7）LocateElem(L, e)		//L中查找与给定值e相等的元素，若成功返回该元素在表中的序号，否则返回0。

（8）GetElem(L, i, &e)	//将线性表L中的第i个位置元素返回给e。
```

#### **补充:操作算法中用到的预定义常量和类型**

//函数结果状态代码

#define TRUE	1

#define FALSE   0

#define OK	    1

#define ERROR		       0

#define INFEASIBLE	  -1

#define OVERFLOW	  -2

//Status是函数的类型，其值是函数结果状态代码

typedef int Status;

typedef char ElemType;

**a、线性表的初始化**

```c
#define TRUE 1
#define FALSE 0
#define OK 1
#define ERROR 0
#define INFEASIBLE -1
#define OVERFLOW -2

typedef int Status;
typedef char ElemType;
Status InitList_Sq(SqList &L)  //构造一个空间的顺序表L
{
    L.elem=new ElemType[MAXSIZE];//为顺序表分配空间
    if(!L.elem) exit(OVERFLOW);  //存储分配失败
    L.length=O;	//空表长度为0
    return OK;
}
```

**b、销毁线性表**

```c
void DestroyList(SqList &L)
{
	if(L.elem)delete[]. L.elem;	//释放存储空间
}
```

**c、清空线性表**

```c
void ClearList(SqList&L)
{
	L.length=0;
}
```

**c、求线性表L的长度**

```c
int GetLength(SqList L)
{
    return(L.lengh);
}
```

**d、判断线性表L是否为空**

```c
int IsEmpty(SqList L)
{
    if(Llenght==0)return 1;
    else return 0;
}
```

**e、顺序表的取值**

```c
int GetElem(SqList L,int i,ElemType &e)
{
    //判断i值是否合理，若不合理，返回ERROR
	if(i<1||i>L.lenght)return ERROR;
    //第i-1的单元存储着第i个数据
	e=L.elem[i-1];
	return OK;
}
```



# 三、线性表

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230302180244958.png" alt="image-20230302180244958" style="zoom: 50%;" />

**线性表具有相同特性的数据元素的一个有限序列**

（a₁，a₂，a₃，……ai-₁，ai，ai+₁，……，an）

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230302181046579.png" alt="image-20230302181046579" style="zoom: 33%;" />



**由n(n≥0)个数据元素(结点)a1, a2,..a,组成的有限序列。**

①其中数据元素的个数n定义为表的长度。

②当n=0时称为空表

③将非空的线性表(n>0)记作:(a1, a2,，...an)

④这里的数据元素ai(1≤in)只是一个抽象的符号，其具体含义在不同的情况下可以不同。

## 1、顺序表

**（1）定义：线性表的顺序表示又称为顺序存储结构或顺序映像。**

**顺序存储定义:**把逻辑上相邻的数据元素存储在物理上相邻的存储单元中的存储结构。

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230307133913536.png" alt="image-20230307133913536" style="zoom:50%;" />

***简而言之：逻辑上相邻，物理上也相邻（中间没有空位）***



### a、线性表的操作

```c
InitList(&L)	//初始化操作，建立一个空的线性表L

DestroyList(&L)	//销毁已存在的线性表L

ClearList(&L)	//将线性表清空

Listlnsert(&L, i, e)	//在线性表L中第i个位置插入新元素

eListDelete(&L, i, &e)	//删除线性表L中第i个位置元素，用e返回

lsEmpty(L)	//若线性表为空，返回true，否则false

LocateElem(L, e)	//L中查找与给定值e相等的元素，若成功返回元素在表中的序号，否则返回0。

GetElem(L,i, &e)	//将线性表L中的第i个位置元素返回给e
```



### b、顺序表的实现

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230307193228992.png" alt="image-20230307193228992" style="zoom:50%;" />

**由于c语言中数组大小是不可动态改变的，所以我们用一个变量去存储数组的大小。**



```c
//线性表存储空间的初始分配
#define LIST_INIT_SIZE	//模板
typedef struct
{
    //定义某个数据类型的数组
    ElemType elem[LIST_INITSIZE];
    //当前长度
    int length;
}SqList;
```

 **（1）、线性表的初始化**

```c
#define TRUE 1
#define FALSE 0
#define OK 1
#define ERROR 0
#define INFEASIBLE -1
#define OVERFLOW -2

typedef int Status;
typedef char ElemType;
//c++中引用符&：
//int &a=b和int *const a=&b类似

//const指针：
//const指针是指针变量的值一经初始化，就不可以改变指向，初
//始化是必要的。其定义形式如下：
//type *const 指针名称;

Status InitList_Sq(SqList &L)  //构造一个空间的顺序表L
{
    //sizeof(ElemType)乘MaxSize
//L.data=(ElemType*)malloc(sizeof(ElemType)*MaxSize)
    L.elem=new ElemType[MAXSIZE];//为顺序表分配空间
    if(!L.elem) exit(OVERFLOW);  //存储分配失败
    L.length=0;	//空表长度为0
    return OK;
}
```

**（2）、销毁线性表**

```c
void DestroyList(SqList &L)
{
	if(L.elem) delete[]. L.elem;	//释放存储空间
}
```

**（3）、清空线性表**

```c
void ClearList(SqList&L)
{
	L.length=0;
}
```

**（4）、求线性表L的长度**

```c
int GetLength(SqList L)
{
    return(L.length);
}
```

**（5）、判断线性表L是否为空**

```c
int IsEmpty(SqList L)
{
    if(Llength==0)return 1;
    else return 0;
}
```



**（6）、顺序表的取值**（将线性表L中的第i个位置的元素返回给e）

```c
int GetElem(SqList L,int i,ElemType &e)
{
    //判断i值是否合理，若不合理，返回ERROR       
	if(i<1||i>L.length)return ERROR;
    //第i-1的单元存储着第i个数据
	e=L.elem[i-1];
	return OK;
}
```



**（7）、按值查找**

例如：在图书表中，按照给定书号进行查找，确定是否存在该图书。

如果存在：输出是第几个元素如果不存在:输出0。

①在线性荐L中查找与指定值e相同的数据元素的位置
②从表的一端开始，逐个进行记录的关键字和给定值的比较。找到，返回该元素的位置序号，未找到，返回0。

```c
//顺序查找法
int LocateElem(SqList L,Elem Type e)
{
    //在线性表L中查找值为e的数据元素，返回其序列号（是第几个元素）
    for(i=0;i<L.length;i++)
    {
        //查找成功，返回序号
        if(L.elem[i]==e)return i+1;
    }
    return 0;//查找失败，返回0
}
```

对含有n个记录的表，查找成功时:

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230308163824821.png" alt="image-20230308163824821" style="zoom:50%;" />

顺序查找的平均查找长度:

ASL=P(1) 2P(2)+...+(n-1)P(n-1)+nP(n),

假设每个记录的查找概率相等:Pi=1/n

则：

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230308163928806.png" alt="image-20230308163928806" style="zoom:50%;" />



**（8）、顺序表插入元素**

（1）插入元素在最后

（2）插入元素在中间

（3）插入元素在最前面

**算法思想**：

①判断插入位置i是否合法。

②判断顺序表的存储空间是否已满，若满返回ERROR。

③将第n至第i位的元素依次向后移动一个位置，空出第i个位置。

④将要插入的新元素e放入第i个位置。

⑤表长加1,插入成功返回OK。

```c
Status Listlnsert_Sq(SqList &L,int i,ElemType e)
{
    //判断i值是否合法
    if(i<1||i>L.length+1)return ERROR;
    //判断当前存储空间是否已满
    if(L.length==MAXSIZE)return ERROR;
    //插入位置及之后的元素后移
    for(j=L.length-1;j>=i-1;j--)
    {
        L.elem[j+1]=L.elem[j];
    }
    //将新元素e放入第i个位置
    L.elem[i-1]=e;
    //表增长1
    L.length++;
    return OK;
```



**（9）、顺序表的删除算法**

（1）删除位置在最后

（2）删除位置在中间

（3）删除位置在最前面

**算法思想:**

①判断删除位置i 是否合法（合法值为1<=i<=n) 。

②将欲删除的元素保留在e中。

③将第i+1至第n位的元素依次向前移动一个位置。

④表长减1，删除成功返回OK。

```c
Staus LIstlnsert_Sq(SqList &L,int i,Elemtype e)
{
    //判断i值是否合法
    if(i<1||i>L.length)return ERROR;
    //被删除元素之后的元素前移
    for(j=i;j<L.length-1;j++)
    {
        L.elem[j-1]=L.elem[j];       
    }
    //表长减一
    L.length--;
    return OK;
}
```

### c、顺序表的优缺点

**优点：**

①存储密度大(结点本身所占存储量/结点结构所占存储量)

②可以随机存取表中任一元素

**缺点：**		**为克服这一缺点**   将引入  **链表**

①在插入、删除某一元素时，需要移动大量元素

②浪费存储空间

③属于静态存储形式，数据元素的个数不能自由扩张。



## 2、链表

**定义：**

①用一组物理位置任意的存储单元来存放线性表的数据元素。

②这组存储单元既可以是连续的，也可以是不连续的，甚至是零散分布在内存中的任意位置上的。

③链表中元素的逻辑次序和物理次序不一定相同。



### **a、与链式存储有关的术语：**

①结点:数据元素的存储映像。由数据域和指针域两部分组成

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230308204005889.png" alt="image-20230308204005889" style="zoom:33%;" />

②链表:n个结点由指针链组成一个链表。

它是线性表的链式存储映像，称为线性表的链式存储结构。

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230308204116922.png" alt="image-20230308204116922" style="zoom:50%;" />

**链表的分类：**

①单链表：结点只有一个指针域的链表，称为单链表或线性链表

②双链表：结点只有一个指针域的链表，称为单链表或线性链表

③循环链表：·首尾相接的链表称为循环链表

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230308204705588.png" alt="image-20230308204705588" style="zoom:50%;" />



**头指针、头结点、首元结点：**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230308205043713.png" alt="image-20230308205043713" style="zoom:50%;" />

①头指针:是指向链表中第一个结点的指针

②头结点:是在链表的首元结点之前附设的一个结点

③首元结点:是指链表中存储第一个数据元素a,的结点

   

**有无头结点的区分：**

①无头结点时：头指针为空时表示空表。

②有头结点时：当头结点的指针域为空时表示空表。



**头结点的好处：**

①便于首元结点的处理

​	首元结点的地址保存在头结点的指针域中所以在链表的第一个位置上的操作和其它位置一致，无须进行特殊处理;

②便于空表和非空表的统一处理

​	无论链表是否为空，头指针都是指向头结点的非空指针，因此空表和非空表的处理也就统一了。



###  b、带头结点的单链表实现

#### 定义：

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230311161945685.png" alt="image-20230311161945685" style="zoom:50%;" />

**单链表的定义：**

单链表是由表头唯一确定，因此**单链表可以用头指针的名字来命名**若头指针名是L，则把链表称为表L



**单链表的存储结构：**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230311162328977.png" alt="image-20230311162328977" style="zoom:50%;" />

data：数据类型			next：指针型



#### 实现：

**（1）、单链表的存储结构定义**

```c
//声明结点的类型和指向结点的指针类型
//嵌套定义5.                                         
typedef struck Lnode
{
    //结点的数据域
    ElemType data;			
    //结点的指针域指向Lnode类型
    struct Lnode *next;		
}Lnode,*LinkList;	//LinkList为指向结构体Lnode的指针类型
```

**更常用的定义类型：**

```c
typedef struck
{
    ElemType data;
    ElemType data_1;
    ElemType data_2;
}ElemType;

typedef struct Lnode
{
    ElemType data;
    struct Lnode *next;
}Lnode,*LinkList;
```

LinkList L 与 Lnode *L是一样的含义

**定义链表L：**LinkList L；

**定义结点指针p：**LNode *p；



**(2)、单链表的初始化**（带头结点的单链表）

**算法步骤：**

①生成新节点作头结点，用头指针L指向头结点。

②将头结点的指针域置空

```c
#define TRUE 1
#define FALSE 0
#define OK 1
#define ERROR 0
#define INFEASIBLE -1
#define OVERFLOW -2

typedef int Status;
typedef char ElemType;

Status lnitList_L(LinkList &L)//引用型L
{
    
    L=new LNOde;//new一个结点作为头结点
    //或L=(LinkList)malloc(sizeof(LNode));
    
    L->next=NULL;//头指针L指向头结点
    return OK;
}
```



**(3)、判断一个链表是否为空**

```c
int ListEmpty(LinkLkst L)
{
    //若为空表，则返回1，否则返回0
    if(L->next) return 0;
    else return 1;
}
```



**(4)、单链表的销毁**

**算法思路：**从头指针开始，依次释放所有结点

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230311172859984.png" alt="image-20230311172859984" style="zoom: 50%;" />

```c
Status DestroyList_L(LinkList &L)
{
    Lnode *p;//或LinkList p;
    while(L==NULL)
    {
        p=L;
        L=L->next;
        delete[]. p;//或free(p);
    }
    return OK;
}
```



**(5)、清空单链表**

**算法思路：**依次释放所有结点，并将头结点指针域设置为空

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230311191113183.png" alt="image-20230311191113183" style="zoom:50%;" />

```c
//非法访问？
Status ClearList(LinkList &L)//将L重置为空表
{
    Lnode *p,*q;//或LinkList p,q;
    p=L->next;
    while(p==NULL)
    {
        q=p->next;
        delete[]. p;
        p=q;
    }
    L->next=NULL;//头结点指针域为空
    return OK;
}
```

 

**（6）、求链表的表长**

**算法思路：**从首元结点开始，依次计数所有结点

```c
int ListLength_L(LinkList L)//返回L中数据元素个数
{
    Lnode * p;
    p=L->next;	//p指向第一个结点
    int i=0;
    while(p !=NULL)	//遍历单链表，统计节点数
    {
        i++;
        p=p->next;
    }
    return i;
}
```



**（7）、从单链表中取第i个元素**

 **算法思路：**从链表的头指针出发，顺着链域next逐个结点往下搜索，直至搜索到第结点为止。因此，链表不是随机存取结构

①从第1个结点 (L->next)顺链扫描，用指针p指向当前扫描到的结点，p初值p = L->next。

②j做计数器，累计当前扫描过的结点数，j初值为1。

③当p指向扫描到的下一结点时，计数器j加1。

④当j ==i时，p所指的结点就是要找的第i个结点。

```c
Status GetElem_L(LinkList L,int i)
{
    Lnode *p;
    p=L->next;		//初始化
    j=1;		//向后扫描，直到p指向第i个元素或p为空
    while(p&&j<i)//p为空或i为0、-1都会结束循环
    {
        p=p->next;
        ++j;
    }
    if(!p||j>i) return ERROR;	//第i个元素不存在
    e=p->data;					//取第i个元素
    return OK;
}
```



**（8）、查找**

**分为：**

A、按值查找:根据指定数据获取该数据所在的位置（该数据的地址)

**算法步骤:**

①.从第一个结点起，依次和e相比较。

②如果找到一个其值与e相等的数据元素，则返回其在链表中的位置"或地址。

③如果查遍整个链表都没有找到其值和e相等的元素，则返回0或"NULL”。

```c
Lnode *LocateELem_L(LinkList L,Elemtype e)
{
    Lnode *p;
    p=L->next;
    while(p&&p->data!=e)
    {
        p=p->next;
    }
    return p;
}
```

算法效率：



B、按值查找:根据指定数据获取该数据所在的位置序号（是第几个数据元素)

```c
int LocateELem_L(LinkList L,Elemtype e)
{
    Lnode *p;
    p=L->next;
    j=1;
    while(p&&p->data!=e)
    {
        p=p->next;
        j++;
    }
    if(p!=NULL) return j;	//p不为空则返回j的值
    else return 0;	//p为空则返回0
}
```

算法效率：



**(9)、插入**（在第i个结点前插入为e的新结点）

**算法思路：**

①首先找到ai-1的存储位置p。

②生成一个数据域为e的新结点s。

③插入新结点:

1新结点的指针域指向结点a;

2结点a-1的指针域指向新结点

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230312102826180.png" alt="image-20230312102826180" style="zoom: 50%;" />

①s->next=p->next;	②p->next=s;

*思考：步骤①和②能互换么？*

*不可以！会丢失ai的地址。*

```c
Status Listlnsert_L(LinkList &L,int i,ElemType e)
{
    Lnode *p;
    p=L;j=0;
    while(p&&j<i-1)//寻找i-1个结点，p指向i-1结点
    {
        p=p->next;
        ++j;
    }
    //i大于表长或者小于1，插入位置非法
    if(!p||j>i-1) return ERROR;
    s=new LNode;
    s->data=e;		
    s->next=p->next;	//将结点s插入L中
    p->next=s;
}
```

**（10）、删除**（删除第i个结点）

**算法步骤：**

①首先找到ai-1的存储位置p，保存要删除的a的值。

②令p ->next指向aj+1。

③释放结点ai的空间。

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230312165200530.png" alt="image-20230312165200530" style="zoom: 50%;" />

**p->next = p->next->next**

```c
Status ListDelete_L(LinkList &L,int i,ElemType &e)
{
    j=0;i=0;
    Status *q,*p=L;
    //寻找到第i个结点，并令p指向其前驱
    while(p->next&&j<i-1)
    {
        p=p->next;
        ++j;
    }
    //排除不合理位置
    if(!(p->next)||j>i-1) return ERROR;
    q=p->next;	//临时保存被删除结点的地址以备用
    p->next=q->next;//改变删除结点前驱的指针域
    e=q->data;//保存删除结点的数据域
    delete[].q;	//释放删除结点
    return OK;
}
```



**（11）、单链表的建立**

**分为：**

A、**头插法**——元素插入在链表头部

①从一个空表开始，重复读入数据;

②生成新结点，将读入数据存放到新结点的数据域中

③从最后一个结点开始，依次将各结点插入到链表的前端

```c
//倒位序输入n个元素的值
void CreateList_H(LinkList &L,int n)
{
    L=new LNode;
    //或者L=(LNode*)mallox(sizeof(LNode))
    L->next=NULL;
    for(i=n;i>0;i--)
    {
        p=new LNode;
        scanf(&p->data);//? 或cin>>p->data;
        p->next=L->next;//插入到表头
        L->next=p;
    }
}
```



B、**尾插法**——元素插入在链表尾部

①从一个空表L开始，将新结点逐个插入到链表的尾部，尾指针r指向链表的尾结点。

②初始时，r同L均指向头结点。每读入一个数据元素则申请一个新结点，将新结点插入到尾结点后，r指向新结点。

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230313201727913.png" alt="image-20230313201727913" style="zoom:50%;" />

p->data=ai;		p->next=NULL;		r->next=p;		r=p;

```c
//正位序输入n个元素的值。
void CreateList_R(LinkList &L,int n)
{
    L=new LNode;
    L->next=NULL;
    r=L;	//尾指针r指向头结点
    for(i=0;i<n;i++)
    {
        p=new LNode;	//生成新节点，输入元素值
        cin>>p->data;	//scanf(&p->data);
        p->next=NULL;
        r->next=p;	//插入到表尾
        r=p;		//r指向新的尾结点
	}
}
```



### c、循环链表的实现

#### 定义：

**循环链表:**是一种头尾相接的链表(即:表中最后一个结点的指向头结点，整个链表形成一个环)。

**优点:**从表中任一结点出发均可找到表中其他结点。



***头指针**表示单循环链表：*（时间复杂度较高）

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230313203054461.png" alt="image-20230313203054461" style="zoom:50%;" />

找a的时间复杂度:O(1)

找an的时间复杂度:O(n)



**注意：表的操作常常是在表的首尾位置上进行。**



***尾指针**表示单循环链表：*

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230313204207791.png" alt="image-20230313204207791" style="zoom:50%;" />

a(1)的存储位置是:R->next->next

a(n)的存储位置是:R

找a(1)和a(n)的时间复杂度都为:O(1)



**注意:**

**表的操作常常是在表的首尾位置上进行。**

由于循环链表中没有NULL指针，故涉及遍历操作时，其终止条件就不再像非循环链表那样判断p或p->next是否为空，而是*判断它们是否等于头指针。*

*循环条件:*

p!=NULL								p!=L

p->next!=NULL					 p->next!=L

单链表									单循环链表



#### 实现：

**（1）、带尾指针循环链表的合并(将Tb合并在Ta之后)**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230313205225257.png" alt="image-20230313205225257" style="zoom:50%;" />

①p存表头结点：p=Ta->next;

②Ta表尾接上Tb表头：Ta->next=Tb->next-next

③释放Tb表头结点：delete[].. Tb->next;

④Tb表尾接上Ta表头：Tb->next=p;

```c
//假设Ta、Tb都是非空的单循环链表
LinkList Connect(LinkList Ta,LinkList Tb)
{
    p=Ta->next;
    Ta->next=Tb->next->next;
    detele Ta->next;
    Ta->next=p;
    return Tb;
}
```



#### **案例：约瑟夫问题**

约瑟夫问题是个著名的问题：N个人围成一圈，第一个人从1开始报数，报M的将被杀掉，下一个人接着从1开始报。如此反复，最后剩下一个，求最后的胜利者。
例如只有三个人，把他们叫做A、B、C，他们围成一圈，从A开始报数，假设报2的人被杀掉。

首先A开始报数，他报1。侥幸逃过一劫。
然后轮到B报数，他报2。非常惨，他被杀了
C接着从1开始报数
接着轮到A报数，他报2。也被杀死了。
最终胜利者是C

**解决方案**
**普通解法**
刚学数据结构的时候，我们可能用链表的方法去模拟这个过程，N个人看作是N个链表节点，节点1指向节点2，节点2指向节点3，……，节点N-1指向节点N，节点N指向节点1，这样就形成了一个环。然后从节点1开始1、2、3……往下报数，每报到M，就把那个节点从环上删除。下一个节点接着从1开始报数。最终链表仅剩一个节点。它就是最终的胜利者。

<img src="https://imgconvert.csdnimg.cn/aHR0cDovL2ltZy5ibG9nLmNzZG4ubmV0LzIwMTcwNjAzMjM0MzQzMDY1?x-oss-process=image/format,png" alt="这里写图片描述"  />

**缺点**：
要模拟整个游戏过程，时间复杂度高达O(nm)，当n，m非常大(例如上百万，上千万)的时候，几乎是没有办法在短时间内出结果的。

**公式法**
约瑟夫环是一个经典的数学问题，我们不难发现这样的依次报数，似乎有规律可循。为了方便导出递推式，我们重新定义一下题目。
问题： N个人编号为1，2，……，N，依次报数，每报到M时，杀掉那个人，求最后胜利者的编号。

这边我们先把结论抛出了。之后带领大家一步一步的理解这个公式是什么来的。
**递推公式：**
**f(N, M) = (f(N − 1, M) + M) % N**

f ( N , M )表示，N个人报数，每报到M时杀掉那个人，最终胜利者的编号。
f ( N − 1 , M )表示，N-1个人报数，每报到M时杀掉那个人，最终胜利者的编号。
下面我们不用字母表示每一个人，而用数字。
1 、 2 、 3 、 4 、 5 、 6 、 7 、 8 、 9 、 10 、 11 

表示11个人，他们先排成一排，假设每报到3的人被杀掉。

①刚开始时，头一个人编号是1，从他开始报数，第一轮被杀掉的是编号3的人。

②编号4的人从1开始重新报数，这时候我们可以认为编号4这个人是队伍的头。第二轮被杀掉的是编号6的人。

③编号7的人开始重新报数，这时候我们可以认为编号7这个人是队伍的头。第三轮被杀掉的是编号9的人。

……

⑤第九轮时，编号2的人开始重新报数，这时候我们可以认为编号2这个人是队伍的头。这轮被杀掉的是编号8的人。

⑥下一个人还是编号为2的人，他从1开始报数，不幸的是他在这轮被杀掉了。

⑦最后的胜利者是编号为7的人。

下图表示这一过程（先忽视绿色的一行）

<img src="https://imgconvert.csdnimg.cn/aHR0cDovL2ltZy5ibG9nLmNzZG4ubmV0LzIwMTcwNjA0MDAxNzE0MzQ1?x-oss-process=image/format,png" alt="这里写图片描述"  />

现在再来看我们递推公式是怎么得到的！
**将上面表格的每一行看成数组，这个公式描述的是：幸存者在这一轮的下标位置**

f ( 1 , 3 ) ：只有1个人了，那个人就是获胜者，他的下标位置是0
f ( 2 , 3 ) = ( f ( 1 , 3 ) + 3 ) % 2 = 3 % 2 = 1 ：在有2个人的时候，胜利者的下标位置为1
f ( 3 , 3 ) = ( f ( 2 , 3 ) + 3 ) % 3 = 4 % 3 = 1 ：在有3个人的时候，胜利者的下标位置为1
f ( 4 , 3 ) = ( f ( 3 , 3 ) + 3 ) % 4 = 4 % 4 = 0 ：在有4个人的时候，胜利者的下标位置为0
……
f ( 11 , 3 ) = 6 

很神奇吧！现在你还怀疑这个公式的正确性吗？上面这个例子验证了这个递推公式的确可以计算出胜利者的下标，下面将讲解怎么推导这个公式。
**问题1：** 假设我们已经知道11个人时，胜利者的下标位置为6。那下一轮10个人时，胜利者的下标位置为多少？
**答**： 其实吧，第一轮删掉编号为3的人后，之后的人都往前面移动了3位，胜利这也往前移动了3位，所以他的下标位置由6变成3。

**问题2：** 假设我们已经知道10个人时，胜利者的下标位置为3。那下一轮11个人时，胜利者的下标位置为多少？
**答**： 这可以看错是上一个问题的逆过程，大家都往后移动3位，所以f ( 11 , 3 ) = f ( 10 , 3 ) + 3 。不过有可能数组会越界，所以最后模上当前人数的个数，f ( 11 , 3 ) = （ f ( 10 , 3 ) + 3 ） % 11。

**问题3：** 现在改为人数改为N，报到M时，把那个人杀掉，那么数组是怎么移动的？
**答：** 每杀掉一个人，下一个人成为头，相当于把数组向前移动M位。若已知N-1个人时，胜利者的下标位置位f ( N − 1 , M ) ，则N个人的时候，就是往后移动M为，(因为有可能数组越界，超过的部分会被接到头上，所以还要模N)，既f ( N , M ) = ( f ( N − 1 , M ) + M ) % n 。

**注：**理解这个递推式的核心在于关注胜利者的下标位置是怎么变的。每杀掉一个人，其实就是把这个数组向前移动了M位。然后逆过来，就可以得到这个递推式。

因为求出的结果是数组中的下标，最终的编号还要加1

下面给出代码实现：

```c++
//约瑟夫环递推算法
/*
f(n, m) = (f(n - 1, m) + m) % n
n代表总人数，m代表报到m是要杀的数
*/

#include<stdio.h>
int main()
{
	//f=1为一个人的时候
	int i = 0, f = 1;
	int m, n;
	scanf("%d%d", &m, &n);
	for (i = 1; i <= n; ++i)
	{
		f = (f + m) % i;
	}
	printf("%d", f);
	return 0;
}
```



**为什么要讨论双向链表：**

**单链表**的结点→有指示后继的指针域→找后继结点方便;

​	  即:查找某结点的后继结点的执行时间为O(1)。

→无指示前驱的指针域→找前驱结点难:从表头出发查找。

​	  即:查找某结点的前驱结点的执行时间为O(n)。

**（可以用双向链表来克服单链表的缺陷）**

**双向链表：**在单链表的每个结点里再增加一个指向其直接前驱的指针域 prior，这样链表中就形成了有两个方向不同的链，故称为双向链表。



### d、双向链表的实现

#### 定义：

**双向链表：**在单链表的每个结点里再增加一个指向其直接前驱的指针域 prior，这样链表中就形成了有两个方向不同的链，故称为双向链表。

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230313211432315.png" alt="image-20230313211432315" style="zoom:50%;" />

**双向循环链表：**

和单链的循环表类似，双向链表也可以有循环表。

①让头结点的前驱指针指向链表的最后一个结点。

②让最后一个结点的后继指针指向头结点。

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230313212210115.png" alt="image-20230313212210115" style="zoom:50%;" />



#### 实现：

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230313211818316.png" alt="image-20230313211818316" style="zoom:50%;" />

**（1）、双链表的结构定义**

```c
typedef struct DuLNode
{
    Elemtype data;
    struct DuLNode *prior,*next;
}DuLNode,*DuLinkList;
```

**（2）、双向链表的插入**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230315204901224.png" alt="image-20230315204901224" style="zoom:50%;" />

①s->prior=p->prior;

②p->prior->next=s;

③s->next=p;

④p->prior=s;

```c
void Listlnsert_DuL(DuLinkList &L,int i,ElemType e)
{
    //GetElemP_DuL(L,i)为查找L中的第i个元素地址
    if(!(p=GetElemP_DuL(L,i))) return ERROR;
    s=new SuLNode;	s->data=e;
    //前驱和后继的更改连接
    s->prior=p->prior;
    p->prior->next=s;
    s->next=p;
    p->prior=s;
}
```

**（3）、双向链表的删除**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230315214131842.png" alt="image-20230315214131842" style="zoom:50%;" />

①p->prior->next=p->next;

②p->next->prior=p->prior;

```c
//删除带头结点的双向循环链表L的第i个元素，并用e返回。
void ListDelete_DuL(DuLink &L,int i,ElemType &e)
{
    if(!(p=GetElemP_DuL(L,i))) return ERROR;
    e=p->data;
    p->prior->next=p->next;
    p->next->prior=p->prior;
    free(p);
    return OK;
}
```

## 3、顺序表和链表的比较

![image-20230315221020784](C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230315221020784.png)

### a、链表

#### 存储优点：

①结点空间可以动态申请和释放;

②数据元素的逻辑次序靠结点的指针来指示，插***入和删除时不需要移动数据元素***。

#### 存储缺点：

①存储密度小，每个结点的***指针域需额外占用存储空间***。当每个结点的数据域所占字节不多时，指针域所占存储空间的比重显得很大。

②链式存储结构是***非随机存取***结构。对任一结点的操作都要从头指针依指针链查找到该结点，这增加了算法的复杂度。



**补：**

存储密度是指结点数据本身所占的存储量和整个结点结构中所占的存储量之比，即:

**存储密度=结点数据本身占用的空间 / 结点占用的空间总量**



## 4、线性表和链表的应用

### **a、线性表的合并**

**问题描述：**

假设利用两个线性表La和Lb分别表示两个集合A和B,现要求一个新的集合A=AUB

​	**La=(7,5,3,11)   Lb=(2,6,3)   →  La=(7,5,3,11,2,6)**

**算法步骤：**

依次取出Lb 中的每个元素，执行以下操作:

①在La中查找该元素

②如果找不到，则将其插入La的最后

```c
void union(List &La,List Lb)
{
    La_len=ListLength(La);
    Lb_len=ListLength(Lb);
    for(i=0;i<Lb_len;i++)
    {
        //将线性表L中的第i个位置的元素返回给e
        GetElem(Lb,i,e);
  //在线性表L中查找值为e的数据元素，返回其序列号（是第几个元素）
        //判断元素e是否在La中
        if(!LocateElem(La,e))
        {
            //在La中的La_len+1的位置插入e元素    
            Listlnsert(&La,++La_len,e);
        }
    }
}
```



### **b、有序表的合并**

**问题描述:**

已知线性表La和Lb中的数据元素按值非递减有序排列，现要求将La和Lb归并一个新的线性表Lc，且Lc中的数据元素仍按值非递减有序排列。

​	**La=(1,7,8)   Lb=(2,4,6,8,10,11)   →  Lc=(1,2,4,6,7,8,8,10,11)**

**（1）、用顺序表的实现**

**算法步骤：**

①创建一个空表Lc

②依次从La或Lb中“摘取”元素值较小的结点插入到Lc表的最后，直至其一个表变空为止

③继续将La 或 Lb其中一个表的剩余结点插入在Lc表的最后

```c
void MergeList_Sq(SqList LA,SqList LB,SqList &LC)
{
    pa=LA.elem;	//指针pa和pb的初始值分别指向连个表的第一个元素
    pb=LB.elem;
    LC.lenght=LA.lenght+LB.lenght;//新表LC长度为LA+LB
    LC.elem=new ElemType[LC.lemght];//为合并后的LC分配空间
    pc=LC.elem;	//指针pc指向LC的第一个元素
    //pa_last指向LA的最后一个元素
    pa_last=LA.elem+LA.lemght-1;
    //pb_last指向LB的最后一个元素
    pb_last=LB.elem+LB.lenght-1;
   
    //循环条件：pa和pb指针都未到达表尾（两表不为空）
    while(pa<=pa_last && pb<=pb_last)
    {
        //依次摘取LA和LB中较小的结点
        if(*pa<=*pb) *pc++=*pa++;
        else *pc++=*pb++;
    }
    //LB表已经到达表尾，将LA中剩余的元素加入LC中
    while(pa<=pa_last) *pc++=*pa++;
    //LA表已经到达表尾，将LB中剩余的元素加入LC中
    while(pb<=pb_last) *pc++=*pb++;
}
```

**（2）、用链表的实现**

```c
void MergeList(LinkList &La,LinkList &Lb,LinkList &Lc)
{
    pa=La->next; pb=Lb->next;
    pc=Lc=La;
    //循环条件为pa和pb指针都未指向NULL
    while(pa && pb)
    {
        //将pc指针指的next域指向较小的值所在的地址
        if(pa->data<=pb->data)
        {
            pc->next=pa;
            pc=pa;
            pa=pa->next;
        }
        else
        {
            pc->next=pb;
            pc=pb;
            pb=pb->next;
        }
    }
    pc->next=pa?pa:pb;	//插入剩余段
    delete[].. Lb;	//释放Lb的头结点
}
```

## 5、实列分析

### a、一元多项式的运算



### b、稀疏多项式的运算

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230317165245496.png" alt="image-20230317165245496" style="zoom:50%;" />

**（1）、顺序表的实现**

**算法步骤：**

①创建一个新数组c。

②分别从头遍历比较a和b的每一项：

​	指数相同，对应系数相加，若其和不为零，则在c中增加一个新项。

​	指数不相同，则将指数较小的项复制到c中。

③一个多项式已遍历完毕时，将另一个剩余项依次复制到c中即可。



**顺序存储结构存在问题**：

√存储空间分配不灵活

√运算的空间复杂度高



**（2）、链表的实现**

```c
typedef struct PNode
{
    float coef;		//系数
    intexpn;		//指数
    struct PNode *next;	//指针域
}PNode,*Polynomial;
```

**多项式创建算法步骤：**

①创建一个只有头结点的空链表。

②根据多项式的项的个数n，循环n次执行以下操作:

​	>>>生成一个新结点*s;

​	>>>输入多项式当前项的系数和指数赋给新结点*s的数据域;

​	>>>设置一前驱指针pre，用于指向待找到的第一个大于输入项指数的	结点	的前驱，pre初值指向头结点;

​	>>>指针q初始化，指向首元结点;

​	>>>循链向下逐个比较链表中当前结点与输入项指数，找到第一个大	于输	入项指数的结点*q;

​	>>>将输入项结点*s插入到结点*q之前。

**多项式相加算法步骤：**

①指针p1和p2初始化，分别指向Pa和Pb的首元结点。

②p3指向和多项式的当前结点，初值为Pa的头结点。

③当指针p1和p2均未到达相应表尾时，则循环比较p1和p2所指结点对应的指数值

​	(p1->expn与p2->expn)，有下列3种情况:

​	当p1->expn==p2->expn时，则将两个结点中的系数相加

​		·若和不为零，则修改p1所指结点的系数值，同时删除p2所指结点

​		·若和为零，则删除p1和p2所指结点;

​	当p1->expn < p2->expn时，则应摘取p1所指结点插入到“和多项式”链表。

​	·当p1->expn > p2->expn时，则应摘取p2所指结点插入到“和多项式”链表。

④将非空多项式的剩余段插入到p3所指结点之后。

⑤释放Pb的头结点。



# 四、栈和队列

**栈和队列是两种常用的、重要的数据结构**

**栈和队列是限定插入和删除只能在表的“端点”进行的线性表**

## 1、栈（stack）

**后进先出（栈尾插入，栈尾闪出）**

由于栈的操作具有后进先出的固有特性，使得栈成为程序设计中的有用工具。另外，如果问题求解的过程具有"后进先出"的天然特性的话，则求解的算法中也必然需要利用"栈”。

**案列：**

数制转换、表达式求值、括号匹配的检验

八皇后问题、行编辑程序、函数调用

迷宫求解、递归调用的实现



### a、定义和特点：

**定义：**

栈是仅在表尾进行插入、删除操作的线性表。

表尾(即a端)称为栈顶Top;表头(即a端)称为栈底Base

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230319163647161.png" alt="image-20230319163647161" style="zoom:50%;" />

**操作：**

插入元素到栈顶(即表尾)的操作，称为入栈。

从栈顶(即表尾)删除最后一个元素的操作，称为出栈。

**"入”=压栈=PUSH(x)**		**“出”=弹栈=POP( y)**



### b、栈的表示和操作实现

```c
ADT Stack 
{
    数据对象:
    D={ ai| ai ∈ElemSet, i=1,2...,n, n≥0 }
    数据关系:
    R1= {<ai-1, ai >| ai-1, ai∈D, i=2,...,n }
    约定an端为栈顶，a1端为栈底。
    基本操作:初始化、进栈、出栈、取栈顶元素等
}ADT Stack
```

#### 顺序栈（顺序表实现）

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230319200456835.png" alt="image-20230319200456835" style="zoom: 50%;" />

**存储方式:同一般线性表的顺序存储结构完全相同，**利用一组地址连续的存储单元依次存放自栈底到栈顶的数据元素。栈底一般在低地址端。

附设top指针，指示栈顶元素在顺序栈中的位置。

另设base指针，指示栈底元素在顺序栈中的位置。

但是，为了方便操作，**通常top指示真正的栈顶元素之上的下标地址**。

另外，用stacksize表示栈可使用的最大容量。



**栈的一些状态：**

空栈：base==top

栈满：top-base==stacksize

栈满时的处理方法：

​	①报错，返回操作系统

​	②分配更大的空间，作为栈的存储空间将原栈的内容移入新栈。



上溢(overflow):栈已经满，又要压入元素

下溢(underflow):栈已经空，还要弹出元素

注:上溢是一种错误，使问题的处理无法进行;而下溢十般认为是
—种结束条件，即问题处理结束。



**（1）、初始化操作**

```c
#define MAX 100
#define TRUE 1
#define FALSE 0
#define OK 1
#define ERROR 0
#define INFEASIBLE -1
#define OVERFLOW -2

typedef int Status;

typedef struct SqStack
{
    SElemType *base;	//栈底指针
    SElemType *top;		//栈顶指针
    int stacksize;	//栈可用容量
}SqStack;
```



```c
//构造一个空栈
Status lniStack(SqStack &S)
{
    S.base=new SElemType[MAX];
	//或 S.base=(SElemType*)malloc(MAX*sizeof(SElenType));
    if(!S.base) exit (OVERFLOW);	//内存分配失败
    S.top=S.base;	//栈顶指针等于栈底指针
    S.stacksize=MAX;
    return OK;
}
```

**（2）、销毁操作**

```c
Status DestroyStack(SqStack &S)
{
    if(S.base)
    {
        delete[].S.base;
        S.stacksize=0;
        S.base=S.top=NULL;
    }
    return OK;
}
```



**（3）、判定栈是否为空**

```c
Status StackEmpty(SqStack S)
{
    if(S.top==S.base) return TRUE;
    else return FALSE;
}
```



**（4）、求栈的长度**

```c
int StackLenght(SqStack S)
{
    return S.top-S.base;
}
```



**（5）、取栈顶元素**

```c

```



**（6）、栈置空操作**

```c
Status ClearStack(SqStack S)
{
    if(S.base) S.top=S.base;
    return OK;
}
```



**（7）、压栈**

①判断是否栈满，若满则出错（上溢)

②元素e压入栈顶

③栈顶指针加1

```c
Status Push(SqStack &S,SElem Typr e)
{
    if(S.top-S.base==S.stacksize) return ERROR;

    //*S.top++=e;
    *S.top=e;//由于一开始top指针是向上加1了的所以可以直接赋值e
    S.top++;
     
    return OK;
}
```



**（8）、弹栈**

①判断是否栈空，若空则出错（下溢）

②获取栈顶元素勇

③栈顶指针减一

```c
Status Pop(SqStack &S,SElemType &e)
{
    if(S.top == S.base) return ERROR;
    //e=*--S.top
    --S.top;  //由于一开始top指针是向上加1了的所以要先下移减1
    e=*S.top;
    return OK;
}
```

#### 链栈（链表实现）

**链栈是运算受限的单链表，只能在链表头部进行操作**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230321191920171.png" alt="image-20230321191920171" style="zoom:50%;" />

​										**注意：链栈中指针的方向**

```cpp
typedef struct StackNode
{
    SElemType data;
    //嵌套定义
    struct StackNode *next;
} StackNode,*LinkStack;
LinkStack S;
```

**（1）、链栈初始化**

```c++
void InitStack(LinkStack &S)
{
    //构造一个空栈，栈顶指针置为空
    S=NULL;
    return OK;
}
```

**（2）、判断链栈是否为空**

```c++
Status StackEmpty(LinkStack S)
{
    if(S==NULL) return TRUE;
    else return FALSE;
}
```

**（3）、链栈的压栈**

```c++
Status Push(LinkStack &S,SElemType e)
{
    p=new StackNode;	//生成新结点p
    p->data=e;	//将新结点数据域置为e
    p->next=S;	//将新结点插入栈顶
    S=p;		//修改栈顶指针
    return OK;
}
```

**（4）、链栈的弹栈**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230321195108723.png" alt="image-20230321195108723" style="zoom:50%;" />

```c++
Status Pop(LinkStack &S,SElemType &e)
{
    if(S==NULL) return ERROR;
    e=S->data;	//用e存储要删除的值
    p=S;		//将p指向S所在地址
    S=S->next;	//将S指针向下移动
    delete p;	//释放所需弹出的栈点
    return OK;
}
```

**（5）、取栈顶元素**

```c++
SElemType GetTop(LinkStack S)
{
    if(S!=NULL) return S->data;
}
```



### c、栈与递归

若一个对象部分地包含它自己，或用它自己给自己定义，则称这个对象是递归的;

若一个过程直接地或间接地调用自己,则称这个过程是递归的过程。

例如:递归求n的阶乘

```c++
long Fact (long n)
{
    if(n==0) 
        return 1;
    else 
        return n*Fact(n-1);
}
```



**（1）、以下三种情况常常用到递归方法**

①递归定义的数学函数

②具有递归特性的数据结构

③可递归求解的问题



**（2）、递归问题——用分治法求解**

分治法:对于一个较为复杂的问题，能够分解成几个相对简单的且解法相同或类似的子问题来求解

**必备的三个条件**

①能将一个问题转变成一个新问题，而新问题与原问题的解法相同或类同，不同的仅是处理的对象，且这些处理对象是变化有规律的

②可以通过上述转化而使问题简化

③必须有一个明确的递归出口，或称递归的边界



**递归函数调用的实现**

递归工作栈”———递归程序运行期间使用的数据存储区

"在作记录”→实在参教,居部变羞,返同地址



**（3）、递归的优缺点和改善**
优点:(结构清晰，程序易读
缺点:每次调用要生成工作记录，保存状态信息，入栈;返回时要出栈,恢复状态信息。时间开销大。

**递归→非递归**
方法1:尾递归、单向递归→循环结构

方法2:自用栈模拟系统的运行时栈



## 2、队列

**先进先出（队尾插入，队头删除）**

由于队列的操作具有先进先出的特性，使得队列成为程序设计中解决类似*排队问题*的有用工具。

**案列：**

①脱机打印输出:按申请的先后顺序依次输出。

②多用户系统中，多个用户排成队，分时地循环使用CPU和主存

③按用户的优先级排成多个队，每个优先级一个队列

④实时控制系统中，信号按接收的先后顺序依次处理

⑤网络电文传输，按到达的时间先后顺序依次进行

### a、特点和定义：

**定义：**

队列(queue)是一种先进先出(Frist In Frist Out ----FIFO)的线性表。在表一端插入（表尾)，在另一端(表头）删除。

**操作：**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230319165538763.png" alt="image-20230319165538763" style="zoom:50%;" />



### b、队列的表示和操作的实现

```c++
ADT Queue
{
数据对象D={alaklemSet,i=1,2... n9)
数据关系: R={<a;1a>la1,aED,i=2..,n)约定其中a端为队列头，a,端为队列尾。
    基本操作:
	lnitQueue(&Q)操作结果:构造空队列Q
	DestroyQueue(&Q)条件:队列Q已存在;操作结果:队列Q被销毁		
    ClearQueue(&Q)条件:队列Q已存在;操作结果:将Q清空
	QueueLength(Q)条件:队列Q已存在―操作结果:返回Q的元素个数，						即队长
    GetHead(Q,&e)条件:Q为非空队列―操作结果:用e返回Q的队头元素	  EnQueue(&Q e)条件:队列Q已存在―操作结果:插入元素e为Q的队尾					   元素	
    DeQueue(&Q, &e)条件:Q为非空队列︰操作结果:删除Q的队头元						素，用e返回值
        .....还有将队列置空、遍历队列等操作......
}ADT Queue

```

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230322204430100.png" alt="image-20230322204430100" style="zoom:50%;" />

**解决假上溢的方法**
1、将队中元素依次向队头方向移动。
缺点:浪费时间。每移动一次，队中元素都要移动。
2、将队空间设想成一个循环的表，即分配给队列的m个存储单元可以循
环使用，当rear为maxqsize时，若向量的开始端空着，又可从头使用空
着的空间。当front为maxqsize时，也是一样。

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230322204829962.png" alt="image-20230322204829962" style="zoom:50%;" />



**解决假上溢的方法——引入循环队列**
base[0]接在base[MAXQSIZE-1]之后，若rear+1==M，则令rear=o;实现方法:利用模(mod，C语言中:%)运算。
插入元素:Q.base[Q.rear]=x;
			     Q.rear=(Q.rear+1)% MAXQSIZE;
删除元素: x=Q.base[s.front]
				 Q.front=(Q.front+1)% MAXQSIZE

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230323161609874.png" alt="image-20230323161609874" style="zoom:50%;" />

**如何判断队空和**

出队移动front队头指针

入队移动rear队尾指针

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230323162238323.png" alt="image-20230323162238323" style="zoom:50%;" />

当队满和队空时，front和rear都指向同一个位置，应该如何判断什么时候队为空，什么时候队为满？

**解决办法：**
1.另外设、一个标悬以区别队空、队满

2.另设一个变童，记录元素个数

***3.少用一个元素空间***



**循环队列解决队满时判断方法——少用一个元素空间:**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230323163129960.png" alt="image-20230323163129960" style="zoom:50%;" />





#### 顺序队（顺序表实现）

**（1）、队列的表示**

```c++
#define MAXQSIZE 100		//最大队列长度
Typedef struct
{
    QElemType *base;	//初始化的动态分配存储空间
    int front;		//头指针
    int rear;		//尾指针
}SqQueue;
```



**（2）、队列的初始化**

```c++
Srarus InitQueue(SqQueue &Q)
{
//Q.base(QElemTyope*)malloc(MAXQSIZE*sizeof(QElemType))
    Q.base=new QElemType[MAXQSIZE]; //分配数组空间
    if(Q.base==NULL) exit(OVERFLOW);//空间分配失败
    Q.front=0；	//头指针和尾指针置为0，队列为空
    Q.rear=0;	
    return OK;
}
```



**（3）、求队列长队**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230323164547991.png" alt="image-20230323164547991" style="zoom: 50%;" />

```c++
int QueueLenght(SqQueue Q)
{
    return((Q.rear-Q.front+MAXQSIZE)%MAXQSIZE);
}
```



**（4）、入队**

base[0]接在base[MAXQSIZE-1]之后，若rear+1==M，则令rear=o;实现方法:利用模(mod，C语言中:%)运算。
插入元素：Qbase[Qrear])
			       Qrear=(Qrear+1)%MAXQSIZE;

```c++
Status EnQueue(SqQueue &Q,QElemType e)
{
    if((Q.rear+1)%MAXSIZE==Q.front) return ERROR; //队满
    Q.base[Q.rear]=e;	//新元素加入队尾
    Q.rear=(Q.rear+1)%MAXQSIZE;	//队尾指针+1
    return OK;
}
```



**（5）、出队**

```c++
Starus DeQueue(SqQueue &Q,QElemType e)
{
    if(Q.rear==Q.front) return ERROR;	//队空
    e=Q.base[Q.front];	//保存队头元素
    Q.rear=(Q.rear+1)%MAXQSIZE;		//对头+1
    return OK;
}
```



**（6）、取队头元素**

```c++
SEemType GetHead(SqQuere Q)
{
    if(Q.front!=Q.rear)		//队列不为空
        return Q.base[Q.front];	//返回队头指针元素的值，对头指针不变
}
```



#### 链队（链表实现）

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230406194405006.png" alt="image-20230406194405006" style="zoom:50%;" />

```c++
#define Max 100		//最大队列长度
typedef struct Qnode
{
    QElemType data;
    stuct Qnode* next;
}QNode,*QuenePtr;

typedef struct
{
    QuenePtr front;	//队头指针
    QuenePtr rear;	//队尾指针
}LinkQueue;
```



**1、链队列的初始化**

```c++
Status InitQueue(LinkQueue &Q)
{
    Q.front=Q.rear=(QueuePtr)malloc(sizeof(QNode));
    if(!Q.front)exit(OVERFLOW);
    Q.front->next=NULL;
    return OK;
}
```



**2、销毁链队列**

```c++
Status DestroyQueue(LinkQUEUE &Q)
{
    QNode *p=NULL;
    while(Q.front)
    {
        p=Q.front->next;
        free(Q.front);
        Q.front=p;
    }
    return OK;
}
```



**3、入队**

```c++
Status EnQueue(LinkQueue &Q,QElenType e)
{
    p=(QueuePtr)malloc(sizeof(QNode));
    if(!p) exit(OVERFLOw);
    p->data=e;
    p->next=NULL;
    Q.rear=p;
    return OK;
}
```



**3、出队**

```C++
Status DeQueue(LinkQueue &Q,QElemType &e)
{
    if(Q.front==Q.rear) return ERROR;
    p=Q.front->next;
    e=p->data;
    Q.front->next=p->next;
    //当出队为尾结点时，要改变尾指针
    if(Q.rear==p) Q.rear=Q.front;
    free(p);
    return OK;
}
```



**4、求链队列的队头元素**

```c++
Status GetHead(LinkQueue Q,QElemType &e)
{
    if(Q.front==Q.rear) return ERROR;
    e=Q.front->next->data;	//跳过头结点
    return 0;
}
```





## 3、案列引入

### a、表达式求值(算符优先级法)

**为了实现表达式求值。需要设置两个栈:**

​	一个是算符栈OPTR，用于寄存运算符。

​	另一个称为操作数栈OPND，用于寄存运算数和运算结果。

**求值的处理过程是自左至右扫描表达式的每一个字符**

**·当扫描到的是运算数则将其压入栈OPND**

**·当扫描到的是运算符时**

​	*·若这个运算符比OPTR栈顶运算符的优先级高，则入栈OPTR，继续向后处理。*

​	*·若这个运算符比OPTR栈顶运算符优先级低，则从OPND栈中弹出两个运算数，从栈OPTR中弹出栈顶运算符进行运算，并将运算结果压入栈OPND。*

继续处理当前字符，直到遇到结束符为止。

3*2-2^2/4+6



# 五、串、数组和广义表



## 1、串

串（string）---- 零个或多个任意字符组**成的有限序列**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230406202028385.png" alt="image-20230406202028385" style="zoom:50%;" />

**几个术语：**

①子串：一个串中任意个连续字符组成的子序列(含空串)称为该串的子串。（真子串是指不包含自身的所有子串。）

②主串：包含子串的串相应地称为主串

③字符位置：字符**在序列中的序号**为该字符在串中的位置

④子串位置：子串第一个字符在主串中的位置

⑤空格串（空格作为内容）：由一个或多个空格组成的串与**空串不同**（无任何内容）

⑥串相等**（完全相等）**：当且仅当两个串的长度相等并且各个对应位置上的字符都相同时，这两个串才是相等的。
如:
" abcd” ≠ "abc"

" abcd” : "abcde"

所有空串相等

### a、串的类型定义、存储结构及运算

**串的定义：**

```c
ADT String 
{
数据对象: D = {a l a, e CharacterSet, i = 1,2,…, n, n ≥ 0}
数据关系: R = {< a 1, a; >| a_1,a, e D, i = 1,2,….， n}

基本操作:
(1)、StrAssign (&T,chars)		//串赋值
(2)、StrCompare (S,T)			//串比较
(3)、StrLength (S)			//求串长
(4)、Concat(&T,S1,S2)			//串连结
(5)、SubString(&Sub,S,pos,len)//求子串
(6)、StrCopy(&T,S)			//串拷贝
(7)、StrEmpty(S)				//串判空
(8)、ClearString (&S)			//清空串
(9)、Index(S,T,pos)			//子串的位置
(11)、Replace(&S,T,V)			//串替换
(12)、StrInsert(&S,pos,T)		//子串插入
(12)、StrDelete(&S,pos,len)	//子串删除
(13)、DestroyString(&S)		//串销毁
    
}ADT String

```



#### **串的存储结构：**

**①串的顺序存储结构**

```c++
#define MAXLEN 255
typedef struct
{
	hay ch[MAXLEN+1];	//存储串的一维数组
    int length;		//串的当前长度长度
}SString;
```



**②串的链式存储结构**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230406205858776.png" alt="image-20230406205858776" style="zoom:50%;" />

```c++
#define CH 80
typedef statuct Chunk
{
    char ch[CH];
    struct Chunk*next;
}Chunk;

typedef Struct
{
    Chunk*head,*tail;//串的头指针和尾指针
    int curlen;//串的当前长度
}LString;//字符串的快链结构
```



#### **串的模式匹配算法**：

算法目的：确定主串中所含子串（模式串）第一次出现的位置。

算法应用：搜素引擎、拼写检查、语言翻译、数据压缩

算法种类：

①BF算法（Brute-Force，又称古典算法，朴素。特点：慢而简单）

②KMP算法（特点：快而复杂）



##### **BF算法（穷举法）：**

算法的思路是从S的每一个字符开始依次T的字符进行匹配。

a a b d a b c d y r f d e a d

a b c d

```c
int Index_BF(SString S,SString T)
{
    int i=0,j=0;
    while(i < S.length && j < T.lenngth)
    {
        if(s.ch[i]==t.ch[j])
        {
            ++i;
            ++j;
        }
        else
        {
            i=i-j+1;	//回溯子串和主串的位置
	        j=1;	
        }
    }
    if(j>=T.length-1) return i-T.length;
    else return 0;
}
```



##### **KMP算法：**

KMP解决的问题类型
KMP算法的作用是在一个已知字符串中查找子串的位置,也叫做串的模式匹配。比如主串s=“university”,子串t=“sit”。现在我们要找到子串t 在主串s 中的位置。大家肯定觉得这还不简单，不就在第七个嘛，一眼就看出来了。
当然，在字符串非常少时，“肉眼观察法”不失为一个好方法。但如果要你在一千行文本里找一个单词，我想一般人都会数得崩溃吧。这就让我想起来考试的时候，如果一两道选择题不会。这时候，“肉眼观察法”可能效果不错，但是如果好几道大题不会呢？“肉眼观察法”就丝毫不起效了。所以打铁还需自身硬，我们把这种枯燥的事以一定的算法交给计算机处理。
第一种我们容易想到的就是暴力求解法。
这种方法也叫朴素的模式匹配：

简单来说就是：从主串s 和子串t 的第一个字符开始，将两字符串的字符一一比对，如果出现某个字符不匹配，主串回溯到第二个字符，子串回溯到第一个字符再进行一一比对。如果出现某个字符不匹配，主串回溯到第三个字符，子串回溯到第一个字符再进行一一比对…一直到子串字符全部匹配成功。

大家可能会想：这个方法也太慢了吧！求一个子串位置需要太多的步骤。而且很多步骤根本不必要进行。
这个想法非常好！！很多伟大的思想都是在一步步完善更正已有方法中诞生的。这种算法在最好情况下时间复杂度为O(n)。即子串的n个字符正好等于主串的前n个字符，而最坏的情况下时间复杂度为O(m*n)。相比而言这种算法空间复杂度为O(1)，即不消耗空间而消耗时间。

下面就开始进入我们的正题：KMP算法是怎样优化这些步骤的。其实KMP的主要思想是：“空间换时间”。
大家打起精神，认真看下面的内容。
首先，为什么朴素的模式匹配这么慢呢？
你再回头看一遍就会发现，哦，原来是回溯的步骤太多了。所以我们应该尽量减少回溯的次数。
怎样做呢？比如上面第一个图：当字符’d’与’g’不匹配，我们保持主串的指向不变，
主串依然指向’d’，而把子串进行回溯，让’d’与子串中’g’之前的字符再进行比对。
如果字符匹配，则主串和子串字符同时右移。
至于子串回溯到哪个字符，这个问题我们先放一放。

我先提出一个概念：一个字符串最长相等前缀和后缀。
教科书常用的手段是：在此处摆出一堆数学公式让大家自行理解。

<img src="https://img-blog.csdnimg.cn/2020021910504033.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NjAwNzI3Ng==,size_16,color_FFFFFF,t_70" alt="在这里插入图片描述"  />

这也是为什么看计算机学科的书没有较好的数学基础会很痛苦。（当初我为什么不好好学数学T_T）
大家先不要强行理解数学公式，且听我慢慢道来：
我给大家个例子。
字符串 abcdab
前缀的集合：{a,ab,abc,abcd,abcda}
后缀的集合：{b,ab,dab,cdab,bcdab}
那么最长相等前后缀不就是ab嘛.

做个小练习吧:
字符串：abcabfabcab中最长相等前后缀是什么呢：
对就是abcab
好了我们现在会求一个字符串的前缀，后缀以及最长相等前后缀了。
这个概念很重要。到这里如果都看懂了，可以鼓励一下自己，然后回想一遍，再往下看。
之前留了一个问题，子串回溯到哪个字符，现在可以着手解决了。

**图解KMP**
现在我们先看一个图：第一个长条代表主串，第二个长条代表子串。红色部分代表两串中已匹配的部分，
绿色和蓝色部分分别代表主串和子串中不匹配的字符。
再具体一些：这个图代表主串"abcabeabcabcmn"和子串"abcabcmn"。

<img src="https://img-blog.csdnimg.cn/2020021815305891.png" alt="在这里插入图片描述" style="zoom:80%;" />

<img src="https://img-blog.csdnimg.cn/20200218154423760.png" alt="在这里插入图片描述" style="zoom:80%;" />

现在发现了不匹配的地方，根据KMP的思想我们要将子串向后移动，现在解决要移动多少的问题。
之前提到的最长相等前后缀的概念有用处了。因为红色部分也会有最长相等前后缀。如下图：

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200218190924976.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NjAwNzI3Ng==,size_16,color_FFFFFF,t_70)

<img src="https://img-blog.csdnimg.cn/20200218154514719.png" alt="在这里插入图片描述" style="zoom:80%;" />

灰色部分就是红色部分字符串的最长相等前后缀，我们子串移动的结果就是让**子串的红色部分最长相等前缀和主串红色部分最长相等后缀对齐。**

<img src="https://img-blog.csdnimg.cn/20200218185542937.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NjAwNzI3Ng==,size_16,color_FFFFFF,t_70" alt="在这里插入图片描述" style="zoom: 80%;" />

<img src="https://img-blog.csdnimg.cn/2020021815504814.png" alt="在这里插入图片描述" style="zoom:80%;" />

这一步弄懂了，KMP算法的精髓就差不多掌握了。接下来的流程就是一个循环过程了。事实上，**每一个字符前的字符串都有最长相等前后缀**，而且**最长相等前后缀的长度是我们移位的关键**，所以我们单独用一个next数组存储子串的最长相等前后缀的长度。**而且next数组的数值只与子串本身有关。**
所以next[i]=j,含义是：**下标为i 的字符前的字符串最长相等前后缀的长度为j。**
我们可以算出，子串t= "abcabcmn"的next数组为next[0]=-1(前面没有字符串单独处理)
next[1]=0；next[2]=0；next[3]=0；next[4]=1；next[5]=2；next[6]=3；next[7]=0；
| a | b |c |a |b | c | m |n |
|–|–|–|–|–|–|–|–|–|–|
|next[0] |next[1] | next[2] | next[3] |next[4] |next[5] | next[6] | next[7] |
|-1 | 0 |0 | 0 | 1 | 2 |3 | 0 |

本例中的蓝色c处出现了不匹配（是s[5]!=t[5]）

<img src="https://img-blog.csdnimg.cn/20200218154514719.png" alt="在这里插入图片描述" style="zoom: 80%;" />

我们把子串移动，也就是让s[5]与t[5]前面字符串的最长相等前缀后一个字符再比较，而该字符的位置就是t[？],很明显这里的？是2，就是**不匹配的字符前的字符串 最长相等前后缀的长度。**

<img src="https://img-blog.csdnimg.cn/2020021815504814.png" alt="在这里插入图片描述" style="zoom: 80%;" />

**也是不匹配的字符处的next数组next[5]应该保存的值，也是子串回溯后应该对应的字符的下标。** 所以？=next[5]=2。接下来就是比对是s[5]和t[next[5]]的字符。这里也是最奇妙的地方，也是为什么KMP算法的代码可以那么简洁优雅的关键。
我们可以总结一下，next数组作用有两个：



**一是之前提到的：**

***next[i]的值表示下标为i的字符前的字符串最长相等前后缀的长度。***

**二是：**

***表示该处字符不匹配时应该回溯到的字符的下标***



next有这两个作用的源头是：之前提到的字符串的最长相等前后缀
想一想是不是觉得这个算法好厉害，从而不得不由衷佩服KMP算法的创始人们。

**KMP算法的时间复杂度**
现在我们分析一下KMP算法的时间复杂度：
KMP算法中多了一个求数组的过程，多消耗了一点点空间。我们设主串s长度为n,子串t的长度为m。求next数组时时间复杂度为O(m)，因后面匹配中主串不回溯，比较次数可记为n，所以KMP算法的总时间复杂度为O(m+n)，空间复杂度记为O(m)。相比于朴素的模式匹配时间复杂度O(m*n)，KMP算法提速是非常大的，这一点点空间消耗换得极高的时间提速是非常有意义的，这种思想也是很重要的。
下面还有更厉害的，我们一起来分析具体的代码。

**求next数组的代码**

***如何找next数组？***

下面我们一起来欣赏计算机如何求得next数组的

```c
typedef struct
{	
	char data[MaxSize];
	int length;			//串长
} SqString;
//SqString 是串的数据结构
//typedef重命名结构体变量，可以用SqString t定义一个结构体。
void GetNext(SqString t,int next[])		
{
	int j,k;
	j=0;k=-1;
    //记录第i个字符前的字符串的最长相等前后缀的长度
	next[0]=-1;//第一个字符前无字符串，给值-1
    	//0 1 2 3 4 5 6 7
		//a b c a m c a a
	   //-1 0 0 0 1 0 0 1
/*
当i个字符前的字符串中出现第0个字符和第i - 1个字符相等时，会继续对 1和i、2和i+1 等等往后比较直到出现不同位止。又回溯到第0个字符（k回溯到-1）和第i个字符（j不变继续往后比较）比较。
*/
	while (j<t.length-1) 
	{	
        //k为-1或比较的字符相等时
		if (k==-1 || t.data[j]==t.data[k]) 	
		{	
			j++;k++;
			next[j]=k;
       	}
       	else
		{
            /*
            回溯k：
            1、当已经找到t.data[j]==t.data[k]时，而再往后
            就出现不相等的情况。
            2、判断出现相等前后缀失败时。
            */
			k=next[k];
		}
	}
}
```

**解释next数组构造过程中的回溯问题**
大家来看下面的图：
下面的长条代表子串，红色部分代表当前匹配上的最长相等前后缀，蓝色部分代表t.data[j]。

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200218171456398.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NjAwNzI3Ng==,size_16,color_FFFFFF,t_70)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200218171509500.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NjAwNzI3Ng==,size_16,color_FFFFFF,t_70)

**KMP算法代码解释**

```c
//s为主串，t为子串
int KMPIndex(SqString s,SqString t)  //KMP算法
{

	int next[MaxSize],i=0,j=0;
	GetNext(t,next);
	while (i<s.length && j<t.length) 
	{
		if (j==-1 || s.data[i]==t.data[j]) 
		{
			i++;j++;  			//i,j各增1
		}
		else j=next[j]; 		//i不变,j后退,让子串回退
    }
    if (j>=t.length)
		return(i-t.length);  	//返回匹配模式串的首字符下标
    else  
		return(-1);        		//返回不匹配标志
}
```

**KMP算法的改进**

为什么KMP算法这么强大了还需要改进呢？
大家来看一个例子:
主串s=“aaaaabaaaaac”
子串t=“aaaaac”

next =-101234

这个例子中当‘b’与‘c’不匹配时应该‘b’与’c’前一位的‘a’比,这显然是不匹配的。'c’前的’a’回溯后的字符依然是‘a’。
**我们知道没有必要再将‘b’与‘a’比对了**，因为回溯后的字符和原字符是相同的，原字符不匹配，回溯后的字符自然不可能匹配。但是KMP算法中依然会将‘b’与回溯到的‘a’进行比对。这就是我们可以改进的地方了。我们改进后的next数组命名为：nextval数组。KMP算法的改进可以简述为： **如果a位字符与它next值指向的b位字符相等，则该a位的nextval就指向b位的nextval值，如果不等，则该a位的nextval值就是它自己a位的next值。** 这应该是最浅显的解释了。如字串"ababaaab"的next数组以及nextval数组分别为：

| 下标 |0|1|2|3|4|5|6|7
|–|–|–|–|–|–|–|–|–|–|
| 子串 |   | a | b| a| b| a|a|a|b|
|next 	  |-1| 0 | 0|1 |2 |3|1|1|
|nextval  |-1| 0 |-1|0 |-1|3|1|0|

我们来分析下代码：

```c
void GetNextval(SqString t,int nextval[])  
//由模式串t求出nextval值
{
	int j=0,k=-1;
	nextval[0]=-1;
   	while (j<t.length) 
	{
       	if (k==-1 || t.data[j]==t.data[k]) 
		{	
			j++;k++;
			if (t.data[j]!=t.data[k]) 
//这里的t.data[k]是t.data[j]处字符不匹配而会回溯到的字符
//为什么？因为没有这处if判断的话，此处代码是next[j]=k;
//next[j]不就是t.data[j]不匹配时应该回溯到的字符位置嘛
				nextval[j]=k;
           	else  
				nextval[j]=nextval[k];
//这一个代码含义是不是呼之欲出了？
//此时nextval[j]的值就是就是t.data[j]不匹配时应该回溯到的字符的nextval值
//用较为粗鄙语言表诉：即字符不匹配时回溯两层后对应的字符下标
       	}
       	else  k=nextval[k];    	
	}

}
```

**例如：**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230415140233130.png" alt="image-20230415140233130" style="zoom: 67%;" />

1.第一位的nextval值必定为0，第二位如果于第一位相同则为0，如果不同则为1。
2.第三位的next值为1，那么将第三位和第一位进行比较，均为a，相同，则第三位的nextval值为第一位的next值，为0。
3.第四位的next值为2，那么将第四位和第二位进行比较，不同，则第四位的nextval值为其next值，为2。
4.第五位的next值为2，那么将第五位和第二位进行比较，相同，第二位的next值为1，则继续将第二位与第一位进行比较，不同，则第五位的nextval值为第二位的next值，为1。
5.第六位的next值为3，那么将第六位和第三位进行比较，不同，则第六位的nextval值为其next值，为3。
6.第七位的next值为1，那么将第七位和第一位进行比较，相同，则第七位的nextval值为0。7.第八位的next值为2，那么将第八位和第二位进行比较，不同，则第八位的nextval值为其next值，为2。

```c
int KMPIndex1(SqString s,SqString t)    
//修正的KMP算法
//只是next换成了nextval
{
	int nextval[MaxSize],i=0,j=0;
	GetNextval(t,nextval);
	while (i<s.length && j<t.length) 
	{
		if (j==-1 || s.data[i]==t.data[j]) 
		{	
			i++;j++;	
		}
		else j=nextval[j];
	}
	if (j>=t.length)  
		return(i-t.length);
	else
		return(-1);
}

```





## 2、数组

**定义：**

按一定格式排列起来的，具有相同类型的数据元素的集合。

**一维数组（略）**



**二维数组：**

![image-20230415152244063](C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230415152244063.png)



二维数组：若一维数组中的数据元素又是一维数组结构，则称为二维数组。

二维数组的逻辑结构：

①非线性结构：每一个数据元素既在一个行表中，又在一个列表中。
②线性结构：该线性表的每个数据元素也是一，定长的线性表个定长的线性表。



**三维数组：**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230416094017269.png" alt="image-20230416094017269" style="zoom: 50%;" />

例如：

```c
int arrr[Max]={ar1[3][3],ar2[3][3],…………};
```





### a、数组的顺序存储

数组特点：结构固定——维数和维界不变。

数组基本操作:初始化、销毁、取元素、修改元素值，一般不做插入和删除操作。

所以：一般都是采用顺序存储结构来表示数组。

注意：数组可以是多维的，但存储数据元素的内存单元地址是一维的，因此，在存储数组结构之前，需要解决将多维关系映射到一维关系的问题。



**以行序为主序：**

存储单元是一维结构，而数组是个多维结构,则用一组连续存储单元存放数组的数据元素就有个次序约定问题。

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230415161801037.png" alt="image-20230415161801037" style="zoom:50%;" />



**以列序为主：**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230415161920036.png" alt="image-20230415161920036" style="zoom:50%;" />



<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230416095324206.png" alt="image-20230416095324206" style="zoom:67%;" />



### b、特殊矩阵的压缩存储

 

**矩阵:**一个由mxn个元素排成的m行n列的表。

**矩阵的常规存储:**
①将矩阵描述为一个二维数组。

**矩阵的常规存储的特点:**
①可以对其元素进行随机存取;
②矩阵运算非常简单;存储的密度为1。

**不适宜常规存储的矩阵：**值相同的元素很多且呈某种规律分布;零元素多。

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230416095712745.png" alt="image-20230416095712745" style="zoom:50%;" />

**矩阵的压缩存储：**为多个相同的非零元素只分配一个存储空间;对零元素不分配空间。



**1.什么是压缩存储?**
若多个数据元素的值都相同，则只分配一个元素值的存储空间，且零元素不占存储空间。

**2.什么样的矩阵能够压缩?**
一些特殊矩阵，如:对称矩阵，对角矩阵，三角矩阵，稀疏矩阵等。

**3.什么叫稀疏矩阵?**
矩阵中非零元素的个数较少（一般小于5%)



#### （1）对称矩阵

**特点**：在nxn的矩阵a中，满足如下性质:
											**a(ij)=a(ji) (1≤i, j≤n)**

**存储方法**：只存储下(或者上)三角(包括主对角线)的数据元素。共占用**n(n+1)/2**个元素空间。



**对称矩阵的存储结构:**
对称矩阵上下三角中的元素数均为:n(n + 1)/2
可以以行序为主序将元素存放在一个一维数组sa [n(n+1)/2]中。

例如：以行序为主序存储下三角（一维数组）:

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230416100401075.png" alt="image-20230416100401075" style="zoom:50%;" />

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230416103155135.png" alt="image-20230416103155135" style="zoom:50%;" />





#### （2）三角矩

**特点：**对角线以下(或者以上)的数据元素(不包括对角线)全部为常数
<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230416112318091.png" alt="image-20230416112318091" style="zoom:50%;" />
**存储方法：**重复元素c共享一个元素存储空间，共占用n(n+1)/2+1个元素空间: sa[1...n(n+1)/2+1]

**下三角矩阵：**

(i-1)×(2n-i+2)/2+j-i+1 	i≥j（存储下标位置）

n(n+1)/2+1					 i<j （占用空间）

**上三角矩阵：**

(i-1)×(2n-i+2)/2+j-i+1    i≤j（存储下标位置）

n(n+1)/2+1					i>j（占用空间）



#### （3）对角矩阵（带状矩阵）

[特点]在nxn的方阵中，所有非零元素都集中在以在对角线为中心的带状区域中，区域外的值全为0，则称为对角矩阵。常见的有三对角矩阵、五对角矩阵、七对角矩阵等。

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230416115724519.png" alt="image-20230416115724519" style="zoom:50%;" />

以对角线的顺序存储：

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230416123638240.png" alt="image-20230416123638240" style="zoom:50%;" />



### d、稀疏矩阵的压缩

**稀疏矩阵：**设在mxn的矩阵中有t个非零元素。
					令= t/(m x n)
					当ð ≤0.05时称为**稀疏矩阵。**

#### **三元组法**

三元组( i, j, a(ji) )惟一确定矩阵的个非零元。

例如：
<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230416132043885.png" alt="image-20230416132043885" style="zoom:50%;" />

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230420185615326.png" alt="image-20230420185615326" style="zoom:50%;" />

**压缩存储原则：**存各非零元的值、行列位置和矩阵的行列数。

三元组的不同表示方法可决定稀疏矩阵不同的压缩存储方法。

**注意：**为更可靠描述，通常再加一个“总体”信息:即总行数、总列数、非零元素总个数。

例如：

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230420190001195.png" alt="image-20230420190001195" style="zoom:50%;" />



三元组顺序表又称有序的双下标法。

**三元组顺序表的优点：**非零元在表中按行序有序存储，因此便于进
行依行顺序处理的矩阵运算。

**三元组顺序表的缺点：**不能随机存取,若按行号存取某一行中的非
零元，则需从头开始进行查找。



#### 链式存储结构（十字链表）

**优点：**它能够灵活地插入困运算而产生的新的非零元素,删除因运算而产生的新的零元素，实现矩阵的各种运算。

十字链表中结点的结构示意图：

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230420190756067.png" alt="image-20230420190756067" style="zoom: 50%;" />

①right：用于连接同一行中的下移个非零元素。

②down：用于连接同一列中的下一个非零元素。

**例如：**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230420191822930.png" alt="image-20230420191822930" style="zoom:50%;" />

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230420191907552.png" alt="image-20230420191907552" style="zoom:50%;" />





## 3、广义表

### **定义**

**（可以存储不同类型的数据）：**

**广义表（又称列表Lists）**是n>=0个元素a0,a1,……,a(n-1)的有限序列，其中每一个ai或者是原子，或者是一个广义表。

**注意事项：**

广义表通常记作: LS=(a1, a2，..., an)
	其中：LS为表名，n为表的长度，每一个ai为表的元素。

习惯上，一般用大写字母表示广义表，小写字母表示原子。

表头：若LS非空(n>=1)，则其第一个元素a1就是表头。
记作head(LS)=a1。
注:表头可以是原子，也可以是子表。

**表尾：除表头之外的其它元素组成的表。**
			记作tail(LS) = (a2,.... ,an)。
注:表尾不是最后一个元素，而是一个子表。



  例如：

(1)A=()		   	  空表，长度为0。
(2)B=(())			  长度为1，表头、表尾均为()。

(3)C=(a, (b,c)）  长度为2，由原子a和子表(b,c)构成。
							表头为a，表尾为((b,c))。

(4) D=(x y, z)	   长度为3，每一项都是原子。
							 表头为×;表尾为(y,z)。

(6)F=(a,F)			长度为2，第一项为原子，第二项为它本身。
							表头为a;表尾为(F)。
							F=(a,(a,(a,……)))



### 性质

注：大写的字母为一个表	如：A为（a，b）

(1)、广义表中的数据元素有相对**次序**，**一个直接前驱和一个直接后继**。

(2)、广义表的**长度**定义为最外层所包含元素的个数;
			如: C=(a,(b, c))是长度为2的广义表。

(3)、广义表的**深度**定义为该广义表**展开后所含括号的重数**;
A=(b, c)的深度为1，B=(A, d)的深度为2，C=(f, B, h)的深度为3。        			注意：“原子”的深度为0，“空表”的深度为1。

(4)广义表可以为其他广义表**共享**，如：广义表B就共享表A。
	在B中不必列出A的值，而是通过名称来引用，B= (A)。

(5)广义表可以是一个**递归**的表。如:F=(a,F)=(a, (a, (a,..)>)
	**注意：递归表的深度是无穷值，长度是有限值。**

(6)广义表是**多层次**结构，广义表的元素可以是单元素，也可以
是子表，而子表的元素还可以是子表，..。
可以用**图形**象地表示。
例：D=(E F)，其中：E=(a, (b,c))	F=(d, (e))

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230420195529326.png" alt="image-20230420195529326" style="zoom:50%;" />





# 六、树和二叉树

## 1、树

### 树的定义：

**树(Tree)**是n (n≥0)个结点的**有限集**。
	若n = 0，称为空树;
	若n > 0，则它满足如下两个条件:
		(1)有且仅有一个特定的称为根(Root)的结点;
		(2)其余结点可分为m (m≥0)个互不相交的**有限集**T1,T2,T3,...
Tm，其中每一个集合本身又是一棵树，并称为根的**子树**(SubTree)。

**注：本质为递归**



### 树的基本术语：

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230420204537811.png" alt="image-20230420204537811" style="zoom:80%;" />



<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230420204922881.png" alt="image-20230420204922881" style="zoom:50%;" />

**有序树:** 树中结点的各子树从左至右有次序(最左边的为第一个孩子)。

**无序树: **树中结点的各子树无次序。



<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230420205106962.png" alt="image-20230420205106962" style="zoom:50%;" />

**森林 :**是m (m≥0)棵**互不相交**的树的集合。

把根结点删除树就变成了森林。
一棵树可以看成是一个特殊的森林。
给森林中的各子树加上一个双亲结点，森林就变成了树。



## 2、二叉树

### 二叉树的定义：

为何要重点研究每结点最多只有两个“叉”的树?

√二叉树的结构最简单，规律性最强；
√可以证明，所有树都能转为唯一对应的二叉树，不失一般性。

普通树(多叉树)若不转化为二叉树，则运算很难实现。



**定义：**二叉树是n(n>=0)个结点的有限集，它或者是空集(n= O)，或者由一个**根结点**及**两棵互不相交**的分别称作这个根的**左子树**和**右子树**的二叉树组成。

1、每个结点最多有俩孩子(二叉树中不存在度大于2的结点)。

**2、子树有左右之分，其次序不能颠倒。**

3、二叉树可以是空集合，根订以有空的左子树或空的右子树。



**注意：二叉树不是树的特殊情况，它们是两个概念。**

**二叉树**结点的子树要区分左子树和右子树，即使只有一棵子树也行区分，说明它是左子树，还是右子树。
**树**当结点只有一个孩子时，就无须区分它是左还是右的次序。因此二者是不同的。这是二叉树与树的最主要的差别。

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230420210017735.png" alt="image-20230420210017735" style="zoom: 50%;" />

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230421100316121.png" alt="image-20230421100316121" style="zoom:50%;" />



**二叉树的基本形态：**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230421100140898.png" alt="image-20230421100140898" style="zoom:50%;" />



### 树转二叉树：

**思路**
大体就两步，很好理解，如图是用来举栗的多叉树：

<img src="https://img-blog.csdn.net/20170410133259616?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvQzIwMTkwMTAy/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast" alt="img" style="zoom:67%;" />

**兄弟连**
将所有的兄弟间连一条线，如图：

<img src="https://img-blog.csdn.net/20170410133447858?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvQzIwMTkwMTAy/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast" alt="img" style="zoom:67%;" />

**右子断**
将所有右儿子与父亲的边删掉，如图：

<img src="https://img-blog.csdn.net/20170410133913920?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvQzIwMTkwMTAy/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast" alt="img" style="zoom:67%;" />

其他
事实上这已经是一棵二叉树了，还有一点小细节。

**调整层次**

<img src="https://img-blog.csdn.net/20170410134402209?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvQzIwMTkwMTAy/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast" alt="这里写图片描述" style="zoom:67%;" />

很容易发现，“兄弟”（即黄色线相连的结点）都在它们的大哥右子树中，且根结点一定没有右儿子（因为根结点没有兄弟）。

**森林的处理**
有的坑爹题目，转为二叉树后有多个结点的父亲都为0（即为根结点），如图：

<img src="https://img-blog.csdn.net/20170410135613646?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvQzIwMTkwMTAy/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast" alt="这里写图片描述" style="zoom:67%;" />

（原谅我直接copy的第一棵树，不过没影响）解决这个很容易，从右到左依次将根结点接到它前一个根结点的右儿子上即可：

<img src="https://img-blog.csdn.net/20170410140112700?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvQzIwMTkwMTAy/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast" alt="这里写图片描述" style="zoom:67%;" />

**实现**
连接兄弟&切断右儿子
这里介绍最好理解的方法：
输入一对关系，如x,y（表示y为x的儿子）
判断：x有没有左儿子
没有：y直接成为x的左儿子；
有：设x的左儿子为x.l，右儿子为x.r，就找到x.l的右儿子的右儿子的右儿子……
为什么不用切断右儿子？因为根本就还没有连接右儿子！
如图：

<img src="https://img-blog.csdn.net/20170407140220788?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvQzIwMTkwMTAy/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center" alt="这里写图片描述" style="zoom:67%;" />


就这样。（这么简单？！）



### 二叉树的实现：



#### **a、二叉树的抽像数据类型定义：**

```c
ADT BinaryTree
{
	数据对象D：D是具有相同特性的数据元素的集合。
    数据关系R：若D=∅，则R=∅;
			 若D≠中，则R=};H是如下二元关系:
			  ①root唯一		//关于根的说明
              ②D(j)nD(k)=∅	 //关于子树不相交的说明
			  ③...			 //关于数据元素的说明
			  ④....			 //关于左子树和右子树的说明
	基本操作P:
}ADT BinaryTree;

```



#### **b、二叉树的操作：**

**CreateBiTree(&T,definition)**
初始条件;definition给出二叉树T的定义。                                           操作结果:按definition构造二叉树T。

**PreOrderTraverse(T)**
初始条件:二叉树T存在。
操作结果:先序遍历T，对每个结点访问一次。

**lnOrderTraverse(T)**
初始条件:二叉树T存在。
操作结果:中序遍历T，对每个结点访问一次。

**PostOrderTraverse(T)**
初始条件:二叉树T存在。
操作结果:后序遍历T，对每个结点访问一次。



#### c、二叉树的性质和存储结构

##### （1）性质：

**性质1：**在二叉树的第 i 层上**至多**有 2^(i-1) 个结点 (i>=1)。

**性质2：**深度为 k 的二叉树至多有 2^k - 1 个结点 (k ≥1)。

**性质3：**对任何一棵二叉树T，如果其叶子数为no，度为2的结点数为n₂，则no= n₂ + 1。

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230421110216316.png" alt="image-20230421110216316" style="zoom:50%;" />



**两种特殊的二叉树：**

注：在他们的顺序存储方式下可以复原。



**（1）、满二叉树**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230427192051624.png" alt="image-20230427192051624" style="zoom:50%;" />

​	**定义：**一棵深度为k且有2k-1个结点的二叉树称为满二叉树。

​	**特点：**1、每一层上的结点数都是最大结点数（即每层都满)。

​			    *2、叶子节点全部在最底层*

​	

​	**对满二叉树结点位置进行编号**
​	编号规则：从根结点开始，自上而下，自左而右。
​				   	每一结点位置都有元素。



**（2）、完全二叉树**

**定义：**深度为k的具有n个结点的二叉树，当且仅当其每一个结点都与深度为 k 的**满二叉树**中**编号**为1~n的结点一一 对应时，称之为完全二叉树。

**列如：**

![image-20230421112625892](C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230421112625892.png)



**注：在满二叉树中，从最后一个结点开始，连续去掉任意个连续的结点，即是一棵完全二叉树。**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230421113217017.png" alt="image-20230421113217017" style="zoom:50%;" />



**特点:**

1、叶子只可能分布在层次最大的两层上。

2、对任一结点，如果其右子树的最大层次为 i ，则其左子树的最大层次必为 i 或 i+1。

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230427192521733.png" alt="image-20230427192521733" style="zoom: 50%;" />





**性质4、具有n个结点的完全二叉树的深度为「log₂ⁿ」 + 1。**
	  **注:「x」:称作x的底，表示不大于x的最大整数**

**性质5、如果对一棵有n个结点的完全二叉树（深度为「log₂ⁿ」 + 1）的结点按层序编号（从第1层到第「log₂ⁿ」 + 1层，每层从左到右），则对任一结点i(1≤i≤n)，有:**
（1）如果 i=1，则结点 i 是二叉树的根，无双亲;如果 i>1，则其双亲是结点 「i / 2」。
（2）如果 2i> n，则结点 i 为叶子结点，无左孩子；否则，
其左孩子是结点 2i。
（3）如果 2i+1 > n，则结点i无右孩子;否则，其右孩
子是结点 2i + 1。

**性质5表明了完全二叉树中双亲结点编号与孩子结点编号之间的关系**



##### （2）存储



**顺序存储：**

**实现：按满二叉树的结点层次编号，依次存放二叉树中的数据元素。**

**例1：**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230427203128939.png" alt="image-20230427203128939" style="zoom:50%;" />



```c
//二叉树顺序存储表示结构
#define MAX 100
//TElemType:元素类型（如：int，char等）
typedef TElemType SqBiTree[MAX] SqBiTree;
SqBiTree bt;
```



**例2：**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230427195740158.png" alt="image-20230427195740158" style="zoom:67%;" />

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230427195827522.png" alt="image-20230427195827522" style="zoom: 50%;" />

**二叉树的顺序存储的缺点：**

最坏情况：深度为k的且只有n个结点的单支树需要长度为2ⁿ-1的一维数组。

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230427200400254.png" alt="image-20230427200400254" style="zoom:50%;" />

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230427200411905.png" alt="image-20230427200411905" style="zoom:50%;" />

特点:
结点间关系蕴含在其存储位置中
浪费空间，适于存**满二叉树**和**完全二叉树**



**二叉树的链式存储结构：**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230427200908644.png" alt="image-20230427200908644" style="zoom:50%;" />

data：数据元素

lchild：指针，指向左孩子。

rchild：指针，指向右孩子。

```c++
//嵌套定义
typedef struct BiNode
{
    TElemType data;
    //左右孩子指针
    struct BiNode *lchild,*rchild;
}BiNode,*BiTree;
```



二叉树的链式存储结构：

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230427201533450.png" alt="image-20230427201533450" style="zoom: 80%;" />



在n个结点的二叉链表中，有**n+1**个空指针域

分析：必有2n个链域。除根结点外每个结点有且仅有一个双亲，所以只会有n - 1个结点的链域存放指针,指向非空子女结点。

**空指针数目 = 2n - (n-1) = n + 1**



**三叉链表：**

![image-20230427202623011](C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230427202623011.png)





#### d、二叉树的遍历和线索二叉树



**遍历定义：顺着某一条搜索路径巡访二叉树中的结点，使得每个结点均被访问一次，而且仅被访问一次（又称周游)。**                              “访问”的含义很广，可以是对结点作各种处理，如:输出结点的信息、修改结点的数据值等，但要求这种访问不破坏原来的数据结构。

**遍历目的：**得到树中所有结点的一个线性排列。

**遍历用途：**它是树结构插入、删除、修改、查找和排序运算的前提，是二叉树一切运算的基础和核心。

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230427203925013.png" alt="image-20230427203925013" style="zoom:50%;" />

依次遍历二叉树中的三个组成部分，便是遍历了整个二叉树

假设：L：遍历左子树	D：访问根结点	R：遍历右子树

则遍历整个二叉树方案共有:

DLR、LDR、LRD、 DRL、RDL、RLD 六种。



<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230427204505632.png" alt="image-20230427204505632" style="zoom: 50%;" />

若规定先左后右，则只有前三种情况：

**注：遍历时是按照以下三种遍历顺序划分树，每划分一次树后只看划分的树的结点，当划分的某棵树的一方（L、R、D）遍历完时才可以按照遍历方式进行后一遍历步骤。**

DLR——先（根）序遍历，LDR——中（根）序遍历，
LRD——后（根）序遍历。

**例如：**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230429121523352.png" alt="image-20230429121523352" style="zoom:50%;" />



**二叉树性质：**

①若二叉树中各结点的值均不相同，则二叉树结点的先序序列、中的予列和后序列都是唯一的。
②由二叉树的先序序列和中序序列，或由二叉树的后序序列和中序序列可以确定唯一—棵二叉树。

 

**例如：**

已知二叉树的先序和中序序列，构造出相应的二叉树

先序：ABCDEFGHIJ
中序：CDBFEAlHGJ

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230429121833963.png" alt="image-20230429121833963" style="zoom:50%;" />



实例分析:已知一棵二叉树的

中序序列:BDCEAFHG
后序序列: DECBHGFA，请画出这棵二叉树。

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230429123142967.png" alt="image-20230429123142967" style="zoom: 67%;" />





##### **（1）遍历算法实现**

```c
//嵌套定义
typedef struct BiNode
{
    TElemType data;
    //左右孩子指针
    struct BiNode *lchild,*rchild;
}BiNode,*BiTree;
```



**先序遍历：**

![image-20230429124018649](C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230429124018649.png)



```c
Status PreOrderTraverse(BiTree T)//先序
{
    //如果二叉树为空
    if(T==NULL)return OK;
    else
    {
        visit(T);	//访问根节点
        PreOrderTraverse(T->lchild);//递归遍历左子树
        PreOrderTraverse(T->rchild);//递归遍历右子树
    }
}
```

**例如：**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230505185442527.png" alt="image-20230505185442527" style="zoom: 67%;" />



**中序遍历：**

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230429131212535.png" alt="image-20230429131212535" style="zoom:67%;" />



```c
Status lnOrderTraverse(BiTree T)//中序
{
	if(T==NULL) return OK;//空二叉树
    else
    {
		InOrderTraverse(T->lchild);//递归遍历左子树
        visit(T);//访问根结点
        InOrderTraverse(T->rchild);//递归遍历右子树
    }
}
```



**后序遍历：**

![image-20230505190930942](C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230505190930942.png)



```c
Status PostOrderTraverse(BiTree T)//后序
{
    if(T==NULL) return OK;//空二叉树
    else
    {
		InOrderTraverse(T->lchild);//递归遍历左子树
        InOrderTraverse(T->rchild);//递归遍历右子树
        visit(T);//访问根结点
    }
}
```



**总结：**

如果去掉输出语句，从递归的角度看，三种算法是完全相同的，或说这**三种算法的访问路径是相同的，只是访问结点的时机不同**。

从虚线的出发点到终点的路径上，每个结点经过3次。

第1次经过时访问=先序遍历

第2次经过时访问=中序遍历

第3次经过时访问=后序遍历

路径：

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230505191652061.png" alt="image-20230505191652061" style="zoom:50%;" />



##### （2）非递归算法（栈实现）

二叉树中序遍历的非递归算法的关键:在中序遍历过某结点的整个左1子树后，如何找到该结点的根以及右子树。

**以中序遍历为例：**
基本思想:
①建立一个栈
②根结点进栈，遍历左子树
③根结点出栈，输出根结点，遍历右子树。

```c
Status InOrderTraverse (BiTree T) 
{
    //创建栈S
    InitStack(S);
    BiTree p; p=T;
    //p为空or栈空,循环结束
	while(p != NULL || !StackEmpty(S)) 
	{
		if(p != NULL)
    	{ 
        	Push(S,p);
        	p = p->lchild;
    	}
		else 
		{ 
            //弹出栈顶元素赋值给q
    		Pop(S,q);
            printf("%c"，q->data);
			p = q->rchild; 
		}//while
	}
	return OK;
}
```



##### （3）二叉树的层次遍历（队列实现）

<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230505195047707.png" alt="image-20230505195047707" style="zoom: 67%;" />

对于一颗二叉树，从根结点开始，按**从上到下**、**从左到右**的顺序访问每一个结点。
每一个结点仅仅访问一次。



**算法设计思路：使用队列**

（1）将根结点进队;
（2）队不空时循环：从队列中出列一个结点*p，访问它;
①若它有左孩子结点，将左孩子结点进队;
②若它有右孩子结点，将右孩子结点进队。



**队列类型定义：**

```c
typedef struct
{
	BTNode data[MaxSize];	//存放队中元素
    int front,rear;	//队头和队尾指针
} SqQueue;	//顺序循环队列类型
```



**二叉树的层次遍历算法：**

```c
void LevelOrder(BTNode *b)
{
    BTNode *p; SqQueue *qu;
    InitQueue(qu);	//初始化队列
    enQueue(qu,b);	//根节点指针b入队
    while(!QueueEmpty(qu))	//队列不为空，则循环
    {
        deQueue(qu,p);	//队头出队赋值给指针p
        printf("%c",p->data);	//访问结点p
        //有左孩子将其入队
        if(p->lchild != NULL) enQueue(qu,p->lchild);
        //有右孩子将其入队
        if(p->rchild != NULL) enQueue(qu,p->rchild);
    }
}
```



##### （4）二叉树建立

按先序遍历序列建立二叉树的二叉链表

例:已知先序序列为:
ABCQEGF
（1）从键盘输入二叉树的结点信息，建立二叉树的存储结构;

（2）在建立二叉树的过程中按照二叉树先序方式建立;

可以得到：<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230505202302800.png" alt="image-20230505202302800" style="zoom: 67%;" />

**由于树的形状不唯一，故补上空节点即可。**

ABC##DE#G##F###（以#代表空节点）

得到：<img src="C:\Users\anscy\AppData\Roaming\Typora\typora-user-images\image-20230505202505812.png" alt="image-20230505202505812" style="zoom: 67%;" />



**算法实现：**

```c
//嵌套定义
typedef struct BiNode
{
    TElemType data;
    //左右孩子指针
    struct BiNode *lchild,*rchild;
}BiNode,*BiTree;
```

**先序建立：**

```c
Status CreateBiTree(BiTree &T)
{
    char ch = 0;
    scanf("%c",&ch); //cin >> ch;
	if (ch == "#")
        T = NULL;
    else 
    {
        //if空间开辟失败
		if (!(T = (BiTNode*)malloc(sizeof(BiTNode))))
            exit(OVERFLOW);//T=new BiTNode;
		T->data = ch;	//生成根结点
        
		CreateBiTree(T->lchild);	//构造左子树
        CreateBiTree(T->rchild);	//构造右子树
    }
	return OK;
}// CreateBiTree
```



##### （5）复制二叉树

**算法思想：**（以先序为例）

如果是空树，递归结束;
否则，申请新结点空间，复制根结点

》递归复制左子树

》递归复制右子树

```c
int TreeCopy(BiTree T， BiTree &NewT)
{
	if(T==NULL)//如果是空树返回0
    {
        NewT = NULL;
        return 0;
    }
	else 
	{
		NewT=new BiTNode;
        NewT->data=T->data;
        TreeCopy(T->lchild, NewT->lchild);
		TreeCopy(T->rchild, NewT->rchild);
	}
}
```

