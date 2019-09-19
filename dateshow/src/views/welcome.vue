<template>
    <div class="welcome">
        <div class="title"> 基于web的数据可视化系统实现 </div>
   <router-link to="/index">
    <div class="enter">点击进入系统</div>
   </router-link>
   
    </div>
</template>

<script>
    export default {
        name:"wel"
    }
</script>

<style lang="scss" scoped>
.welcome{
    margin: auto auto;
    .title{
        font-size: 30px;}
.enter{
        font-size: 24px;
        color: #fff;
    }

}
    
</style>