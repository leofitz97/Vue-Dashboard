<script setup>

defineProps({
  header: {
    type: String,
    required: true
  },
  amount:{
    type: String,
    required: true
  },
  details:{
    type: String,
    required: true
  }
}) 


</script>


<template>
  <div id="card">
    <div id="card-main-body">
      <p id="card-head">{{ header }}</p>
      <p id="card-amount">{{ amount }}</p>
      <p id="card-details">{{ details }}</p>
    </div>
    <div id="card-charts">
      <slot name="chart"></slot>
    </div>
  </div>
</template>


<style scoped>
  #card {
    display: flex;
    flex:1;
    align-items: center;
    border: 1px solid black;
    padding: 2rem;
    height: 10rem;
    border-radius: 10px;
    border-color: lightgray;
    margin: 10px;
  }

  #card-head {
    font-weight: 600;
    font-size: large;
  }

  #card-amount {
    font-weight: 900;
    font-size: x-large;
  }

  #card-details {
    margin-top: 5px;
    color: gray;
  }

  #card-charts {
    display: flex;
    justify-content: center;
  }

  .progress-circle {
    width: 8rem;
    height: 8rem;
    border: 5px solid lightgray;
    border-radius: 5rem;
  }

  .progress {
    width: 8rem;
    height: 8rem;
    border: 5px solid lightgray;
    /* border-radius: 5rem; */
  }


  @media (min-width: 1024px){
    #card {
      min-width: 10rem;
    }
  }
</style>