---
layout: post
title: "2021 테스트 데이터"
subtitle: "1차원 배열"
categories: dev
tags: algorithm
comments: true
---

## 알고리즘 공부

> 알고리즘 사이트 `백준` 에서 단계별로 묶어서 올릴 예정이다. 이전에 했던 내용들은 두고, 1차원 배열 단계의 4번째 문제부터 업로드할 예정.

- 목차
  - [10818 최소,최대](#10818)
  - [2562 최댓값](#2562)
  - [2577 숫자의 개수](#2577)
  - [3052 나머지](#3052)
  - [1546 평균](#1546)
  - [8958 OX퀴즈](#8958)
  - [4344 평균은 넘겠지](#4344)

<br/>

## 10818

---

![ALTER TEXT](/assets/img/dev/algorithm/2021-04-04-dev-algorithm-1.png)

<br/>

> N을 먼저 스캐너로 받아서 입력받은 N 만큼 반복문을 돌려 int [] 에 하나씩 담아준 뒤 Arrays 클래스의 sort() 함수로 한번 정렬해주고, 가장 작을 0번 인덱스와 가장 큰 마지막 인덱스 값을 출력!

<br/>

```jsx
package baekjoon.ex_array;

import java.util.Arrays;
import java.util.Scanner;

public class Q_10818 {

	public static void main(String[] args) throws Exception {
// TODO Auto-generated method stub

		Scanner sc = new Scanner(System.in);
		int N = sc.nextInt();
		int[] arr = new int[N];
		for (int i = 0; i < N; i++) {
			arr[i] = sc.nextInt();
		}
		Arrays.sort(arr);
		System.out.println(arr[0] + " " + arr[arr.length - 1]);

		sc.close();
	}

}
```

<br/><br/>

## 2562

---

<br/><br/>

## 2577

---

![ALTER TEXT](/assets/img/dev/algorithm/2021-04-04-dev-algorithm-2.png)

<br/>

> 내가 생각한 접근법은 우선 스캐너로 A,B,C 를 입력받고 세 값을 곱한 값을 임의의 int 변수에 담아준다. 그리고 그걸 String타입으로 바꿔서 CharAt()으로 한자리씩 반복문 돌려서 비교해서 카운트하는 방식이다. 효율적인 방법이 맞는지는 모르겠지만 일단 답은 정확히 나온다.

<br/>

```jsx
package baekjoon.ex_array;

import java.util.Scanner;

public class Q_2577 {

	public static void main(String[] args) throws Exception {
// TODO Auto-generated method stub

		Scanner sc = new Scanner(System.in);
		int A = sc.nextInt();
		int B = sc.nextInt();
		int C = sc.nextInt();

		int mul = A * B * C;
		String strMul = mul + "";
		int[] cnt = { 0, 0, 0, 0, 0, 0, 0, 0, 0, 0 };
		for (int i = 0; i < strMul.length(); i++) {
			switch (Integer.parseInt((strMul.charAt(i)) + "")) {
			case 0:
				cnt[0]++;
				break;
			case 1:
				cnt[1]++;
				break;
			case 2:
				cnt[2]++;
				break;
			case 3:
				cnt[3]++;
				break;
			case 4:
				cnt[4]++;
				break;
			case 5:
				cnt[5]++;
				break;
			case 6:
				cnt[6]++;
				break;
			case 7:
				cnt[7]++;
				break;
			case 8:
				cnt[8]++;
				break;
			case 9:
				cnt[9]++;
				break;
			default:
				break;
			}
		}
		for (int i = 0; i < cnt.length; i++) {
			System.out.println(cnt[i]);
		}

		sc.close();
	}

}
```

<br/><br/>

## 3052

---

나머지

## 1546

---

평균

## 8958

---

OX퀴즈

## 4344

---

평균은 넘겠지
