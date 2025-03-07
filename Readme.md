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



