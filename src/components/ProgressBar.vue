<script setup>

  data({
    percentage: String,
    required: true
  })

  method:{
    progress:()=>{
      var p = this.percentage;
      var off = -51 -((51/100)*p);
      new TweenMax.to('stat-circle', .4, {
        strokeDashoffset: off
      });
    }
  }
</script>


<template>
  <div is="vue:stat-circle" :percentage="10"></div>
</template>