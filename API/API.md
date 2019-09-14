# Log
```js
@void Log.d(String log)
```
> 로그를 디버그 모드로 작성합니다.

```js
@void Log.e(String log)
```
> 로그를 에러 모드로 작성합니다.

# Api
```js
@Context Api.getContext()
```
> `Context`를 반환해 줍니다.

```js
@boolean Api.replyRoom(String room, String msg)
```
> `room`이라는 방에 `msg`라는 메세지를 전송합니다.<br>
전송 성공 여부를 `boolean`으로 반환합니다.

```js
@boolean Api.replyRoomShowAll(String room, String msg1, String msg2)
```
> `room`이라는 방에 `msg1`는 그냥 보이고, `msg2`는 전체보기 버튼을 눌러야 보이게 전송합니다.<br>
전송 성공 여부를 `boolean`으로 반환합니다.

```js
@String Api.post(String adress, String name, String data)
```
> `adress`에 `data`라는 내용의 post를 `name`이라는 이름으로 전송합니다.

```js
@boolean Api.replyRoom(String room, String content)
```
> `room`이라는 방에 `content`라는 메세지를 전달합니다. 성공 여부를 반환합니다.<br>
만약 false가 리턴될 경우 `room`이라는 방으로 부터 메세지를 적어도 한개 이상 받아야 합니다.

```js
@String Api.getHtml(String adress)
```
> `adress`의 `HTML`을 파싱해 반환해 줍니다.<br>
※ `java.io.InputStreamReader`을 사용합니다! ※

```js
@String Api.deleteHtml(String html)
```
> `html`에서 HTML 태그를 제거해 반환해 줍니다.

```js
@String Api.translate(String source, String target, String text)
```
> 파파고에서 `text`라는 텍스트를 `target`으로 변역하여 반환합니다.<br>
※ 어플 설정에서 API 사용 설정이 필요합니다. ※

# Clock
```js
@String Clock.normal(boolean isFull)
```
> 현재 시간을 반환합니다. 만약 `isFull`이 `true`일 경우 24시간 단위로 반환합니다.

```js
@String Clock.digital(boolean isFull)
```
> 디지털 시계를 텍스트 형식으로 만들어서 반환합니다. 만약 `isFull`이 `true`일 경우 24시간 단위로 반환합니다.

```js
@String Clock.analog()
```
> 아날로그 시계를 텍스트 형식으로 만들어서 반환합니다. 시침은 나오지 않습니다.

# Device
```js
@String Device.getPhoneModel()
```
> 핸드폰 모델명을 반환합니다.

```js
@int Device.getAndroidSDKVersion()
```
> 핸드폰의 SDK 버전을 반환합니다.

```js
@String Device.getAndroidVersion()
```
> 핸드폰의 안드로이드 버전을 반환합니다.

```js
@int Device.getBattey()
```
> 핸드폰의 남은 배터리의 양을 반환합니다.

```js
@boolean Device.getIsCharging()
```
> 현재 핸드폰이 충전중인지를 반환합니다.

# File
```js
@String File.getSdcardPath()
```
> 핸드폰의 SD카드 경로를 반환합니다.<br>
※ File.save와 File.read의 path 인자엔 첨부되어 있습니다. ※

```js
@void File.createFolder(String path)
```
> `path` 라는 경로에 폴더를 생성합니다.<br>
사용 예시 : File.createFolder("AAA/BBB") - AAA라는 경로에 BBB라는 폴더를 생성

```js
@void File.write(String path, String content)
```
> `path` 라는 경로에 `content`라는 내용을 가진 파일을 생성합니다.<br>
사용 예시 : File.save("BOT/ChatLog.log", "성빈 : 새자봇 많이 써주세요.");

```js
@String File.read(String path, String _null)
```
> `path` 라는 경로에 있는 파일을 읽어서 반환합니다. 만약 파일이 존재하지 않다면 `_null`을 반환합니다.<br>
사용 예시 : File.read("BOT/ChatLog.log", "로그가 없습니다.");

```js
@void File.append(String path, String content)
```
> `path` 라는 경로에 있는 파일에 `content` 라는 내용을 덮어씁니다.

