## 冒泡排序
```c++
void Bubble_sort(vector<int> &arr, int n){
    for (int i = 0; i < n - 1; i++){
        bool flag = false;
        for (int j = n - 1; j > i; j--){
            if (arr[j - 1] > arr[j]){
                swap(arr[j - 1], arr[j]);
                flag = true;
            }
        }
        if (flag == false)  // 减少不必要的比较
            return;
    }
}
```