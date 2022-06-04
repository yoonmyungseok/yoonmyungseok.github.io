---
title: "[프로그래머스JAVA] Level.1 - 정수 내림차순으로 배치하기"
excerpt: 프로그래머스 코딩 테스트 연습, https://programmers.co.kr/learn/challenges
categories:
- Programmers
tags:
- [프로그래머스, 코딩테스트]
toc: false
toc_sticky: false
toc_label: "정수 내림차순으로 배치하기"
date: '2022-06-04 15:00:00'
last_modified_at: '2022-06-04'
published: true
---
> 코린이의 문제 풀이... 훈수 대환영!!!

## 문제 설명
함수 solution은 정수 n을 매개변수로 입력받습니다. n의 각 자릿수를 큰것부터 작은 순으로 정렬한 새로운 정수를 리턴해주세요. 예를들어 n이 118372면 873211을 리턴하면 됩니다.

## 제한 조건
-	n은 1이상 8000000000 이하인 자연수입니다.

## 입출력 예
|n|return|
|:---:|:---:|
|118372|873211|

## 👉나의 풀이

```java
import java.util.Arrays;
import java.util.Collections;
class Solution {
    public long solution(long n) {
        String str=Long.toString(n);
        String[] arr=new String[str.length()];
        for(int i=0; i<arr.length; i++){
            arr[i]=str.substring(i,i+1);
        }
        Arrays.sort(arr);
        Collections.reverse(Arrays.asList(arr));
        str="";
        for(String i:arr){
            str+=i;
        }
        return Long.parseLong(str);
    }
}
```

> 출처: 프로그래머스 코딩 테스트 연습, [https://programmers.co.kr/learn/challenges](https://programmers.co.kr/learn/challenges "프로그래머스 코딩 테스트 연습")