# Popular interview questions for campus placements

## 1) Count frequency of each element in an array

```cpp 
void frequencyCount(vector<int>& arr){
    map<int, int> mpp;
    for(auto i:arr){
        mpp[i]++;
    }
    for(auto i: mpp){
        cout<<i.first<<" "<<i.second<<endl;
    }
}
```

## 2) Find the median of a given array

### Python
```python 
from statistics import median

arr1 = [3, 1, 4, 1, 5]

print("Median of arr1:", median(arr1))

```
### Cpp
```cpp 
double find_median(vector<int>& arr) {
    if (arr.empty()) {
        throw std::runtime_error("Array is empty");
    }
    // Sort the array
    std::sort(arr.begin(), arr.end());
    int n = arr.size();

    // If length is odd, return middle element
    if (n % 2 != 0) {
        return arr[n / 2];
    }

    // If length is even, return average of two middle elements
    return (arr[(n / 2) - 1] + arr[n / 2]) / 2.0;
}

```

## 3) Frequency of each element in an array

```cpp 
void frequencyOfEachElement(vector<int> &arr)
{
    vector<int> v;
    v.push_back(arr[0]);
    int n = arr.size();
    for (int i=1; i<n; i++)
    {
        if(v.back() != arr[i]) v.push_back(arr[i]);
    }
    for(auto i:v){
        cout<<i<<endl;
    }
}
```
## 4) Find all the repeting elements in the array

```cpp 
void repetingElement(vector<int> &arr)
{
    map<int, int> mpp;
    for(auto i: arr){
        mpp[i]++;
    }

    for(auto i:mpp) 
        if(mpp[i.second] > 1) cout<<i.first;
}
```
## 5) Find all the non-repeting elements in the array

```cpp 
void nonRepetingElement(vector<int> &arr)
{
    map<int, int> mpp;
    for(auto i: arr){
        mpp[i]++;
    }

    for(auto i:mpp) 
        if(mpp[i.second] == 1) cout<<i.first;
}
```