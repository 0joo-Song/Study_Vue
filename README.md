# Study Vue

Vue 유튜브 강의 - 코딩애플


## 1. 데이터 바인딩

 >데이터 값   {{ 데이터 이름 }}
 >속성         :속성="데이터 이름"



## 2. html 반복문
> <태그 v-for="작명 in 몇번반복" :key="작명">
> key 안쓰면 에러남 용도 / 속성 값
>
> 숫자 위치에 array/object를 넣을 수 있음
> 해당 array의 개수만큼 반복
>인덱스도 출력 가능
 
```js
<a v-for="menuNm in menu" :key="menuNm">{{ menuNm }}</a>
```
```js
<a v-for="(menuNm, i) in menu" :key="i">{{ menuNm }}</a>
```




## 3. 이벤트 핸들러
> 버튼을 클릭했을때 이벤트 효과
> v-on:click   
>vue 방식 : @click

```html
<button @click="rpCnt++">허위매물신고</button> <span>신고수 : {{ rpCnt }}</span>
```
```html
<button @click="rpCnt += 1">허위매물신고</button> <span>신고수 : {{ rpCnt }}</span>
```

- 추가 기능이 다양하다.
    - @mouseover  : 마우스를 올렸을 때
    - @input : 작성할 때
    - @change : 변경될 때 
    - . . .
   
> 스크립트로 함수를 만들 때
- 태그에 함수 명 입력
```html
<button @click="clcickReport">허위매물신고</button> <span>신고수 : {{ rpCnt }}</span>
```
- 스크립트 methods 안에 함수 생성
    - 주의사항: 함수안에서 데이터 쓸 땐 this.데이터명 
```js
  export default {
  name: 'App',
  data(){
    return {
      rpCnt : 0,
    }
  },
  methods : {
    clcickReport(){
      this.rpCnt += 1;
    }
  },
  components: {
  }
}
```


## 4. 조건식 v-if
> v-if="조건식"
>
> v-if의 값이 true 일때 동작
```js
  <div class="black-bg" v-if="modalOpen">
    <div class="white-bg">
      <h4>상세페이지</h4>
      <p>상세페이지 내용</p>
      <button @click="modalOpen = false">닫기</button>
    </div>
  </div>
```

## 5. import / export
>  import / export 쓰는법 
>
> 파일을 보낼 js파일 하단에 export defalt 내보낼변수명
>
> 가져올 파일에 스트립트 안에 
>
> import 가져올변수 from 경로
>
> 여러개의 파일을 내보낼 때는 export{ 변수명, 변수명2 }
>
> 가져올 때도 import { 변수명, 변수명2 } from 경로
