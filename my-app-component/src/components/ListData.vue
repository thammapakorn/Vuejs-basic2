<template>
    <div>
        <h1>{{ message }}</h1>
        <!-- ถ้าอยากเรียกใช้หลายๆอันก็ เรียกใช้บ่อยๆนะ -->
        <PersonComponent/>
        <PersonComponent/>
        <PersonComponent/>
        <PersonComponent/>
        
    </div>
</template>

<script>
import PersonComponent from './PersonComponent.vue';

export default {
    name:"ListData",
    components:{
        PersonComponent
    },
    data(){
        return{
            message:"แสดงรายชื่อพนักงานทุกคน"
        }
    }
  }

</script>

<style>

</style>