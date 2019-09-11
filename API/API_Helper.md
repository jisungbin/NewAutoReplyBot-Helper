# Picture Transmission API
It is a picture send API in New Kakaotalk Bot 2.

![logo](https://img.shields.io/badge/API-Picture_transmission-blue.svg)

## 1. 좌표 설정법
1. 개발자 모드 활성화 [[참고 링크]](https://androidsfactory.com/310)
2. 개발자 옵션에서 포인터 위치표시 활성화
3. 아래 이미지 처럼 화면 상단에 X좌표와 Y좌표 표시 되는지 확인 (Xv와 Yv가 아니라 X와 Y)
![Image](https://raw.githubusercontent.com/sungbin5304/NewAutoReplyBot-Helper/master/IMAGE/xyz.png)
4. ```Image.getXY()``` 실행 후 아래 이미지 처럼 표시되는 화면에서 채팅 버튼 부분, 전송할 채팅방 체크박스 부분, 확인 버튼 부분, ← 버튼 부분의 X, Y 좌표 값을 기록
![Image](https://raw.githubusercontent.com/sungbin5304/NewAutoReplyBot-Helper/master/IMAGE/kakaotalk.png)

## 2. 접근성 권한 허용
안드로이드 설정에서 접근성 → 서비스에서 카카오톡 봇 활성화

## 3. API 호출
1. 1.4 번에서 가져온 X,Y 좌표 값을 차례대로 변수에 배열형태로 등록.
> ex) ```var xy = [500, 500];```
2. API 호출
> ex) ```Image.send(xy, xy2, xy3, xy4, "Picture/AAA.png");```

### ※ 주의사항 ※
1. 안드로이드 버전 7.0.0 이상 사용 가능합니다.
2. 오류가 날 경우 접근성 권한을 해제했다가 다시 설정 해 주세요.
3. 핸드폰 화면이 켜져 있을때만 사용 가능합니다.
4. 카카오톡에 잠금이 없어야 합니다.

-----

# Kaven Library
It is a Maven for New Kakaotalk Bot 2.

![logo](https://img.shields.io/badge/Library-Kaven-pink.svg)

## What is Kaven?
Kaven은 Maven의 카카오톡 봇 버전 입니다.
> Maven : 아파치 메이븐은 자바용 프로젝트 관리 도구이다. 아파치 앤트의 대안으로 만들어졌다. 아파치 라이선스로 배포되는 오픈 소스 소프트웨어이다. (출처: 구글 검색)

## 어떻게 Kaven을 업로드 하나요?
1. 새카봇2 자유게시판에 들어간다.
2. 글을 작성하는 + 버튼을 누르고 스크립트 업로드 버튼을 누른다.
3. 자신이 Kaven에 올리고 싶은 스크립트를 선택한다.
(이때 Kaven에 올라가는 이름은 스크립트의 이름이다.)
4. 툴바에 있는 저장 버튼을 누른다.

## 어떻게 Kaven을 나의 소스에 적용하나요?
1. 새카봇2 Kaven 에 들어간다.
2. 하단에 있는 + 버튼을 누르고 다이얼로그가 표시되면 자신이 추가하고 싶은 Kaven의 스크립트 이름을 입력한다.
3. 다이얼로그에 있는 다운로드 버튼을 누른다.
4. 자신의 스크립트 **최상단**에 `Kaven.add(자신이 다운로드한 Kaven 스크립트 이름)` 을 입력한다.
> ex) `Kaven.add("ImageSender.js");`

## 어떻게 내가 다운로드한 Kaven을 제거하나요?
1. 새카봇2 Kaven 에 들어간다.
2. 자신이 제거하고 싶은 Kaven 스크립트 이름을 클릭한다.
3. 다이얼로그가 뜨면 삭제 버튼을 누른다.

또는 

1. 툴바에 있는 쓰레기통 버튼을 누른다. (다운로드한 Kaven 스크립트 전체 삭제)
