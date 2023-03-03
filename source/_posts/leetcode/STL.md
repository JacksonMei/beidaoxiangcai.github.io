## Sort

```c++
// lambda 
sort(s.begin(), s.end(), [&](const char &iter1, const char &iter2) {
    return iter1 > iter2;
});


// operator() 
struct IntCompareClass{
	bool operator()(const char& elem1, const char& elem2){
		return elem1 > elem2;
	}
} IntObjectCom;
sort(s.begin(), s.end(), IntObjectCom);
```



## String

```c++
islower/isupper
isalpha
isdigit 是否是十进制数字
isalnum 是否数字或字母
```

