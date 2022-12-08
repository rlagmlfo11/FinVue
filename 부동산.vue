<template>
<div id="container">

<div class="black-bg" v-if="(모달창열렸니 == true)">
  <div class="white-bg">
    <h4>상세페이지임</h4>
    <p>상세페이지내용임</p>
    <button @click="(this.모달창열렸니 =flase)">닫기</button>
  </div>
</div>



<div class="menu">
  <a class="a" v-for="(menu,i) in 메뉴들" :key="i">{{menu}}</a>
</div>

<div v-for="원룸 in 원룸들" :key="원룸">
  <img :src="원룸.image" class="room-img" alt="">
  <h4>{{원룸.title}}</h4>
  <p>{{원룸.price}}</p>
  <p>{{원룸.content}}</p>
</div>



</div>
</template>


<script>
import oneroom from "./components/oneroom.js"

export default {
  name: "app",
  data(){
    return{
      원룸들: oneroom,
      모달창열렸니: false,
      신고수: [0,0,0],
      메뉴들: ["Home", "Shop", "About"],
      products: ["역삼동원룸", "천호동원룸", "마포구원룸"]
    }
  },

  
}
</script>


<style>
body{
  margin: 0;
}
div{
  box-sizing: border-box;
}
.black-bg{
  width: 100%;
  height: 100%;
  background-color: rgba(0,0,0,0.5);
  position: fixed; padding: 20px;
}
.white-bg{
  width: 100%;
  background-color: white;
  border-radius: 8px;
  padding: 20px;
}



#container{
  text-align: center;
}

.menu{
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}

.a{
  color: white;
  padding: 10px;
}
.room-img{
  width: 100%;
  margin-top: 40px;
  height: 200px;
}
</style>