---
layout: post
current: post
cover:  assets/built/images/blockchain/blockchain-1.png
navigation: True
title: Bitcoin 지갑
date: 2021-02-09 16:40:00
tags: [itstory]
class: post-template
subclass: 'post blockchain'
author: joo-pe
---

{% include blockchain-table-of-contents.html %}

### bitcoin 참고 소스

bitcoinj 프로젝트를 참고하였다.
bitcoinj는 비트 코인 프로토콜 작업을위한 라이브러리다. 
비트 코인 코어의 로컬 사본없이 지갑을 유지하고 트랜잭션을 송수신 할 수 있으며 다른 많은 고급 기능이 있습니다. 
Java로 구현되지만 모든 JVM 호환 언어에서 사용할 수 있다.

## bitcoinj 

https://bitcoinj.org/getting-started-java


## 1. bitcoinj 기본구조

NetworkParameters : 현재 네트워크 (프로덕션 또는 테스트)를 선택 하는 인스턴스입니다.
Wallet :  저장할 수 ECKey의 및 기타 데이터를.
PeerGroup : 네트워크 연결을 관리 하는 인스턴스입니다.
BlockChain : 비트 코인을 작동시키는 공유 글로벌 데이터 구조를 관리 하는 인스턴스.
BlockStore : 디스크와 같은 어딘가에 블록 체인 데이터 구조를 유지 하는 인스턴스.
WalletEventListener : 지갑 이벤트를 수신하는 구현.

## 2. wallet 실행시키기

1. JavaFX 를 다운 받는다.
   intelliJ 내 Edit Configurations에 아래를 추가한다.
   lib는 자신의 lib로 설정하여 준다.

~~~
--module-path /Users/jaden/Downloads/javafx-sdk-11.0.2/lib --add-modules=javafx.controls,javafx.fxml
~~~


2. wallettemplate 모듈에서 Main 클래스를 실행시킨다.

![img.png](/assets/built/images/blockchain/blockchain-4.png)

가 실행되는 것을 볼 수 있다.
기본은 MainNet으로 접속된다.

3. NetworkParameters 을 참고하여 메인넷을 바꾸어준다.