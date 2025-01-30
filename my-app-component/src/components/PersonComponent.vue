<template>
  <li>
    <h1>{{ name }}</h1>
    <button>ดูรายละเอียด</button> &nbsp;
    <button>ลบข้อมูล</button>
  <div v-show="isVisible">
    <p>เงินเดือน : {{ salary }} บาท ตำแหน่งงาน : {{ department }}</p>
  </div>
  </li>
</template>

<script>
export default {
    name:"PersonComponent",
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
    }
}
</script>

<style scoped>
  li{
    margin:1rem 0;
    font-size: 1.25rem;
    font-weight: bold;
    background-color: rgb(240, 159, 134);
    padding: 0.5rem;
    color: #1f1f1f;
    border-radius: 25px;
}
button{
  font:inherit;
  cursor: pointer;
  border: 1px solid #ff0077;
  background: #ff0077;
  color: white;
  padding: 0.05rem 1rem;
  box-shadow: 1px 1px 2px rgba(0,0,0,0.26);
}
</style>