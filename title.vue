<template lang="">
    <h1 class="title">
    <a class="title a" v-for="title in titles" ::key="title">
      {{title}}
    </a>

  </h1>
</template>
<script>
export default {
    props:{
        titles: String
    }
}
</script>
<style lang="">
    
</style>