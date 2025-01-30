<template>
  <CardComponent>
    <h1>{{ name }}</h1>
    <button @click="showDescription(id)">ดูรายละเอียด</button> &nbsp;
    <button @click="deleteEmployees(id)">ลบข้อมูล</button>
    <transition name="fade">
      <div v-show="isVisible">
        <p>เงินเดือน : {{ salary }} บาท ตำแหน่งงาน : {{ department }}</p>
      </div>
    </transition>
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
      isVisible:{
        type:Boolean
      }
    },
    methods:{
      showDescription(id){
        //ใช้ emit ส่งสัญญานไปหาแม่ event ชื่อ show โดยส่งข้อมูล id ไปด้วย
        this.$emit("show",id);
      },
      deleteEmployees(id){
        this.$emit("delete",id);
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