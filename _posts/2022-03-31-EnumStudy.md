---
layout: post
title:  "Enum 기초"
---

# JAVA Enum 기초

**java Enum 기초**, 자바 Enum(상수집합) 기초 사용법 입니다..

```java
// Enum(상수집합)이란?
// 서로 관련이 있는 여러개의 상수 집합을 정의할 대 사용하는 자료형이다.


package java_study;

public class Emum_study {
	//상수집합 생성
	enum CoffeeType {
	    AMERICANO,
	    ICE_AMERICANO,
	    CAFE_LATTE
	};
	
	public static void main(String[] args) {
		
		
		//상수집합 사용하기
		System.out.println(CoffeeType.AMERICANO);  // AMERICANO 출력
        System.out.println(CoffeeType.ICE_AMERICANO);  // ICE_AMERICANO 출력
        System.out.println(CoffeeType.CAFE_LATTE);  // CAFE_LATTE 출력
        
        for(CoffeeType type: CoffeeType.values()) {
            System.out.println(type);  // 순서대로 AMERICANO, ICE_AMERICANO, CAFE_LATTE 출력
    }
	}

}

```
