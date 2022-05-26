# Study Vue

Vue 유튜브 강의 - 코딩애플


## 데이터 바인딩
 >데이터 값   {{ 데이터 이름 }}
 >속성         :속성="데이터 이름"


## html 반복문
> <태그 v-for="작명 in 몇번반복" :key="작명">
> key 안쓰면 에러남 용도 / 속성 값
>
> 숫자 위치에 array/object를 넣을 수 있음
> 해당 array의 개수만큼 반복

<pre><code><a v-for="menuNm in menu" :key="menuNm">{{ menuNm }}</a></code></pre>

<pre><code><a v-for="(menuNm, i) in menu" :key="i">{{ menuNm }}</a></code></pre>

인덱스도 출력 가능


## 이벤트 핸들러
- 버튼을 클릭했을때 이벤트 효과
> v-on:click   
>vue 방식 : @click

<pre><code><button @click="rpCnt++">허위매물신고</button> <span>신고수 : {{ rpCnt }}</span></code></pre>
<pre><code><button @click="rpCnt += 1">허위매물신고</button> <span>신고수 : {{ rpCnt }}</span></code></pre>

- 마우스를 올렸을 때
@mouseover

등 다양한 함수가 있다.
함수를 만들 때  methods : { 함수명(){} }


## 이미지 넣는 법