```js
@void File.remove(String name)
```
> `name`이라는 경로에 있는 파일을 삭제합니다.

# Utils
```js
@void Utils.makeToast(String content)
```
> `content`라는 내용을 가진 `android.widget.Toast`를 생성합니다.

```js
@void Utils.makeNoti(String title, String content)
```
> `title`이라는 제목과, `content`라는 내용을 가진 `android.app.Notification`을 생성합니다.

```js
@void Utils.makeVibration(int time)
```
> `time`초 동안 진동을 생성합니다.

```js
@void Utils.copy(String content)
```
> `content`라는 내용을 복사합니다.

```js
@String Utils.getWebText(String adress)
```
> `adress`의 `HTML`을 파싱해 반환해 줍니다.<br>
※ `org.jsoup.Jsoup`을 사용합니다! ※

# AppData
```js
@void AppData.putInt(String name, int value)
```
> 앱 데이터에 `name`이라는 이름으로 `int` 타입의 `value`라는 값을 가진 데이터를 저장합니다.

```js
@void AppData.putString(String name, String value)
```
> 앱 데이터에 `name`이라는 이름으로 `String` 타입의 `value`라는 값을 가진 데이터를 저장합니다.

```js
@void AppData.putBoolean(String name, Boolean value)
```
> 앱 데이터에 `name`이라는 이름으로 `Boolean` 타입의 `value`라는 값을 가진 데이터를 저장합니다.

```js
@int AppData.getInt(String name, int _null)
```
> 앱 데이터에 `name`이라는 이름으로 저장된 `int` 타입의 데이터를 불러옵니다.<br>
만약 존재하지 않는다면 `_null`을 반환합니다.

```js
@String AppData.getString(String name, String _null)
```
> 앱 데이터에 `name`이라는 이름으로 저장된 `String` 타입의 데이터를 불러옵니다.<br>
만약 존재하지 않는다면 `_null`을 반환합니다.

```js
@boolean AppData.getBoolean(String name, boolean _null)
```
> 앱 데이터에 `name`이라는 이름으로 저장된 `boolean` 타입의 데이터를 불러옵니다.<br>
만약 존재하지 않는다면 `_null`을 반환합니다.

```js
@void AppData.remove(String name)
```
> 앱 데이터에서 `name`이라는 이름을 가진 데이터를 제거합니다.

```js
@void AppData.clear()
```
> `AppData API`로 작업한 앱 데이터를 초기화 합니다.

# Bridge
```js
@String Bridge.getVariableValue(String scriptName, String variabaleName)
```
> 스크립트 `scriptName` 에서 `variabaleName` 라는 변수명을 가진 변수의 값을 `String` 타입으로 반환합니다.<br>
※ 스크립트 이름에 확장자를 포함해야 합니다! Ex) Bridge.getVariableValue("테스트.js", "a"); ※

# Image
```js
@void Image.getXY()
```
> 좌표를 얻기 위한 화면을 표시합니다.

```js
@void Image.send(int[] xy, int[] xy2, int[] xy3, int[] xy4, String imagePath)
--- API를 통한 사용 불가 (API 추가 가능 인자 부적합), Kaven으로 사용 바람 ---
```
> [[참고]](https://github.com/sungbin5304/NewAutoReplyBot-Helper/blob/master/API/API_Helper.md#picture-transmission-api)

# Kaven
> [[참고]](https://github.com/sungbin5304/NewAutoReplyBot-Helper/blob/master/API/API_Helper.md#kaven-library)

# School
``` js
@String[] School.getMeal(String area, String name, int year, int month)
```
> `area`에 위치한 `name`이라는 학교를 찾아 `year`년 `month`월자 급식을 하루하루씩 배열에 담아 배열을 반환합니다.<br>
오류가 날 경우 0번 index에 `false`를 담고, 1번 index에 오류 내용을 담습니다.

``` js
@String[] School.getPlan(String area, String name, int year, int month)
```
> `area`에 위치한 `name`이라는 학교를 찾아 `year`년 `month`월자 학사일정을 하루하루씩 배열에 담아 배열을 반환합니다.<br>
오류가 날 경우 0번 index에 `false`를 담고, 1번 index에 오류 내용을 담습니다.
