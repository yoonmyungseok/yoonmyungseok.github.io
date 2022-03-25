---
title: "[프로그래머스JAVA] Level.1 - 내적"
excerpt: 프로그래머스 코딩 테스트 연습, https://programmers.co.kr/learn/challenges
categories:
- Programmers
tags:
- [프로그래머스, 코딩테스트]
toc: false
toc_sticky: false
toc_label: "평균 구하기"
date: '2022-03-25 20:40:00'
last_modified_at: '2022-03-25'
published: true
---
### 문제 설명
길이가 같은 두 1차원 정수 배열 a, b가 매개변수로 주어집니다. a와 b의 내적을 return 하도록 solution 함수를 완성해주세요.
이때, a와 b의 내적은 a[0]\*b[0] + a[1]\*b[1] + ... + a[n-1]\*b[n-1] 입니다. (n은 a, b의 길이)

### 제한 사항
-   a, b의 길이는 1 이상 1,000 이하입니다.
-   a, b의 모든 수는 -1,000 이상 1,000 이하입니다.

### 입출력 예

 **a** | **b** | **result** 
 --- | --- | --- 
 [1,2,3,4] | [-3,-1,0,2] | 3 
 [-1,0,1] | [1,0,-1] | -2 

### 입출력 예 설명
입출력 예 #1
-   a와 b의 내적은 1\*(-3) + 2\*(-1) + 3\*0 + 4\*2 = 3 입니다.

입출력 예 #2
-   a와 b의 내적은 (-1)\*1 + 0\*0 + 1\*(-1) = -2 입니다.

### 👉나의 풀이
```java
class Solution {
    public int solution(int[] a, int[] b) {
        int answer=0;
        for(int i=0;i<a.length;i++){
            answer+=a[i]*b[i];
        }
        return answer;
    }
}
```

-   값들을 계속 더해줘야 해서 answer를 0으로 초기화
-   for문을 이용해서 index를 0부터 a배열의 길이만큼 반복
-   answer=answer+a[i]\*b[i]; => answer+=a[i]\*b[i];

> [출처: 프로그래머스 코딩 테스트 연습](https://programmers.co.kr/learn/courses/30/lessons/70128?language=java)