<template>
  <ul>
    <PersonComponent
      v-for="(item,index) in employees"
      :key="index"
      :name="item.name"
      :salary="item.salary"
      :department="item.department"
      :gender="item.gender"
      :skill="item.skill"
    />
  </ul>
</template>

<script>
import PersonComponent from './PersonComponent.vue';

export default {
    name:"ListData",
    components:{
        PersonComponent
    },
    props:["employees"]
}

</script>

<style scoped>
ul {
  list-style: none;
  margin: 1rem 0;
  padding: 0;
}
</style>
