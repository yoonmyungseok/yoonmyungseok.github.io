---
title: "[프로그래머스JAVA] Level.1 - 문자열 다루기 기본"
excerpt: 프로그래머스 코딩 테스트 연습, https://programmers.co.kr/learn/challenges
categories:
- Programmers
tags:
- [프로그래머스, 코딩테스트]
toc: false
toc_sticky: false
toc_label: "문자열 다루기 기본"
date: '2022-06-01 19:40:00'
last_modified_at: '2022-06-01'
published: true
---
### 문제 설명
문자열 s의 길이가 4 혹은 6이고, 숫자로만 구성돼있는지 확인해주는 함수, solution을 완성하세요. 예를 들어 s가 "a234"이면 False를 리턴하고 "1234"라면 True를 리턴하면 됩니다.

### 제한 사항
- s는 길이 1 이상, 길이 8 이하인 문자열입니다.

### 입출력 예

|s|return|
|:---:|:---:|
|"a234"|false|
|"1234"|true|

### 👉나의 풀이
```java
class Solution {
    public boolean solution(String s) {
        boolean answer = true;
        for(int i=0;i<s.length();i++){
            if((s.charAt(i)>=48&&s.charAt(i)<=57)&&(s.length()==4||s.length()==6)){
                answer=true;
            }else{
                answer=false;
                break;
            }  
        }
        return answer;
    }
}
```

> [출처: 프로그래머스 코딩 테스트 연습](https://programmers.co.kr/learn/courses/30/lessons/12918)