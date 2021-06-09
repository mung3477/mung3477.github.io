---
title: 자주 쓰는 std 함수들
excerpt: "PS 하면서 매번 cplusplus.com을 참고할 순 없으니, 정리도 해둘 겸 메모하면서 외울 겸 제가 자주 찾아보는 함수들을 정리해두려고 합니다."
categories:
 - PS
tags:
 - C++
 - PS
 - Algorithm
last_modified_at: 2020-07-23T13:50-05:00
use_math: true
---

PS 하면서 매번 [cplusplus](https://cplusplus.com) 를 참고할 순 없으니, 정리도 해둘 겸 메모하면서 외울 겸 제가 자주 찾아보는 함수들을 정리해두려고 합니다. PS 공부를 하면서 꾸준히 작성해야지.

---

### 1. std::sort

```void sort(first, last, comp)```

sort 함수는 리스트(배열, 벡터 등등)의 정렬하려는 값들의 범위를 [first, last) 형식으로 iterator를 인자로 받습니다. 정렬하려는 부분의 시작 부분부터, 정렬하려는 마지막 원소의 다음 위치를 주면 됩니다. 

comp 자리를 비우면 원소들을 오름차순 정렬합니다. 

내림차순으로 만들고 싶다면 comp 자리에 bool 형 리턴값을 갖는 binary 함수, 또는 클래스에 함수 객체를 만들어서 넣어줘도 됩니다. ```string```, ```int```같은 기본 타입들은 ```greater<typename>```이라는 기본 함수 템플릿이 있으니 이걸 넣어주면 됩니다. 

 comp 함수의 값이 false인 경우에 두 요소를 swap합니다(오름차순을 만드려면 $a>b$일때 true를 return). 시간복잡도는 $NlogN$입니다.

원소의 크기가 동률인 경우 순서를 유지하고 싶다면 ```std::stable_sort```를 사용하면 됩니다. 사용법은 같습니다.

---

