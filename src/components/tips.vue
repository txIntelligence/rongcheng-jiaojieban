<template>
  <div class="tips-wrap" v-if="visible">
      <div class="tip fail">
        <span>{{msg}}</span>
        <i class="shibai"></i>
      </div>
  </div>
</template>

<script>
  export default {
    name: "tips",
    data(){
      return {

      }
    },
    props:{
      msg:{
        type:String,
        default:'暂无相关数据'
      },
      visible:{
        type:Boolean,
        default:true
      }
    }
  }
</script>

<style scoped>
  .tips-wrap{
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
  }
  .tips-wrap .success{
    background-color: rgba(25,190,107,0.7);
  }
  .tips-wrap .fail{
    background-color: rgba(255,45,11,0.7);
  }

  .tips-wrap .tip{
    display: flex;
    justify-content: flex-start;
    align-items: center;
    /*animation: fadeIn 8s linear infinite;*/
  }

  /*@keyframes fadeIn {*/
    /*0% { opacity: 1;}*/
    /*!*10% { opacity: .8;}*!*/
    /*!*50% { opacity: .6;}*!*/
    /*!*60% { opacity: .4;}*!*/
    /*!*90% { opacity: .2;}*!*/
    /*100% { opacity: 0;}*/
  /*}*/

  .tips-wrap .tip span{
    padding: 0.1rem 0.12rem;
    font-size:0.14rem;
    color:#ffffff;
  }
  .tips-wrap .tip i{
    display: inline-block;
    width: 0.14rem;
    height: 0.14rem;
  }
  .tips-wrap .tip .shibai{
    background: url("../assets/shibai.png") no-repeat;
    background-size: contain;
  }

</style>
