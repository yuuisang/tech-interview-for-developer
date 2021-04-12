---
layout: post
title: "Rest API 서버와 클라이언트의 물리적/논리적 분리"
date: 2021-04-12 21:24:32 +0900
categories: Web
tags: [RESTAPI, HTTP]
---

## 백엔드와 프론트엔드의 물리적/논리적 분리

> RESTAPI로 **JSON **타입의 데이터만 넘겨주는 방식은 하나의 소스(Data)를 다양한 클라이언트(웹,앱 등)에서 사용하고자 하는 목적이라고 생각한다.

<br>
스마트폰이 등장하면서 웹과 앱들에서 같은 소스를 보여주기 위해 서버쪽 로직을 API 형태로 분리하고, 각 클라이언트는 그것을 호출해서 각자 맞는 방식으로 보여주기 위한 진화라고 생각함.

<br>이게 하나의 방법론 처럼 되면서 웹 단독으로 서비스 하면서도 프론트와 서버단(API)를 분리해서 구성하고 있다고 생각함.

<br>API와 프론트의 구문은 URI 로 구분하는 방법을 많이 사용한다.

하나의 **WAS**에서

- http://www.xxx.com/web/~ 으로 접근하면 프론트

- http://www.xxx.com/api/~ 로 접근하면 API 접근으로 간주 하도록 설정하면 하나의 서버에서 구동 할 수도 있다.