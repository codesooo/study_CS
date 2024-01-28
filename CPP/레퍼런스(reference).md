# 레퍼런스
변수나 상수를 가리키는 방법. 컴파일러에게 별명을 알려주는 것

## 댕글링 레퍼런스(Dangling reference)
본체는 사라지고 별명만 남은 경우

**주의사항**
- 댕글링 레퍼런스 주의 : 레퍼런스를 리턴하는 함수에서 지역변수의 레퍼런수를 리턴하지 않도록 조심하기
- 반드시 처음에 누구의 별명이 될 것인지 지정해야함
  - cf) 포인터는 명시 안해도 가능
- 한번 지은 별명은 다른 이의 별명이 될 수 없다
- 레퍼런스는 메모리 상에 존재하지 않을 수 있다.
  - cf) 물론 존재하는 경우도 있다.
- 레퍼런스의 레퍼런스(별명의 별명) : 불가능(illegal)
- 레퍼런스의 배열 : 불가능(illegal)
  - cf) 배열의 레퍼런스는 가능
- 레퍼런스의 포인터 : 불가능(illegal)

### 예시 : 댕글링 레퍼런스
```cpp
int& function() {
  int a = 2;
  return a;
}

int main() {
  int b = function(); // function()의 return과 동시에 반환값(a의 별명)가 사라짐
  b = 3; // 본체가 사라짐
  return 0;
}
```

### 예시
**레퍼런스**
```cpp
int a = 3;
int b = 1;

// int& antoher_a; // 별명 대상을 명시하지 않으면 안됨
int& another_a = a; // a의 별명임을 명시

int* p; // 누구를 가리킬건지 처음부터 안써도 됨

// another_a = b; // 이미 another_a는 a의 별명이 되었으므로 b의 별명이 될 수 없음
// &another_a = b; // 이것도 안됨(&a = b를 의미하는데, 말이 안되기 때문)

another_a = 5;
std::cout << "a : " << a << std::endl;// [출력] a : 5
std::cout << "another_a : " << another_a << std::endl; // [출력] another_a : 5
```

**상수의 레퍼런스**
```cpp
// int &ref = 4; // 상수 4가 리터럴이라 불가능. ref = 5(4=5)가 불가능하므로

// 상수 참조자는 다음과 같이
const int &ref = 4;
int a = ref; // a=4
```

**배열의 레퍼런스**
```cpp
// 일차원배열
int arr[3] = {1, 2, 3};
int(&ref)[3] = arr; // ref가 arr을 참조

std::cout << arr[0] << arr[1] << arr[2] << std::endl; // [출력] 123
ref[0] = 2; // arr[0] = 2
ref[1] = 3; // arr[1] = 3
ref[2] = 1; // arr[3] = 1
std::cout << arr[0] << arr[1] << arr[2] << std::endl; // [출력] 231

// 이차원배열
int arr2[3][2] = {{1,2,3}, {4,5,6}};
int (&ref)[3][2] = arr2;

for(auto it : arr) std::cout << it << std::endl; // [출력] 123456
ref[0][1] = 7;
ref[1][2] = 8;
for(auto it : arr) std::cout << it << std::endl; // [출력] 173458
```

# 참고자료
[모두의 코드](https://modoocode.com/141)
