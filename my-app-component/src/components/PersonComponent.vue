<template>
  <CardComponent>
    <template v-slot:card-header>
      <h1>{{ name }}</h1>
    </template>
    <template v-slot:card-content>
          <p>เพศ : {{ gender }}</p>
          <p>ตำแหน่งงาน : {{ department }} เงินเดือน : {{ salary }} บาท</p>
          <p>ภาษา : {{ skill }}</p>
    </template>
  </CardComponent>
</template>

<script>
import CardComponent from './CardComponent.vue';

export default {
    name:"PersonComponent",
    components:{
        CardComponent
    },
    // รับค่า props name
    props:{
      id:{
        type:Number
      },
      name:{
        type:String,
        required:true
      },
      salary:{
        type:Number,
        //salary
        default:15000
      },
      department:{
        type:String,
        required:true
      },
      gender:{
        type:String,
        required:true
      },
      skill:{
        type:Array,
      },
      isVisible:{
        type:Boolean
      }
    }
}
</script>

<style scoped>

button{
  font:inherit;
  cursor: pointer;
  border: 1px solid #ff0077;
  background: #ff0077;
  color: white;
  padding: 0.05rem 1rem;
  box-shadow: 1px 1px 2px rgba(0,0,0,0.26);
}
.fade-enter-from{
  opacity: 0;
}
.fade-enter-active{
  transition: all 0.5s linear;
}
</style>