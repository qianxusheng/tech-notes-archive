# Data Structure

## Abstract data structure (design behavior)
- **Stack**：LIFO，出栈入栈，访问栈顶 `peek()`，判断是否为空  
- **Queue**：FIFO，出队入队，查看队首元素 `front()`，判断是否为空  
- **Deque**：stack+queue 的操作  
- **List**：`insert`，`delete`，`get(index)`，`size`，`is_empty`  
- **Set**：`add`，`remove`，`contains`，集合运算操作  
- **Map**：`put`，`get`，`remove`，`contains`  
- **PQ**：`insert(x, priority)`，`peek()` 最高优先级  
- **Tree**：`insert`，`delete`，`search`，`traverse`  
- **Graph**：插入删除点，插入删除边，访问邻居节点，`hasPath()`  
- **Array**：基础，一般语言内置

## Data structure (implementation)
- **Stack**：数组  
- **Queue**：数组  
- **Deque**：数组（分段连续数组）  
- **List**：节点+指针（链表，链式结构）  
- **Set**：哈希表（通过哈希表映射到数组上），红黑树  
- **Map**：哈希表（通过哈希表映射到数组上），红黑树  
- **PQ**：最小堆  
- **Tree**：节点+指针（链表，链式结构）  
- **Graph**：二维数组或哈希表+数组（邻接表，邻接矩阵）  
- **Array**：连续内存块  
