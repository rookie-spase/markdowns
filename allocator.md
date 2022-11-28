这一章将介绍SGI 的 allocator是怎么运行的  
## GNU 的allocator分为2级  
>- 第一级单纯的调用malloc  
>- 第二级则会搭配链表来管理内存  
> > 当分配的内存大于等于128B的时候调用第一级allocator,小于128B时候调用第二级allocator、
---
# 第一级分配器
这个分配器就是简单的将malloc包装了一下
