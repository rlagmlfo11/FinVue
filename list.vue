<template lang="">
      <h2 v-for="room,index in Rooms" :key="index">
    <img :src="room.image" class="image">
    <p>상세정보 => <mark @click="$emit('modalopen', room.id), (selected=index)" >{{room.title}}</mark></p>
    <p>{{room.content}}</p>
    <p>{{room.price}}</p>
  </h2>
</template>
<script>
export default {
    props: {
        Rooms: Array,
        selected: Number
    }
}
</script>
<style lang="">
    
</style>