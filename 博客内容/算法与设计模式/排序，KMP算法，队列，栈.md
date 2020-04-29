# 排序 

## 1. 基本的排序算法

### 冒泡排序
```c++
void sort(int[] nums) {
    //定义一个布尔变量 hasChange，用来标记每轮遍历中是否发生了交换
    boolean hasChange = true; 
    //每轮遍历开始，将 hasChange 设置为 false
    for (int i = 0; i < nums.length - 1 && hasChange; i++) {
        hasChange = false;

        //进行两两比较，如果发现当前的数比下一个数还大，那么就交换这两个数，同时记录一下有交换发生
        for (int j = 0; j < nums.length - 1 - i; j++) {
            if (nums[j] > nums[j + 1]) {
                swap(nums, j, j + 1);
                hasChange = true;
            }      
        }
     }
 }
```

### 插入排序（Insertion Sort）

```c++
void sort(int[] nums) {
    // 将数组的第一个元素当作已经排好序的，从第二个元素，即 i 从 1 开始遍历数组
    for (int i = 1, j, current; i < nums.length; i++) {
        // 外围循环开始，把当前 i 指向的值用 current 保存
        current = nums[i];

        // 指针 j 内循环，和 current 值比较，若 j 所指向的值比 current 值大，则该数右移一位
        for (j = i - 1; j >= 0 && nums[j] > current; j--) {
            nums[j + 1] = nums[j];
        }
    
        // 内循环结束，j+1 所指向的位置就是 current 值插入的位置
        nums[j + 1] = current;
    }
}
```

## 2. 排序算法





# KMP




# 队列 栈