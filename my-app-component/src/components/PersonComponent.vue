<template>
  <div>
    <h1>{{ message }}</h1>
  </div>
</template>

<script>
export default {
    name:"PersonComponent",
    data(){
        return{
            message:"ข้อมูลพนักงาน"
        }
    }
}
</script>

<style scoped>
  h1{
    color: red;
  }
</style>