<template>
  <!-- 모달창 -->
  <div class="black-bg">
    <div class="white-bg">
      <h4></h4>
    </div>
  </div>

  <div class="menu">
    <a v-for="(menuNm, i) in menu" :key="i">{{ menuNm }}</a>
  </div>

  <div>
    <img src="./assets/img/room1.jpg" class="room-img">
    <h4>{{ products[0] }}</h4>
    <p>30 만원</p>
    <button @click="rpCnt[0]++">허위매물신고</button> <span>신고수 : {{ rpCnt[0] }}</span>
  </div>
   <div>
    <img src="./assets/img/room2.jpg" class="room-img">
    <h4>{{ products[1] }}</h4>
    <p>40 만원</p>
    <button @click="rpCnt[1]++">허위매물신고</button> <span>신고수 : {{ rpCnt[1] }}</span>
  </div>
   <div>
    <img src="./assets/img/room3.jpg" class="room-img">
    <h4>{{ products[2] }}</h4>
    <p>50 만원</p>
    <button @click="rpCnt[2]++">허위매물신고</button> <span>신고수 : {{ rpCnt[2] }}</span>
  </div>
  
</template>

<script>

export default {
  name: 'App',
  // 데이터 보관함
  data(){
    return {
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
