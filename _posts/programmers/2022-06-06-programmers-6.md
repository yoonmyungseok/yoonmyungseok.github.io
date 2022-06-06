---
title: "[프로그래머스JAVA] Level.1 - 모의고사"
excerpt: 프로그래머스 코딩 테스트 연습, https://programmers.co.kr/learn/challenges
categories:
- Programmers
tags:
- [프로그래머스, 코딩테스트]
toc: false
toc_sticky: false
toc_label: "모의고사"
date: '2022-06-06 23:50:00'
last_modified_at: '2022-06-06'
published: true
---
> 코린이의 문제 풀이... 훈수 대환영!!!

## 문제 설명
수포자는 수학을 포기한 사람의 준말입니다. 수포자 삼인방은 모의고사에 수학 문제를 전부 찍으려 합니다. 수포자는 1번 문제부터 마지막 문제까지 다음과 같이 찍습니다.

1번 수포자가 찍는 방식: 1, 2, 3, 4, 5, 1, 2, 3, 4, 5, ...
2번 수포자가 찍는 방식: 2, 1, 2, 3, 2, 4, 2, 5, 2, 1, 2, 3, 2, 4, 2, 5, ...
3번 수포자가 찍는 방식: 3, 3, 1, 1, 2, 2, 4, 4, 5, 5, 3, 3, 1, 1, 2, 2, 4, 4, 5, 5, ...

1번 문제부터 마지막 문제까지의 정답이 순서대로 들은 배열 answers가 주어졌을 때, 가장 많은 문제를 맞힌 사람이 누구인지 배열에 담아 return 하도록 solution 함수를 작성해주세요.

## 제한 조건
-	시험은 최대 10,000 문제로 구성되어있습니다.
-	문제의 정답은 1, 2, 3, 4, 5중 하나입니다.
-	가장 높은 점수를 받은 사람이 여럿일 경우, return하는 값을 오름차순 정렬해주세요.

## 입출력 예
answers|return
---|---
[1,2,3,4,5]|[1]
[1,3,2,4,2]|[1,2,3]

## 입출력 예 설명
#### 입출력 예 #1

수포자 1은 모든 문제를 맞혔습니다.
수포자 2는 모든 문제를 틀렸습니다.
수포자 3은 모든 문제를 틀렸습니다.
따라서 가장 문제를 많이 맞힌 사람은 수포자 1입니다.

#### 입출력 예 #2

모든 사람이 2문제씩을 맞췄습니다.

## 👉나의 풀이
```java
import java.util.ArrayList;
class Solution {
    public int[] solution(int[] answers) {
        int[] answer = {};
        ArrayList<Integer> list = new ArrayList<>();
        int[] arr1 = {1,2,3,4,5}; //5
        int[] arr2 = {2,1,2,3,2,4,2,5}; //8
        int[] arr3 = {3,3,1,1,2,2,4,4,5,5}; //10
        int a=0, b =0, c =0;
        
        for(int i =0; i<answers.length; i++){
            if(arr1[i%5] == answers[i]) a++;
            if(arr2[i%8] == answers[i]) b++;
            if(arr3[i%10] == answers[i]) c++;
        }
        int max = Math.max(Math.max(a, b),c); 
        
        if(max==a) list.add(1);
        if(max==b) list.add(2);
        if(max==c) list.add(3);
        
        answer = new int[list.size()];
        
        for(int i =0; i<answer.length; i++) {
        	answer[i] = list.get(i);
        }
        return answer;
    }
}
```

> 출처: 프로그래머스 코딩 테스트 연습, [https://programmers.co.kr/learn/challenges](https://programmers.co.kr/learn/challenges "프로그래머스 코딩 테스트 연습")