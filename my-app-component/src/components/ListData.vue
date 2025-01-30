<template>
  <ul>
    <PersonComponent
      v-for="item in employees"
      :id="item.id"
      :key="item.id"
      :name="item.name"
      :salary="item.salary"
      :department="item.department"
      :isVisible="item.isVisible"
      @show="toggleVisible"
      @delete="removeEmployee"
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
    data(){
    return{
      employees:[
        { id:1,name:"เปรม ตั้งใจ",salary:30000,department:"IT Support",isVisible:false},
        { id:2,name:"จูน เก่งมาก",salary:60000,department:"Sales Admin",isVisible:false},
        { id:3,name:"ก้อง เก่งมาก",salary:40000,department:"Programmer",isVisible:false},
        { id:4,name:"โจ๊ก หล่อ",salary:30000,department:"Programmer",isVisible:false},
        { id:5,name:"ตุ๊ก ขยัน",salary:50000,department:"SA IT",isVisible:false},
        { id:6,name:"มิ๊ก กี้",department:"HR",isVisible:false}
        ] 
    }
    },
    methods:{
        toggleVisible(emp_id){
            this.employees = this.employees.map((item)=>{
                if(item.id === emp_id){
                    return {...item,isVisible:!item.isVisible}
                }
                return item;
            })        
        },
        removeEmployee(emp_id){
            this.employees =this.employees.filter(item=>{
            //item ที่มี id ไม่ตรงกันกับ id อื่น จะคงสภาพสมาชิกเอาไว้ 
            //เช่น ได้ emp_id = 3 มา ค่าอื่นที่ไม่ใช่ 3 ก็จะคงสภาพเอาไว้ ถ้าเป้น 3 ก็ลบ
                return item.id !== emp_id
                })
            }
        }
}


</script>

<style scoped>
ul {
  list-style: none;
  margin: 1rem 0;
  padding: 0;
}
</style>
