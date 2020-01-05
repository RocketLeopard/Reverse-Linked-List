# Reverse-Linked-List（反转链表）
反转一个单链表。

## Sampple
输入: 1->2->3->4->5->NULL  
输出: 5->4->3->2->1->NULL  

## Solution
方法一：迭代
初始化的时候，curr指针指向当前节点，prev指针指向当前节点的前一个节点。在遍历列表时，将curr的next指针改为指向前驱节点的prev指针。在更改引用之前，还需要另一个指针来存储curr的next。curr不断迭代，将curr指针的next指向prev之后再将curr指针赋值给prev，等于想prev链表从表头插入元素。  

方法二：递归
其实就是使用栈帧来存储当前节点和后驱节点的指针。通过递归方法返回，也就是弹栈来实现单项链表的反向遍历。反向遍历过程中不断的把当前节点的next的next指向自己，然后再将next指向null，最后返回递归最底层的节点指针。  

## 复杂度分析
方法一：迭代
时间复杂度：O(N)，n是列表的长度。    
空间复杂度：O(1)。  

方法二：递归
时间复杂度：O(N)，n是列表的长度。  
空间复杂度：O(N)，由于使用递归，将会使用隐式栈空间。递归深度可能会达到n层。

## 备注
链接：https://leetcode-cn.com/problems/reverse-linked-list/solution/fan-zhuan-lian-biao-by-leetcode/
来源：力扣（LeetCode）
