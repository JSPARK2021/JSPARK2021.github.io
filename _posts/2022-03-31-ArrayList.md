---
layout: post
title:  "JAVA ArrayList 기초 1"
date: 2022-03-31 00:00:01
---

# JAVA ArrayList 기초

**java ArrayList 기초**, 자바 ArrayList 기초 사용법 입니다..

```java
package java_study;

import java.util.ArrayList;

//리스트는 배열과 비슷하지만 편리한 기능이 많다.
		//리스트와 배열의 가장 큰 차이는 크기가 정해져  있지 않고 동적으로 변한다는 점이다.
		
		
		//List 자료형에는 ArrayList, Vector, LinkedList 등의 자료형이 있다.
		//List 자료형중 가장 간단한 형태의 자료형 ArrayList

public class List_study {

	public static void main(String[] args) {
		ArrayList pitches = new ArrayList();  //Ctrl + shift+ o 누르면 자동으로 import java.util.ArrayList; 가 입력됨
		pitches.add("138");
		pitches.add("129");
		pitches.add("142");
		
		pitches.add(0, "133"); // 첫번째 위치에 133 삽입.
		pitches.add(1, "134"); // 두번째 위치에 134 삽입.
		
		System.out.println(pitches.get(1)); // 두분째 위치 출력, 134
		System.out.println(pitches.size()); // ArrayList의 갯수 출력, 5
		System.out.println(pitches.contains("142"));  //해당 항목이 리스트 안에 있는지 boolean으로 리턴
		System.out.println(pitches.remove("129"));    //리스트에서 해당 항목을 삭제후 결과를 true, false로 리턴
		System.out.println(pitches.remove(0));		  //""를 안쓰면 숫자를 인덱스 번호로 인식하고 해당 인덱스 번호 삭제 후 삭제된 항목 리턴
		
		
													  
		

	}

}
```
