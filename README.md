## 数据结构排序算法——内部排序
### 摘要
> 排序是计算机程序设计中的一种重要操作，其功能是对一个数据元素集合或序列重新排列成一个按数据元素某个相知有序的序列。排序分为两类：外排序和内排序。外部排序指的是大文件的排序，即待排序的记录存储在外存储器上，待排序的文件无法一次装入内存，需要在内存和外部存储器之间进行多次数据交换，以达到排序整个文件的目的。内部排序是指待排序列完全存放在内存中所进行的排序过程，适合不太大的元素序列。其中快速排序的是目前排序方法中被认为是最好的方法。
-  内部排序方法：
1. 插入排序—直接插入排序；
2. 插入排序—希尔排序；
3. 选择排序—简单选择排序；
4. 选择排序—堆排序；
5. 交换排序—冒泡排序；
6. 交换排序—快速排序；
7. 归并排序；
8. 桶排序/基数排序
####
![内部排序](https://upload-images.jianshu.io/upload_images/2077144-aacd6a8212ec156d.jpg)

### 1.插入排序—直接插入排序(Straight Insertion Sort)
- 基本思想：每一趟将一个待排序的记录，按其关键字的大小插入到已经排好序的一组记录的适当位置上，直到所有待排序记录全部插入为止。
- 时间复杂度为 O(n^2)，特别情况下， 当所要排序的数据是有序的情况下，时间复杂度变为更好的O(n);
- 空间复杂度：O（1）；
- 稳定性：稳定
- C语言代码实现：
####
![直接插入](https://upload-images.jianshu.io/upload_images/2077144-07154377c7ef3e84.PNG)

### 2. 插入排序—希尔排序（Shell`s Sort）
- 基本思想：先将整个待排序记录序列分割成若干个子序列分别进行直接插入排序，待整个序列中的记录“基本有序”时，再对全体记录进行依次直接插入排序。
【注】分割子序列是通过增量因子进行分割的，增量因子选取时，应注意它除了1外没有公因子，且最后一个增量因子必为1。
####
![希尔](https://upload-images.jianshu.io/upload_images/2077144-5d740374bdf12582.jpg)
- 时间复杂度：O（n^1.3）---O(n^1.5)
- 空间复杂度：O（1）
- 稳定性：不稳定
- C语言代码实现
####
![希尔排序](https://upload-images.jianshu.io/upload_images/2077144-d7f595f0877ebe51.PNG)

### 3. 选择排序—简单选择排序（Simple Selection Sort）
- 基本思想：在要排序的一组数中，选出最小（或者最大）的一个数与第一个位置的数进行交换，然后在剩下的数中再找最小（或者最大）的与第二个位置的数交换，依次类推，直至第n-1个元素（倒数第二个数）与第n个元素(最后一个数)比较为止。【注】第一趟，从n个记录中选出关键码最小的记录与第一个记录进行交换；第二趟，从第二个记录开始的n-1个记录里选出关键码最小的记录与第二个记录进行交换；.......第i趟，从第i个记录开始的n-i+1个记录中选出关键码最小的记录与第i个记录进行交换。
- 时间复杂度：O（n^2）
- 空间复杂度：O（1）
- 稳定性：不稳定
- C语言代码实现
####
![](https://upload-images.jianshu.io/upload_images/2077144-97adb0437cb0bb63.PNG)

### 4. 选择排序—堆排序（Heap Sort）
- 基本思想：首先需要建立大根堆（父>子）或者小根堆（父<子），这样就得到了最大值或者最小值（即堆顶元素），此时将堆顶元素与堆中最后一个元素进行交换，再对最后一个元素除外的所有元素进行大根堆或者小根堆的重新调整。这样直到所有元素都调整完毕，就得到了一个有序序列的记录。
【注】
1.父-->子：n-->2*n+1 ,2*n+2 ;子-->父：n-->(n-1)/2
2.构造大根堆（小根堆）：第一次构造大根堆（小根堆），需要从最后一颗子树开始，从后往前多次调整，每次调整的过程是从上往下。
- 时间复杂度：O（nlog2^n）(log以2为底n的对数)（注：一次堆调整的时间复杂度是O（log2^n））
- 空间复杂度：O（1）
- 稳定性：不稳定
- C语言代码实现：
####
![](https://upload-images.jianshu.io/upload_images/2077144-1f9f26963b67ec88.PNG)
![](https://upload-images.jianshu.io/upload_images/2077144-ecd81407e1740188.PNG)

### 5. 交换排序—冒泡排序（Bubble Sort）
- 基本思想：在要排序的一组数中，自上而下的对相邻的两个数依次进行比较和调整，较大的数往下沉，较小的数往上冒。
- 时间复杂度：O（n^2）
- 空间复杂度：O（1）
- 稳定性：稳定
- C语言代码实现：
 ####
 ![](https://www.jianshu.com/p/3da04f989d00)

 ### 6. 交换排序—快速排序（Quick Sort）
- 基本思想：
1.选择一个基准元素,通常选择第一个元素或者最后一个元素,
2.通过一趟排序讲待排序的记录分割成独立的两部分，其中一部分记录的元素值均比基准元素值小。另一部分记录的 元素值比基准值大。
3.此时基准元素在其排好序后的正确位置
4.然后分别对这两部分记录用同样的方法继续进行排序，直到整个序列有序。•时间复杂度：O（nlog2^n）快速排序数据越有序，时间复杂度越大，性能越不好。
####
![](https://upload-images.jianshu.io/upload_images/2077144-e6fddeb29cbeae9a.jpg)
![](https://upload-images.jianshu.io/upload_images/2077144-2a1063ef6b6e61ae.jpg)
- 空间复杂度：O（log2^n）
- 稳定性：不稳定
- C语言代码实现：
####
![](https://upload-images.jianshu.io/upload_images/2077144-e610d27d04d50a8a.PNG)

### 7. 归并排序（Merge Sort）
- 基本思想：将两个（或者两个以上）的有序表合并成一个新的有序表，即把待排序序列分为若干个子序列，每个子序列都是有序的。然后再把有序子序列合并为整体有序序列。
####
![](https://upload-images.jianshu.io/upload_images/2077144-142c6fe3cc7df2ad.jpg)
- 时间复杂度：O（nlog2^n）
- 空间复杂度：O（n）
- 稳定性：稳定
- C语言代码实现：
####
![](https://upload-images.jianshu.io/upload_images/2077144-6c60ca8a6a985ffc.PNG)
![](https://upload-images.jianshu.io/upload_images/2077144-038df22e7facd4b3.PNG)
![](https://upload-images.jianshu.io/upload_images/2077144-7f33f1597dd79792.PNG)

### 8. 桶排序/基数排序(Radix Sort)
- 基本思想：低位优先，链式队列。将数字按位数划分出n个关键字，每次针对一个关键字进行排序，然后针对排序后的序列进行下个关键字的排序，循环至所有关键字都是用过，则排序完成。
- 时间复杂度：O（d*n）d代表数字的个数，n代表要排序的数的总数
- 空间复杂度：O（n）
- 稳定性：稳定

### 总结
![](https://upload-images.jianshu.io/upload_images/2077144-9785539c2b812eb4.jpg)



