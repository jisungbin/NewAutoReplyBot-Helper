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
@String Api.post(String adress, String data)
```
> `adress`에 `data`라는 내용의 post를 전송합니다.

```js
@boolean Api.replyRoom(String room, String content)
```
> `room`이라는 방에 `content`라는 메세지를 전달합니다. 성공 여부를 반환합니다.<br>
만약 false가 리턴될 경우 `room`이라는 방으로 부터 메세지를 적어도 한개 이상 받아야 합니다.

```js
@String Api.getHtml(String adress)
```
> `adress`의 `HTML`을 파싱해 반환해 줍니다.

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
@void File.save(String path, String content)
```
> `path`이라는 경로에 `content`라는 내용을 가진 파일을 생성합니다.<br>
사용 예시 : File.save("BOT/ChatLog.log", "성빈 : 새자봇 많이 써주세요.");

```js
@String File.read(String path, String _null)
```
> `path`이라는 경로에 있는 파일을 읽어서 반환합니다. 만약 파일이 존재하지 않다면 `_null`을 반환합니다.<br>
사용 예시 : File.read("BOT/ChatLog.log", "로그가 없습니다.");

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
> `area`에 위치한 `name`이라는 학교를 찾아 `year`년 `month`월자 급식을 하루하루씩 배열에 담아 배열을 반환합니다.

``` js
@String[] School.getPlan(String area, String name, int year, int month)
```
> `area`에 위치한 `name`이라는 학교를 찾아 `year`년 `month`월자 학사일정을 하루하루씩 배열에 담아 배열을 반환합니다.
