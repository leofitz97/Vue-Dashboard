
  <script>
  import {
    Chart as ChartJS,
    Title,
    Tooltip,
    Legend,
    BarElement,
    CategoryScale,
    LinearScale
  } from 'chart.js'
  import { Bar } from 'vue-chartjs'
  import * as chartConfig from './barConfig.js'
  
  ChartJS.register(CategoryScale, LinearScale, BarElement, Title, Tooltip, Legend)
  
  export default {
  name: 'BarChart',
  components: {
    Bar
  },
  data() {
    return chartConfig
  }
}

  </script>
  
  <template>
    <div id="container">
      <div id="container-top">
        <h2>Total Revenue</h2>
        <div id="updates">
          <p>Data Updates Every 3 Hours</p>
          <button>View All Orders</button>
        </div>
      </div>
      <div id="detail">
        <p id="money">$50.4K</p>
        <P id="percentage">8% than last month</P>
      </div>
      <div id="bar-container">
        <Bar :data="data" :options="options" id="bar"/>
      </div>
    </div>
    
  </template>


<style scoped>
  #container {
    display: flex;
    flex-direction: column;
    flex: 2;
    width: 20rem;
    border: 1px solid lightgray;
    border-radius: 10px;
    margin: 10px;
    margin-right: 20px;
  }
  #bar {
    height: 100%;
  }
  #bar-container {
    height: 100%;
  }
  #container-top {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        margin: 10px;
        
    }
    #container-top h2 {
      font-weight: 700;
    }
    #updates {
        display: flex;
    }
    #updates button {
        background-color: blue;
        border-radius: 5px;
        padding: 10px;
        outline: none;
        color: white;
        font-weight: 600;
    }
    #updates p {
        color: gray;
        margin-right: 10px;
    }

    #detail {
      display: flex;
      margin-left: 10px;
    }

    #detail #money {
      font-weight: 800;
      font-size: x-large;
      margin-bottom: 0;
    }
    #detail #percentage {
      color: green;
      vertical-align: middle;
      margin-left: 10px;
      margin-bottom: 0;
    }
</style>
  