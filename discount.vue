<template lang="">

        <h2>지금 계약하면 {{discount}}% 할인임 ㅋ</h2>

</template>
<script>
export default {
    props: {
        discount: Number
    }
}
</script>
<style scoped>
h2{
    background: gray;
    color: white;
    padding: 20px;
}


</style>