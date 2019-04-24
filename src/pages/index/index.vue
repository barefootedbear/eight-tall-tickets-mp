<template>
  <div class="body">
    <div class="ticket-container">
      <div style="color:red; padding-top:10px;">发现好货</div>
      <div style="margin-top: 10px;">
        <div v-for="ticket in tickets" v-bind:key="ticket" class="scale-1px">
          {{ticket + 1}}
        </div>
      </div>
    </div>  
  </div>
</template>

<script>
import card from '@/components/card'

export default {
  data () {
    return {
      tickets: ['1', '2', '3', '5', '6', '7']   
    }
  }
}
</script>

<style scoped>
  .body{
    background-color: rgb(243, 240, 240);
  }
  .ticket-container{
    margin: 10px
  }
  .scale-1px{
    position: relative;
    margin-bottom: 15px;
    border:none;
    height: 200px;
    background-color: white;
  }
  .scale-1px:after{
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    border: 1px solid rgb(235, 231, 231);
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
    width: 200%;
    height: 200%;
    -webkit-transform: scale(0.5);
    transform: scale(0.5);
    -webkit-transform-origin: left top;
    transform-origin: left top;
  }
</style>
