## 数据结构排序算法——内部排序
### 摘要
> 排序是计算机程序设计中的一种重要操作，其功能是对一个数据元素集合或序列重新排列成一个按数据元素某个相知有序的序列。排序分为两类：外排序和内排序。外部排序指的是大文件的排序，即待排序的记录存储在外存储器上，待排序的文件无法一次装入内存，需要在内存和外部存储器之间进行多次数据交换，以达到排序整个文件的目的。内部排序是指待排序列完全存放在内存中所进行的排序过程，适合不太大的元素序列。其中快速排序的是目前排序方法中被认为是最好的方法。
> 内部排序方法：
1. 插入排序—直接插入排序；
2. 插入排序—希尔排序；
3. 选择排序—简单选择排序；
4. 选择排序—堆排序；
5. 交换排序—冒泡排序；
6. 交换排序—快速排序；
7. 归并排序；
8. 桶排序/基数排序

### 1.插入排序—直接插入排序(Straight Insertion Sort)

- 基本思想：每一趟将一个待排序的记录，按其关键字的大小插入到已经排好序的一组记录的适当位置上，直到所有待排序记录全部插入为止。
- 时间复杂度为 O(n^2)，特别情况下， 当所要排序的数据是有序的情况下，时间复杂度变为更好的O(n);
- 空间复杂度：O（1）；
- 稳定性：稳定
- C语言代码实现：


# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/XW-Queen/Vacation-task/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
