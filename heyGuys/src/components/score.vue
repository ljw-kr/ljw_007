<template>
<div>
    <span>AP课程</span>
    <hr>
    <el-progress type="circle" :percentage="25"></el-progress>
    <br>
    <span>托福</span>
    <hr>
    <el-progress type="circle" :percentage="75"></el-progress>
    <br>
    <span>雅思</span>
    <hr>
    <el-progress type="circle" :percentage="88"></el-progress>
</div>

</template>
<script>
export default {
}
</script>
<style scoped>
  span{
      /* float: left;
       */
       /* margin-left: 10px; */
  }
</style>
