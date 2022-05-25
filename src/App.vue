<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div>
    <h4>{{ products[0] }}</h4>
    <p>70 만원</p>
  </div>
   <div>
    <h4>{{ products[1] }}</h4>
    <p>40 만원</p>
  </div>
   <div>
    <h4>{{ products[2] }}</h4>
    <p>50 만원</p>
  </div>
  
</template>

<script>

export default {
  name: 'App',
  // 데이터 보관함
  data(){
    return {
      products : ['역삼동원룸', '천호동원룸', '마포구원룸'],
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
  margin-top: 60px;
}
</style>
