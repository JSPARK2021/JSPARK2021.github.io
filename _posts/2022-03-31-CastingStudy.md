---
layout: post
title:  "JAVA Casting 기초"
date: 2022-03-31 00:00:07
---

# JAVA Casting 기초

**java Casting 기초**, 자바 Casting (형변환), final 기초 사용법 입니다..

```java
//자바의 형변환과 final

package java_study;

import java.util.List;

public class CastingStudy {

	public static void main(String[] args) {
		//문자열 자료형에 내용은 숫자 값일때
		//문자열을 정수로 바꾸려면 Integer 클래스를 사용한다.
		String num = "123";
        int n = Integer.parseInt(num);
        System.out.println(n);  // 123 출력
        
        
        
        //정수 321을 문자열 "321"로 변환 
        int n1 = 321;
        String num1 = "" + n1;
        System.out.println(num1);  // 321 출력
        
        //정수 456을 문자열 "456"로 변환 
        int n3 = 456;
        String num2 = String.valueOf(n3);
        String num3 = Integer.toString(n3);
        System.out.println(num2);  // 믄자열 456 출력
        System.out.println(num3);  // 정수형 456 출력
		
        //소숫점 숫자 문자열을 실수형으로 변환 
        String num4 = "123.456";
        double d = Double.parseDouble(num4);
        System.out.println(d);
        
        
        //실수형을 정수형으로 변환
        int n5 = 123;
        double d1 = n5;  // 정수를 실수로 바꿀때에는 캐스팅이 필요없다.
        System.out.println(d1);  // 123.0 출력

        double d2 = 123.456;
        int n2 = (int) d2; // 실수를 정수로 바꿀때에는 반드시 정수형으로 캐스팅해 주어야 한다.
        System.out.println(n2);  // 소숫점이 생략된 123 출력
        
        
        
        /*
         !! 실수형 문자열을 정수로 변경하면 오류발생!!
        String num6 = "123.456";
        int n6 = Integer.parseInt(num6);  // 실수 형태의 문자열을 정수로 변환할 경우 NumberFormatException이 발생한다.
        */
        
        
        //final이란?
        //자료형에 값을 단 한번만 설정할 수 있게 강제하는 키워드
        // 프로그램 수행 도중 그 값이 변경되면 안되는 상황에서 사용한다. 
        /*
        final int nn = 123;  // final 로 설정하면 값을 바꿀수 없다.
        nn = 456;  // 컴파일 에러 발생
        */
        
        
        //리스트의 경우에서도 final 사용시 재할당 불가능
        /*
        final ArrayList<String> a = new ArrayList<>(Arrays.asList("a", "b"));
        a = new ArrayList<>(Arrays.asList("c", "d"));  // 컴파일 에러 발생
        */
        
        
        //리스트의 경우 final 선언시 리스트에서 값을 더하거나(add) 빼는(remove)것은 가능함
        //더하는것과 빼는것도 불가능하게 만드려면 List.of 사용하면 됨
        /*
        final List<String> a = List.of("a", "b");
        a.add("c");  // UnsupportedOperationException 발생
        */
	}

}

```
