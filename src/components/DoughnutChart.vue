
  <script lang="ts">
  import { Chart as ChartJS, ArcElement, Tooltip, Legend } from 'chart.js'
  import { Doughnut } from 'vue-chartjs'
  import * as chartConfig from './doughConfig.js'
  
  ChartJS.register(ArcElement, Tooltip, Legend)
  
  export default {
    name: 'App',
    components: {
      Doughnut
    },
    data() {
      return chartConfig
    }
  }
  </script>
  

  <template>
    <div id="container">
      <div id="sold">
        <p>Most Sold Items</p>
        <button>...</button>
      </div>
      <div>
        <Doughnut :data="data" :options="options" id="dough"/>
      </div>
    </div>
    
  </template>
  

  <style scoped>
    #container {
      display: flex;
      flex-direction: column;
      border: 1px solid lightgray;
      border-radius: 10px;
      flex: 1;
      margin: 5px;
      margin-left: -5px;
    }
    #sold {
      display: flex;
      justify-content: space-between;
      padding: 10px;
    }

    #sold p {
      font-weight: 700;
      font-size: large;
    }

    #sold button {
      border: none;
      padding:5px;
      border-radius: 5px;
      width: 40px;
      font-size: large;
    }
  </style>