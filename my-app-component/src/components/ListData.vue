<template>
    <div>
        <ul>
            <li>
                
            </li>
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
    //รับค่า props
    props:["employees"]
  }

</script>

<style>

</style>