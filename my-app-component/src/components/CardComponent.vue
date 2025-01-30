<template>
  <li>
    <img src="https://cdn-icons-png.flaticon.com/128/547/547413.png"/>
    <hr/>
    <slot></slot>
  </li>
</template>

<script>

export default {

}
</script>

<style scoped>
  li{
    margin:1rem 0;
    font-size: 1.25rem;
    font-weight: bold;
    background-color: rgb(240, 134, 213);
    padding: 0.5rem;
    color: #ffffff;
    border-radius: 25px;
}
img{
  widows: 150px;
  height: 150px;
}

</style>