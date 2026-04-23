---
layout: post
title: 컴퓨터는 어떻게 통신하는가 (IP / Port 완전 기초)
description: IP와 Port 개념을 통해 컴퓨터 통신 구조를 이해하고 실제 포트 확인 방법까지 설명합니다.
author: dennis
date: 2026-04-23 10:00:00 +0900
categories: [Security, Network]
tags: [ip, port, network, basic]
pin: false
math: false
mermaid: false
image:
  path: /assets/commons/2026-04-23-how-computers-communicate.png
  alt: image
---

# 1. 문제 상황

웹사이트는 접속이 되는데, 특정 서비스는 접속이 안 되는 경우가 있습니다.

예를 들어:
- 서버는 살아있음 (ping 가능)
- 그런데 웹은 안 열림
- 혹은 특정 프로그램만 연결 실패

이 경우 대부분 원인은 아래 중 하나입니다:

- 포트가 열려 있지 않음
- 서비스가 실행되지 않음
- 방화벽에서 차단됨

이 문제를 이해하려면  
먼저 **컴퓨터가 어떻게 통신하는지** 알아야 합니다.

---

# 2. 핵심 개념

## 2.1 IP 주소 (Address)

IP는 **컴퓨터의 주소**입니다.

- 인터넷에서 서로를 찾기 위한 값
- 예: `192.168.0.1`

즉:
> “어느 컴퓨터인가?” 를 식별

---

## 2.2 Port (문 번호)

Port는 **컴퓨터 내부 서비스의 번호**입니다.

하나의 컴퓨터에는 여러 프로그램이 동시에 실행됩니다.

예:
- 웹 서버 (80, 443)
- SSH (22)
- DB (3306)

즉:
> “그 컴퓨터 안에서 어떤 프로그램인가?” 를 식별

---

## 2.3 통신 구조 (핵심)

컴퓨터 통신은 아래 형태입니다:
