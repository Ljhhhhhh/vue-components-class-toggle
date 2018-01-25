<template>
  <div class="btn" v-show="showValue" @click="hide">
    {{value}}
  </div>
</template>
<script>
  export default {
    props:['showValue'],
    data(){
      return {
        value:123
      }
    },
    methods:{
      hide(){
        this.$emit('hideClick')
      }
    }
  }
</script>
<style lang="less" scoped>
  .btn{
    background-color: aqua;
    color: #FFF;
    text-align: center;
    transition: all .1s;
  }
</style>
