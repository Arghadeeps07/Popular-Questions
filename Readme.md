# **Popular Interview Questions for Campus Placements**

## **Array**

### **1) Count Frequency of Each Element in an Array**

```cpp
void frequencyCount(vector<int>& arr) {
    map<int, int> mpp;
    for (auto i : arr) {
        mpp[i]++;
    }
    for (auto i : mpp) {
        cout << i.first << " " << i.second << endl;
    }
}
```

### **2) Find the Median of a Given Array**

#### **Python**

```python
from statistics import median

arr1 = [3, 1, 4, 1, 5]
print("Median of arr1:", median(arr1))
```

#### **C++**

```cpp
double find_median(vector<int>& arr) {
    sort(arr.begin(), arr.end());
    int n = arr.size();

    if (n % 2 != 0) {
        return arr[n / 2];
    }

    return (arr[(n / 2) - 1] + arr[n / 2]) / 2.0;
}
```

### **3) Find All Repeating Elements in an Array**

```cpp
void repeatingElements(vector<int>& arr) {
    map<int, int> mpp;
    for (auto i : arr) {
        mpp[i]++;
    }

    for (auto i : mpp) {
        if (i.second > 1) {
            cout << i.first << " ";
        }
    }
}
```

### **4) Find All Non-Repeating Elements in an Array**

```cpp
void nonRepeatingElements(vector<int>& arr) {
    map<int, int> mpp;
    for (auto i : arr) {
        mpp[i]++;
    }

    for (auto i : mpp) {
        if (i.second == 1) {
            cout << i.first << " ";
        }
    }
}
```

### **5) Check if a Year is a Leap Year**

```cpp
bool isLeapYear(int year) {
    if (year % 400 == 0) {
        return true;
    } else if (year % 100 == 0) {
        return false;
    } else if (year % 4 == 0) {
        return true;
    } else {
        return false;
    }
}
```

### **6) Arrange in Increasing-Decreasing Order**

**Example:**

```
Input: 8 7 1 6 5 9
Output: 1 5 6 9 8 7
```

```cpp
void increasingDecreasing(vector<int>& arr) {
    int n = arr.size();
    sort(arr.begin(), arr.end());
    reverse(arr.begin() + n / 2, arr.end());
    for (int i : arr) {
        cout << i << " ";
    }
}
```

### **7) Find Primes in a Given Range**

```cpp
vector<int> getPrimesInRange(int start, int end) {
    vector<int> primes;
    if (start < 2) start = 2;
    for (int num = start; num <= end; ++num) {
        bool isPrime = true;
        for (int i = 2; i * i <= num; ++i) {
            if (num % i == 0) {
                isPrime = false;
                break;
            }
        }
        if (isPrime) {
            primes.push_back(num);
        }
    }
    return primes;
}
```

### **8) Remove elements**

```
Example 1:

Input: nums = [3,2,2,3], val = 3
Output: 2, nums = [2,2,_,_]
Explanation: Your function should return k = 2, with the first two elements of nums being 2.
It does not matter what you leave beyond the returned k (hence they are underscores).
```

```cpp
int removeElement(vector<int>& arr, int val) {
    int k =0;
    int n= arr.size();
    for(int i=0; i<n; i++){
        if(arr[i] != val){
            arr[k] = arr[i];
            k++;
        }
    }
    return k;
}
```


### **9) Remove duplicates from unsorted array**

```cpp
int main(){
  int arr[] = {1,1,2,3,4,4};
  set<int> st;
  for(auto i:arr){
    st.insert(i);
  }
  int ans[st.size()];
  copy(st.begin(),st.end(),ans);
  for(auto i:ans){
    cout<<i<<" ";
  }
  
  return 0;
}
```



## **String**

### **1) Remove Spaces from a String**

```cpp
string removeSpaces(string str) {
    str.erase(remove(str.begin(), str.end(), ' '), str.end());
    return str;
}
```

### **2) Sum of Numbers Present in a String**

```cpp
int sumOfNumbersInString(string str) {
    int sum = 0;
    for (char i : str) {
        if (isdigit(i)) {
            sum += i - '0';
        }
    }
    return sum;
}
```
### **3) Length of Last Word using stl**

```cpp
int lengthOfLastWord(string s) {
    int index = s.find_last_not_of(' ')+1;
    s.erase(index);
    int lastSpaceIndex = s.find_last_of(' ');
    return lastSpaceIndex == string::npos ? s.length() : s.size() - lastSpaceIndex-1;
}
```
### **4) Write a program to find a substring within a string. If found display its starting position**

```cpp
int main(){
  string str = "Arghadeep";
  int position = str.find("rgha");
  cout<<"posioiton of Argha is "<<position<<endl;
  return 0;
}
```
### **5) Change case of each character in a string**

```cpp
int main(){
  string str = "Arghadeep";
  for(int i=0; i<str.size(); i++){
    if(isupper(str[i])) str[i] = tolower(str[i]);
    else str[i] = toupper(str[i]);
  }
  cout<<str<<endl;
  return 0;
}
```
### **6) Sort the charecters in a string**

```cpp
int main(){
  string str = "Arghadeep";
  sort(str.begin(),str.end());
  cout<<str<<endl;
  return 0;
}
```


