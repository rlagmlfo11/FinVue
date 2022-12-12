<template lang="">
  
  <modal 
  :selected="selected" 
  :modal="modal" 
  :Rooms="Rooms"
  @close="this.modal=false">
  </modal>

  <Title :titles="titles"></Title>

  <discount :discount="discount"></discount>

  <list 
  :Rooms="Rooms"
  :selected="selected"
  @modalopen="this.modal=true, selected=$event">
  </list>

</template>



<script>
import data from "./components/data";
import Title from "./components/title.vue";
import discount from "./components/discount.vue"
import modal from "./components/modal.vue"
import list from "./components/list.vue"

export default {
  components: {
    Title,
    discount,
    modal,
    list
  },
  data(){
    return{
      selected: 0,
      modal: false,
      discount: 30,
      Rooms: data,
      titles: ["Home", "Girls", "About"]
    }
  }  
}
</script>



<style>

.modal{
  background-color: rgba(0, 0, 0, 0.5);
  width: 100%;
  height: 100%;
  position: fixed;
  color: black;
  margin-top: 0;
  padding-top: 100px;
}
.modalback{
  background-color: white;
  padding: 40px;
  }

body{
  text-align: center;
  margin: 0%;
}  
.title{
  background-color: darkslateblue;
  padding: 20px;
  color: white;
  margin-top: 0;
}
.title a{
  padding: 20px
}
.image{
  width: 400px;
  height: 400ox;
}



@import url("https://fonts.googleapis.com/css2?family=Itim&display=swap");

html,
body {
  font-family: "Itim", cursive;
}
#app {
  font-family: "Itim", cursive;
}
</style>