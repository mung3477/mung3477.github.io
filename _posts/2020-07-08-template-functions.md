---
title: 자주 쓰는 template 함수들
excerpt: ""
categories:
 - PS
tags:
 - C++
 - PS
 - Algorithm
last_modified_at: 2020-07-08T20:31-05:00
---

PS 하면서 매번 [cplusplus](https://cplusplus.com) 를 참고할 순 없으니, 정리도 해둘 겸 메모하면서 외울 겸 제가 자주 찾아보는 함수들을 정리해두려고 합니다. PS 공부를 하면서 꾸준히 작성해야지.

---

### 1. std::sort

```void sort(first, last, comp)```

sort 함수는 리스트(배열, 벡터 등등)의 정렬하려는 값들의 범위를 [first, last) 형식으로 iterator를 인자로 받습니다. 정렬하려는 부분의 시작 부분부터, 정렬하려는 마지막 원소의 다음 위치를 주면 됩니다. 

comp 자리에는 bool 형 리턴값을 갖는 binary 함수가 들어갑니다. comp 함수의 값이 false인 경우에 두 요소를 swap합니다. 두 개씩 비교하면서 swap하는 형식인 것 같습니다(gnu에 따라 알고리즘이 다른 듯). 따라서 시간복잡도는 NlogN입니다.

comp를 비운 채 2개의 인자만 주면 default로 오름차순 정렬이 됩니다. 

---

