<template>
  <div>
    <FormComponent/>
    <ListData :employees="employees" />
</div>
</template>

<script>
import FormComponent from './components/FormComponent.vue';
import ListData from './components/ListData.vue';
export default{
  name:"App",
  components:{
    ListData,
    FormComponent
  },
  data(){
    return{
      employees:[
        {name:"เปรม",salary:30000},
        {name:"จูน",salary:60000},
        {name:"ก้อง",salary:40000},
        {name:"โจ๊ก",salary:30000},
        {name:"ตุ๊ก",salary:50000},
        {name:"มิ๊ก"}
      ]
    }
  }
}
</script>

<style>

</style>