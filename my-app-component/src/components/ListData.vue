<template>
    <div>
        <ul>
            <PersonComponent 
            v-for="(item,index) in employees" 
            :key="index" 
            :name="item.name" 
            :salary="item.salary" 
            />
        </ul>
    </div>
</template>

<script>
import PersonComponent from './PersonComponent.vue';

export default {
    name:"ListData",
    components:{
        PersonComponent
    },
    //รับค่า props employees จาก App component
    props:["employees"]
  }

</script>

<style>

</style>