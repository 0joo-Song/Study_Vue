# vuedongsan

Vue 유튜브 강의 - 코딩애플

#### 데이터 바인딩
 데이터 값   {{ 데이터 이름 }}
 속성         :속성="데이터 이름"


#### html 반복문
 <태그 v-for="작명 in 몇번반복" :key="작명">
  > key 안쓰면 에러남 용도 / 속성 값

- 숫자 위치에 array/object를 넣을 수 있음
- 해당 array의 개수만큼 반복

<a v-for="menuNm in menu" :key="menuNm">{{ menuNm }}</a>

<a v-for="(menuNm, i) in menu" :key="i">{{ menuNm }}</a>
인덱스도 출력 가능


