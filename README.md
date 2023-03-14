Data-Structure-Sequence_Stack
Declaration Implementation and use of Sequence_Stack

栈作为一种数据结构，是一种只能在一端进行插入和删除操作的特殊线性表。
它按照后进先出的原则存储数据，先进入的数据被压入栈底，最后的数据在栈顶，需要读数据的时候从栈顶开始弹出数据（最后一个数据被第一个读出来）。
栈具有记忆作用，对栈的插入与删除操作中，不需要改变栈底指针。
栈是允许在同一端进行插入和删除操作的特殊线性表。
允许进行插入和删除操作的一端称为栈顶(top)，另一端为栈底(bottom)；栈底固定，而栈顶浮动；栈中元素个数为零时称为空栈。
插入一般称为进栈（PUSH），删除则称为退栈（POP）。栈也可以称为：先进后出表。

----------------------------------------------------------------------------------------------------------------------------------
一个栈的组成结构如下所示：
----------------------------------------------------------------------------------------------------------------------------------
typedef double Element_Type; /*栈内的元素为 double类型*/

typedef struct Sequence_Stack /*栈的存储结构*/
{
    Element_Type data[MAX_SIZE]; /*栈数据*/
    int top_index;               /*栈顶下标索引*/
} _Sq_Stack_;

为了完成栈的各种操作需要声明并实现以下几个函数：
----------------------------------------------------------------------------------------------------------------------------------
/*功能 01）初始化栈*/
bool Init_Stack(_Sq_Stack_ *new_stack);

/*功能 02）获得栈的长度*/
int Get_Stack_Length(_Sq_Stack_ stack);

/*功能 03）判断栈是否为空*/
bool Empty_Stack(_Sq_Stack_ stack);

/*功能 04）入栈*/
bool Push_Stack(_Sq_Stack_ *stack, Element_Type *data);

/*功能 05）出栈*/
bool Pop_Stack(_Sq_Stack_ *stack, Element_Type *data);

/*功能 06）获取栈顶元素（不出栈）*/
bool Get_Top_Element(_Sq_Stack_ stack, Element_Type *data);

/*功能 07）遍历并输出栈的所有元素*/
bool Print_Stack_Element(_Sq_Stack_ stack);

/*功能 08）清空栈*/
bool Clear_Stack(_Sq_Stack_ *stack);

----------------------------------------------------------------------------------------------------------------------------------
鄙人目前正在复习数据结构，以后会经常再Github.com上更新，如有问题请各位指出，Thanks!!
Date:2023.3.14 Author:JesseZ332623
