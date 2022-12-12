<template lang="">
    
  <h2 class="modal" v-if="modal">
    <div class="modalback">
      <div>{{Rooms[selected].title}}</div>
      <div>{{Rooms[selected].content}}</div>
      <span style="color: red">최소 3개월부터 계약가능!!</span>
      <br>
      <input type="number" v-model="value">
      <div>{{Rooms[selected].price * this.value}}won</div>
      <button @click="$emit('close')">Close</button>
  </div>
  </h2>
</template>
<script>
export default {
    props: {
        Rooms: Array,
        modal: Boolean,
        selected: Number
    },
    data(){
        return{
            value: 3
        }
    },
    watch: {
        value(){
            if(this.value <= 2){
                alert("3개월부터라고 돈없냐??")
                this.value = 3
            }
        }
    }
  
}
</script>
<style lang="">
    
</style>