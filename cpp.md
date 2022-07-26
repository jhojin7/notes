# C++

## `rbegin`, `rend`
- 역순으로 iterator를 사용한 for loop을 돌고 싶을때 사용.
- 그냥 정방향으로 하려면 https://stackoverflow.com/a/14374550/3413574
- https://stackoverflow.com/a/3610963/3413574
- 주의할것: begin, end도 마찬가지지만, begin이 첫번째 elem을 가르키는 iterator고, end는 마지막 iterator가 아니라 마지막 iter의 다음 elem을 가르킴.
  - https://en.cppreference.com/w/cpp/iterator/rbegin (그림있음)
```cpp
// for (auto it = company.begin(); it!=company.end(); it++)
//     cout << *it << '\n';
for (auto it = company.rbegin(); it!=company.rend(); it++){
    cout << *it << '\n';
}
```

## `long int` vs `long long int`
- 그냥 long은 (최소)32bit, long long은 (최소)64bit. 
- (표준마다 차이가 있는듯함. 적어도 cpp표준은 32,64)
- 그냥 문제풀때 대충 엄청 큰 수 나올 것 같고 mod 쓰라하면 후자가 편할듯함. (아니면 py)
- short=> 16bit.
- References
  - https://stackoverflow.com/a/18971763/3413574
  - https://en.cppreference.com/w/cpp/language/types
  - [boj15829 코드](https://github.com/jhojin7/problem-solving/blob/main/%EB%B0%B1%EC%A4%80/Bronze/15829.%E2%80%85Hashing/Hashing.cc)

## a^b mod m 구현
- 파이썬의 `pow(base,exp,mod)`과 동일함. 
- `math.pow`가 아니라 빌트인 함수임. import 필요없음.
- https://docs.python.org/3/library/functions.html?highlight=pow#pow
- [boj15829 코드](https://github.com/jhojin7/problem-solving/blob/main/%EB%B0%B1%EC%A4%80/Bronze/15829.%E2%80%85Hashing/Hashing.cc)
```cpp
using LLong = long long int;
LLong power(int a, int b, int m){
    LLong ret = 1;
    for (int i=0;i<b;i++)
        ret = (ret*a)%m;
    return ret;
}
```
