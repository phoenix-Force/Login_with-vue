<template>
<div>
  <div id="on" :class ="{isactive:value}" @click="dswitch(true)">
    On
  </div>
  <div id="off" :class ="{isactive:!value}" @click="dswitch(false)">
    Off
  </div>

</div>

</template>
<script>
export default {
 props:['value'],
 methods:{
   dswitch(isOn){
     this.$emit('input',isOn)
   }

 }

}
</script>
<style scoped>
#on,#off{
  height:20px;
  width:40px;
  float:left;
  background-color: lightgray;
  cursor: pointer;
  text-align: center;


}
#on.isactive,#on:hover{
  color:white;
  background-color: lightgreen;
}
#off.isactive,#off:hover{
  color:white;
  background-color: lightcoral;
}
</style>
