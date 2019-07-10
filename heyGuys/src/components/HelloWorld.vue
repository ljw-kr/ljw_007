<template>
 <div class="bx">
  <el-tabs v-model="activeName" @tab-click="handleClick">
    <el-tab-pane label="广外" name="first"><School></School></el-tab-pane>
    <el-tab-pane label="广工" name="second"><manage></manage></el-tab-pane>
    <el-tab-pane label="广大" name="third"><query></query></el-tab-pane>
    <el-tab-pane label="中大" name="fourth"><score></score></el-tab-pane>
  </el-tabs>
 </div>
</template>
<script>
import School from '@/components/School'
import manage from '@/components/manage'
import query from '@/components/query'
import score from '@/components/score'
export default {
  data () {
    return {
      activeName: 'second'
    }
  },
  components: {School, manage, query, score},
  methods: {
    handleClick (tab, event) {
      // console.log(tab, event)
    }
  }
}
</script>
<style scope>
   .bx {
     width: 500px;
     height: 150px;
     margin: 0 auto;
   }
</style>
