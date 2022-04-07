---
layout: post
title:  "JAVA while문 기초 "
date: 2022-04-07 00:02:00
---

# JAVA while문 기초

**JAVA while문 기초**, 자바 while문 기초 사용법 입니다..

```java

package java_study;

public class While_Study {

	public static void main(String[] args) {
		//while 문은 문장을 반복해서 사용할 경우 씀
		
		//while문 기본구조
		/*
		 while (조건문) {
		    <수행할 문장1>;
		    <수행할 문장2>;
		    <수행할 문장3>;
		    ...
		}
		 */
		
		//while문은 조건문이 참인동인 반복수행함
		//10번 반복하는 예시
		int treeHit = 0;
		while (treeHit < 10) {		//threeHit 변수가 0~9가 될때까지 10회 반복 10이 되면 "나무가 넘어갑니다" 출력
		    treeHit++;				//변수가 10이 while문의 조건이 거짓이 되므로 while문을 빠져나감
		    System.out.println("나무를  " + treeHit + "번 찍었습니다.");
		    if (treeHit == 10) {			//변수가 10이 되면 "나무가 넘어갑니다" 출력
		        System.out.println("나무 넘어갑니다.");
		    }
		}
		
		
		
		//while문을 이용한 무한루프
		/*
		 
		 while (true) {    
		    <수행할 문장1>;
		    <수행할 문장2>;
		    ...
		}
		 
		 */
		
		
		
		
		//break를 이용하여 while문 빠져나가기
		int coffee = 10;
		int money = 300;

		while (money > 0) {
		    System.out.println("돈을 받았으니 커피를 줍니다.");
		    coffee--;
		    System.out.println("남은 커피의 양은 " + coffee + "입니다.");
		    if (coffee == 0) {
		        System.out.println("커피가 다 떨어졌습니다. 판매를 중지합니다.");
		        break;
		    }
		}
		//money는 항상 0보다 크기때문에 무한루프이지만 coffee값이 줄어들면서 break가 실행되어 중지됨
		
		
		
		
		//continue 사용하기
		//continue는 while문을 빠져나가는 대신 while의 맨처음(조건문)으로 돌아가게 한다
		//continue를 이용한 짝수 출력
		int a = 0;
		while (a < 10) {
		    a++;
		    if (a % 2 == 0) {
		        continue;  // 짝수인 경우 조건문으로 돌아간다.
		    }
		    System.out.println(a);  // 홀수만 출력된다.
		}
		
		
	}

}


```
