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

## 1. bitcoingj 기본구조

NetworkParameters : 현재 네트워크 (프로덕션 또는 테스트)를 선택 하는 인스턴스입니다.
Wallet :  저장할 수 ECKey의 및 기타 데이터를.
PeerGroup : 네트워크 연결을 관리 하는 인스턴스입니다.
BlockChain : 비트 코인을 작동시키는 공유 글로벌 데이터 구조를 관리 하는 인스턴스.
BlockStore : 디스크와 같은 어딘가에 블록 체인 데이터 구조를 유지 하는 인스턴스.
WalletEventListener : 지갑 이벤트를 수신하는 구현.