<script setup>
  import Card from '../components/Card.vue'
  import BarChart from '../components/BarChart.vue';
  import DoughnutChart from '../components/DoughnutChart.vue'
  import Table from '../components/Table.vue'
</script>

<template>
  <div id="dashboard">
    <div id="dashboard-top">
      <Card header="Todays Sales" amount="$20.4K" details="We have sold 123 items">
        <template #chart>
          
        </template>
      </Card>
      <Card header="Todays Sales" amount="$20.4K" details="We have sold 123 items">
        <template #chart>
          
        </template>
      </Card>
      <Card header="Todays Sales" amount="$20.4K" details="We have sold 123 items">
        <template #chart>
          
        </template>
      </Card>
    </div>
    <div id="dashboard-middle">
      <BarChart />
      <DoughnutChart />
    </div>
    <div>
      <Table />
    </div>
  </div>
</template>


<style scoped>
  #dashboard {
    background-color: white;
    display: flex;
    flex-direction: column;
    padding: 20px
  }

  #dashboard-top {
    display: flex;
  }

  #dashboard-middle {
    display: flex;
    /* max-width: 50%; */
  }



  @media (min-width: 1024px){
    #dashboard {
      min-width: 87%;
    }

    #dashboard-middle {
      max-width: 100%;
    }
  }
</style>