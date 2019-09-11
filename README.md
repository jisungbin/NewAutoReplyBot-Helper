# 새로운 자동응답 봇
> New Auto-reply Bot

![Image](https://img.shields.io/badge/CHAT%20BOT-New%20AutoReply%20Bot%202-9cf.svg) 
![Image](https://img.shields.io/badge/Language-JavaScript-yellow.svg)
![Image](https://img.shields.io/badge/Language-CoffeeScript-lightgrey.svg)
![Image](https://img.shields.io/badge/Language-LuaScript-blueviolet.svg)
![Image](https://img.shields.io/badge/Language-not_needed-ff69f4.svg)

<img src="https://raw.githubusercontent.com/sungbin5304/NewAutoReplyBot-Helper/master/IMAGE/Lve%20is%20love.png" width="300" height="300">

-----

## 설명
새자봇(새로운 자동응답 봇)은 메신저 자동 답장 봇 입니다.<br>
반응할 채팅과 대답할 말을 설정하기 위해 코딩이 필요합니다.<br>
지원하는 언어는 총 3가지로 자바스크립트, 커피스크립트, 루아스크립트가 있습니다.<br>
추가로 코딩이 필요 없는 단순 자동 응답 키워드 설정도 지원 합니다.


## 미리보기 이미지
<div>
<img src="https://raw.githubusercontent.com/sungbin5304/NewAutoReplyBot-Helper/master/IMAGE/screener_1562496049538.png" width="300" height="500">
<img src="https://raw.githubusercontent.com/sungbin5304/NewAutoReplyBot-Helper/master/IMAGE/screener_1562496123021.png" width="300" height="500">
<img src="https://raw.githubusercontent.com/sungbin5304/NewAutoReplyBot-Helper/master/IMAGE/screener_1562496149897.png" width="300" height="500">
<img src="https://raw.githubusercontent.com/sungbin5304/NewAutoReplyBot-Helper/master/IMAGE/screener_1562496170558.png" width="300" height="500">
</div>

## 개발
![Image](https://raw.githubusercontent.com/sungbin5304/NewAutoReplyBot-Helper/master/IMAGE/sungbin.png)

## 메인 함수
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

## 메인함수 인자  설명
``` JavaScript
@replier
replier.reply(@String content) : content를 Action이 replier인 방으로 보냄

@ImageDB
ImageDB.getProfileImage() : 카카오톡에서 메세지를 받은 상대방의 프로필 사진을 Base64로 인코딩해서 리턴
ImageDB.getPicture() : 카카오톡에서 가장 마지막으로 받은 사진을 Base64로 인코딩해서 리턴. (Default : null)

※ ImageDB.getPicture() 사용시 `data parcel size 1541904 bytes` 라는 오류가 발생할 수 있습니다.<br>
이러한 경우는 사진의 Base64 값이 너무 길어서 발생하는 오류이니, 용량이 작은 사진으로 받으면 정상 작동 합니다.
```

## 자바스크립트 작성 예시
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

-----

## API 리스트
[[API List]](https://github.com/sungbin5304/NewAutoReplyBot-Helper/blob/master/API/API.md)

## 릴리즈 노트
[[Relase]](https://github.com/sungbin5304/NewAutoReplyBot-Helper/releases)

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

### 고마운 분들
PartWorm, Nenka
