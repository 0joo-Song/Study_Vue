<template>
  <!-- 모달창 -->
  <div class="black-bg" v-if="modalOpen == true">
    <div class="white-bg">
      <h4>상세페이지</h4>
      <p>상세페이지 내용</p>
      <button @click="modalOpen = false">닫기</button>
    </div>
  </div>

  <div class="menu">
    <a v-for="(menuNm, i) in menu" :key="i">{{ menuNm }}</a>
  </div>

  <div v-for="(room, i) in oneRoom" :key="i">
    <img :src="room.image" class="room-img">
    <h4 @click="modalOpen = true">{{ room.title }}</h4>
    <p> {{ room.price }}원</p>
  </div>
   
  
</template>

<script>
import oneRoomList from './assets/data/oneRoom.js';

export default {
  name: 'App',
  // 데이터 보관함 - state 라고 부름
  data(){
    return {
      oneRoom : oneRoomList,
      modalOpen : false,
      rpCnt : [0,0,0],
      products : ['역삼동원룸', '천호동원룸', '마포구원룸'],
      menu : ['Home', '아파트', '빌라/주택', '원룸'],
    }
  },
  methods : {
    clcickReport(){
      
    }
  },
  components: {
  }
}
/* 데이터 바인딩 
   데이터 값   {{ 데이터 이름 }}
   속성        :속성="데이터 이름"
*/
</script>

<style>
body {
  margin: 0;
}
div {
  box-sizing: border-box;
}
.black-bg {
  width: 100%; height: 100%;
  background-color:rgba(0, 0, 0, 0.5);
  position: fixed; 
  padding: 20px;
}
.white-bg {
  width: 100%;
  background-color: white;
  border-radius: 8px;
  padding: 20px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}

.menu a {
  color:white;
  padding: 10px;
  cursor: pointer;
}

.room-img {
  width:60%;
  margin-top: 40px;
}
</style>
