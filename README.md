# 새로운 자동응답 봇
> New Auto-reply Bot

![Image](https://img.shields.io/badge/CHAT%20BOT-New%20AutoReply%20Bot%202-9cf.svg) 
![Image](https://img.shields.io/badge/Language-JavaScript-yellow.svg)
![Image](https://img.shields.io/badge/Language-CoffeeScript-lightgrey.svg)
![Image](https://img.shields.io/badge/Language-LuaScript-blueviolet.svg)
![Image](https://img.shields.io/badge/Language-not_needed-ff69f4.svg)

<img src="https://raw.githubusercontent.com/sungbin5304/NewAutoReplyBot/master/IMAGE/Lve%20is%20love.png" width="300" height="300">

-----

## Introduce (Kor)
새로운 자동응답 봇(줄여서 새자봇)은 메신저 자동 답장 봇 입니다. 
반응할 채팅과 대답할 말을 설정하기 위해 코딩이 필요합니다.
지원하는 언어는 총 3가지로 자바스크립트, 커피스크립트, 루아스크립트가 있습니다.
추가로 코딩이 필요 없는 단순 자동 응답 키워드 설정도 지원 합니다.
새카봇2는 LGPL 3.0 라이선스를 가지고 오픈소스로 릴리즈 됩니다.

## Introduce (Eng)
The New Auto-reply Bot is Messenger auto-reply bot. 
Coding is required to establish which chat to respond to and what to answer.
There are three languages that are supported:
JavaScript, Coffee Script, and Ruascript.
It also supports simple, automatic response keyword settings that do not require further coding.
The New Messenger Bot is released as an open source with LGPL 3.0 license.

## Preview Image
<div>
<img src="https://raw.githubusercontent.com/sungbin5304/New-Kakaotalk-Bot-2/master/IMAGE/screener_1562496049538.png" width="300" height="500">
<img src="https://raw.githubusercontent.com/sungbin5304/New-Kakaotalk-Bot-2/master/IMAGE/screener_1562496123021.png" width="300" height="500">
<img src="https://raw.githubusercontent.com/sungbin5304/New-Kakaotalk-Bot-2/master/IMAGE/screener_1562496149897.png" width="300" height="500">
<img src="https://raw.githubusercontent.com/sungbin5304/New-Kakaotalk-Bot-2/master/IMAGE/screener_1562496170558.png" width="300" height="500">
</div>

## Developed by
![Image](https://raw.githubusercontent.com/sungbin5304/New-Kakaotalk-Bot-2/master/IMAGE/sungbin.png)
> SungBin

## Function
``` JavaScript
function response(room, msg, sender, isGroupChat, replier, ImageDB, package) {
  /*
  @String room : 메세지를 받은 방 이름 리턴
  @String sender : 메세지를 보낸 상대의 이름 리턴
  @Boolean isGroupChat : 메세지를 받은 방이 그룹채팅방(오픈채팅방은 그룹채팅방 취급) 인지 리턴
  @Object replier : 메세지를 받은 방의 Action를 담은 Object 리턴
  @Object ImageDB : 이미지 관련 데이터를 담은 Object 리턴
  @String package : 메세지를 받은 어플의 패키지명 리턴
  */
}
```
## Example
``` JavaScript
function response(room, msg, sender, isGroupChat, replier, ImageDB, package) {
  switch(package){
    case "com.kakao.talk" :
      replier.reply("카카오톡에서 메세지 받음");
      break;
    default :
      replier.reply(package + "에서 메세지 받음");
  }
    
  if(msg == "내 프로필 사진") {
    replier.reply(sender + "님의 프로필 사진을 Base64로 인코딩한 결과 입니다. \n\n" + ImageDB.getProfileImage());
  }
}
```

## Methods
``` JavaScript
replier.reply(@String content) : content를 Action이 replier인 방으로 보냄

ImageDB.getProfileImage() : 메세지를 보낸 상대방의 프로필 사진을 Base64로 인코딩해서 리턴
ImageDB.getPicture() : 받은 사진을 Base64로 인코딩해서 리턴. 단 받은지 3분이 안된 사진들 한정 작동. (Default : null)

Kaven.add(String name) : 현재 스크립트에 Kaven 스크립트 추가
```
> [[Kaven 도움말]](https://github.com/sungbin5304/New-Kakaotalk-Bot-2/blob/master/release/API_Helper.md#kaven-library)

## API List
[[API List]](https://github.com/sungbin5304/New-Kakaotalk-Bot-2/blob/master/release/API.md)

## Release Note
[[Relase]](https://github.com/sungbin5304/New-Kakaotalk-Bot-2/releases)

## 추가 예정
1. 자유 게시판 수정/삭제/댓글/공감 기능
2. 더 많은 API

## 플레이스토어 링크
[[Playstore]](https://play.google.com/apps/testing/com.sungbin.kakaotalk.bot)

## 지원하는 메신저
#### 2019.07.03 기준 작동 확인된 메신저들 목록
1. 카카오톡
2. 텔레그램
3. 메세지 (문자)
4. 라인
5. 페이스북 메세지

-----

### 공식 카페
[[Cafe]](https://cafe.naver.com/nameyee)

### 공식 디스코드 방
[[Discord]](https://discord.gg/pvnCGwE)

-----

## Project License
```
                  GNU LESSER GENERAL PUBLIC LICENSE
                       Version 3, 29 June 2007

 Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
 Everyone is permitted to copy and distribute verbatim copies
 of this license document, but changing it is not allowed.


  This version of the GNU Lesser General Public License incorporates
the terms and conditions of version 3 of the GNU General Public
License, supplemented by the additional permissions listed below.
```
