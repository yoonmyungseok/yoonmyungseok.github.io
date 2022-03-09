---
title: "Level.1 - 평균 구하기"
excerpt: 프로그래머스 코딩 테스트 연습, https://programmers.co.kr/learn/challenges
categories:
- Programmers
tags:
- [프로그래머스, 코딩테스트]
toc: false
toc_sticky: false
toc_label: "평균 구하기"
date: '2022-03-09 20:40:00'
last_modified_at: '2022-03-09'
published: true
---
> 코린이의 문제 풀이... 훈수 대환영!!!

## _**문제 설명**_

정수를 담고 있는 배열 arr의 평균값을 return하는 함수, solution을 완성해보세요.

## _**제한사항**_

-   arr은 길이 1 이상, 100 이하인 배열입니다.
-   arr의 원소는 -10,000 이상 10,000 이하인 정수입니다.

## _**입출력 예**_

| **arr** | **return** |
| --- | --- |
| \[1,2,3,4\] | 2.5 |
| \[5,5\] | 5 |

## _**나의 풀이**_

```
class Solution {
    public double solution(int[] arr) {
        int sum=0; // 1
        for(int i : arr){ //2
            sum+=i; //3
        }
        double answer = (double)sum/arr.length; //4
        return answer;
    }
}
```

1.  평균값을 구하기위한 합계, 정수형 변수sum을 0으로 초기화
2.  arr배열의 index값은 중요하지 않은 것 같아서 향상된 for문을 사용
3.  for문을 이용해 arr배열의 합을 구함
4.  합계를 arr배열의 길이로 나눈 값을 double로 형변환 

> 출처: 프로그래머스 코딩 테스트 연습, [https](https://programmers.co.kr/learn/challenges "프로그래머스 코딩 테스트 연습")[://programmers.co.kr/learn/challenges](https://programmers.co.kr/learn/challenges "프로그래머스 코딩 테스트 연습")