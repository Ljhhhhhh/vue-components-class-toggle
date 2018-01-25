<template>
  <div>
    <p @click="hide">hello</p>
    <comp :showValue="showValue" @hideClick="hide" :class="{big1:isbig,small1:issmall}"></comp>
    <el-button type="success" @click="go" :class="{big:isbig,small:issmall}">BTN</el-button>
  </div>
</template>
<script>
  import comp from './comp'
  export default {
    data(){
      return {
        showValue:true,
        isbig:true,
        issmall:false
      }
    },
    components:{
      comp
    },
    methods:{
      hide(){
        this.isbig=!this.isbig
        this.issmall=!this.issmall
      },
      go(){
        this.isbig=!this.isbig
        this.issmall=!this.issmall
      }
    }
  }
</script>
<style lang="less" scoped>
  .big{
    font-size: 40px;
    color: yellow;
  }
  .small{
    font-size: 12px;
    color: red;
  }
  .big1{
    width: 500px;
    height: 500px;
    line-height: 500px;
  }
  .small1{
    width: 50px;
    height: 50px;
    line-height: 50px;
  }
</style>
