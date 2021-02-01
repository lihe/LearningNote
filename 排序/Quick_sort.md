## 快速排序
```c++
void quicksort(vector<int> &arr, int left, int right){
    if (left < right) {
        int pos = _partation(arr, left, right);
        quicksort(arr, left, pos - 1);
        quicksort(arr, pos + 1, right);
    }
}

int _partation(vector<int> &arr, int l, int r) {
    int pivot = arr[l];

    while (l < r){
        while (l < r && pivot <= arr[r])
            r--;
        arr[l] = arr[r];
        while (l < r && arr[l] <= pivot)
            l++;
        arr[r] = arr[l];
    }
    arr[l] = pivot;
    return l;
}
```

