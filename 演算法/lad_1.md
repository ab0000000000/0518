# GenAI_Algorithm_lab1 ==> 二元搜尋樹的各種實作(heap sort)
- `提問詞`:請寫出二元搜尋樹的演算法
- `提問詞`:請計算二元搜尋樹演算法的時間複雜度
- `提問詞`:請用Python寫出二元搜尋樹的演算法
- `提問詞`:請用C寫出二元搜尋樹的演算法
- `提問詞`:請用C++寫出二元搜尋樹的演算法
- `提問詞`:請用JAVA寫出二元搜尋樹的演算法
- `提問詞`:請用Rust寫出二元搜尋樹的演算法
- `提問詞`:請用go寫出二元搜尋樹的演算法
- `提問詞`:請用C#寫出二元搜尋樹的演算法
- `提問詞`:請用Javascript#寫出二元搜尋樹的演算法

## 提問詞:請寫出二元搜尋樹的演算法
以下是堆積排序的基本步驟：

建立最大堆積（Max Heap）或最小堆積（Min Heap）：
如果要將陣列遞增排序，則使用最大堆積；如果要遞減排序，則使用最小堆積。
將要排序的陣列製作成堆積結構，使得每個父節點的值都大於（或小於）其子節點的值。
排序：
交換根節點（最大值或最小值）與最後一個節點。
移除最後一個節點（已排序的部分）。
重新調整堆積，使其滿足堆積性質。
重複以上步驟，直到整個陣列排序完成

# 提問詞:請用Python寫出二元搜尋樹的演算法

def binary_search_recursive(data, low, high, key):
    if low > high:
        return -1
    mid = (low + high) // 2
    if key == data[mid]:
        return mid
    elif key > data[mid]:
        return binary_search_recursive(data, mid + 1, high, key)
    else:
        return binary_search_recursive(data, low, mid - 1, key)

data = [1, 9, 2, 7, 4, 10, 3, 8, 5, 6]
data.sort()
key = 7
print(data)
result = binary_search_recursive(data, 0, len(data) - 1, key)
if result == -1:
    print("找不到")
else:
    print(f"找到索引值 {result}")


![lad_1.md](labs_1_1.png)_

 
