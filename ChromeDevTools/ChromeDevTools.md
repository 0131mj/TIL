# Chrome Dev Tools

크롬 개발자 도구

## Elements 탭

- sources는 소스를 그대로 보여주는 반면, Elements는 렌더링된 결과물을 보여준다.
- 



## Properties Tab 

- 돔이 어떤 속성을 갖고 있는지 알려줌



#### DOM Breakpoints

- 브레이크 포인트를 걸 수 있음
- 브레이크 포인트를 걸 때, 1) 문장 중간에 커서를 위치한 다음 줄번호를 위치하게 하면 긴 줄중에서 브레이크포인트가 가능한 곳을 알려줘서 정확하게 걸 수 있음.

####  XHR Breakpoint

- 통신이 가능한 곳에 걸때 사용

#### callStack - blackbox

- stack에서 blackbox 기능을 사용하여 비활성화할 수 있음.







## Network 탭 

- 이미지 등을 가져오는 모습을 보여줌
- 얼마나 많은 시간이 걸리고, 어떤 순서로 실행되는지, 어떤 요청이 오고 가는지



### 파일위에 있는 탭메뉴 

#### status

- 304 : 이미 접속한 적이 있어서 데이터를 갖고 있는 경우

#### Waterfall 

갖다대면 요청 및 응답에 사용된 소요시간 등을 볼 수 있다. 

#### 파란줄 :  

이벤트라는 것이 발생한 시점 DOM content 돔 컨텐트로드가 끝난 시점

#### 빨간줄 :  

소스가 모두 로딩된 시점



### 빨간색 점

쌓아서 보여준다. 







## Sources 탭

자바스크립트 디버깅 할 때 주로 사용된다. 

- 파일 내 검색 : Ctrl+F

- 전체 검색 : Ctrl + Shift + F
- 함수만 검색(해당문서 안) : Ctrl + Shift + O



### 네비게이션 영역



### 우측메뉴

- 위아래 메뉴 : 함수 안으로 들어왔다가 나가는 것
- BreakPoints 
- 파란색 화살표 : 다음 브레이크포인트까지 실행
- watch 탭 : 변수가 어떻게변하는지를 관찰 가능
- XHR : ajax통신을 관찰할 수 있는 탭





### 디버깅 순서

1. BreakPoint 설정 : 앱을 실행하는 도중에 멈추고 상태를 보여준다.



## Network Tab







## Console

- ctrl + shift + J : 콘솔탭 단축키



#### monitorEvents

해당 엘리먼트의 모든 이벤트를 콘솔로 찍어서 보여준다.

```javascript
const searchBtn = document.getElementById("searchBtn")
monitorEvents(searchBtn ['click', 'mouseout'])
```



#### debug(함수명)

```javascript
debug(함수명)
```



#### monitor(함수명) / ㅕㅜmonitor(함수명)

해당 함수가 호출될때마다 보여준다.

```javascript
monitor(함수명)
```



console.timer





## Audit

- 웹페이지의 현재 상태를 감사, 조언해주는 



https://www.youtube.com/watch?v=oYvtsHu6GmY

30분 보는중

- 공식사이트 : https://developers.google.com/web/tools/chrome-devtools/?hl=ko