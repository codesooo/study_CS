# 레퍼런스
변수나 상수를 가리키는 방법

### 예시
```cpp
int a = 3;
int& another_a = a; // a의 별명

another_a = 5;
std::cout << "a : " << a << "\n"; // [출력] a : 5
std::cout << "another_a : " << another_a << "\n"; // [출력] another_a : 5
```


