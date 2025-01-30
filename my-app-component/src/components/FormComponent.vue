<template>
  <form>
    <div class="form-control">
      <label for="emp-name">ชื่อพนักงาน</label>
      <input type="text" v-model.trim="employee.name"/>
    </div>
    <div class="form-control">
      <label for="emp-salary">เงินเดือน</label>
      <input type="number" v-model="employee.salary"/>
    </div>
    <div class="form-control">
      <label for="department">ตำแหน่งงาน</label>
      <select v-model="employee.department">
        <option value="ฝ่ายการตลาด">ฝ่ายการตลาด</option>
        <option value="ฝ่ายการเงิน">ฝ่ายการเงิน</option>
        <option value="ฝ่ายขาย">ฝ่ายขาย</option>
      </select>
    </div>
    <div class="form-control">
      <h2>เพศ</h2>
      <div>
        <input type="radio" value="ชาย" v-model="employee.gender"/>
        <label for="gender-name">เพศชาย</label>
      </div>
      <div>
        <input type="radio" value="หญิง" v-model="employee.gender"/>
        <label for="gender-name">เพศหญิง</label>
      </div>
    </div>
    <div>
      <button type="submit">บันทึกข้อมูล</button>
    </div>
    {{ JSON.stringify(employee) }}
  </form>
</template>

<script>
export default {
    name:"FormComponent",
    data(){
        return{
          employee:{
            name:"",
            salary:0,
            department:"่ฝ่ายการตลาด",
            gender:""
          }
        }
    }
}
</script>

<style scoped>
form{
  margin: 2rem auto;
  max-width: 40rem;
  border-radius: 12px;
  box-shadow: 0 2px 10px rgba(0, 0, 0,0.25);
  padding:2rem;
  background: white;
}
.form-control{
  font-weight: bold;
}
label{
  font-weight: bold;
}
input,select{
  display: block;
  width: 100%;
  font:inherit;
  margin-top: 5px;
}
button{
  font:inherit;
  background: rgb(177, 11, 135);
  color: white;
  cursor: pointer;
  padding: 0.5rem 1rem;
  margin-top: 10px;
  border-radius: 15px;
}
input[type="radio"]{
  display: inline-block;
  width: auto;
  margin-right: 1rem;
}
input[type="radio"]+label{
  font-weight: normal;
}
h2{
  font-size: 1rem;
  margin: 0.5rem 0;
}
</style>