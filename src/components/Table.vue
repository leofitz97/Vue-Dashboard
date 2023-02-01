
<script>
    import dataList from '../stores/dataList'
    
    export default {
        name:'Table',
        methods: {
            data(){
                return {
                    items: dataList
                }
            }
        }
    }
</script>



<template>
    <div id="table-container">
        <div id="container-top">
            <h2>Lastest Orders</h2>
            <div id="updates">
                <p>Data Updates Every 3 Hours</p>
                <button>View All Order</button>
            </div>
        </div>
    
        <table>
            <thead>
                <tr>
                    <td>Products</td>
                    <td>Order ID</td>
                    <td>Date</td>
                    <td>Customer name</td>
                    <td>Status</td>
                    <td>Amount</td>
                    <td>Action</td>
                </tr>
            </thead>
            <tbody>
                
                <tr v-for="data in items" :key="data.id">
                    <th scope="row">{{ data.product  }}</th>  
                    <td>{{ data.order }}</td> 
                    <td>{{ data.date }}</td>  
                    <td>{{ data.customerName }}</td>
                    <td>{{ data.status }}</td>
                    <td>{{ data.amount }}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>


<style scoped>
    table {
        /* margin-top: 10px; */
        margin: 10px;
    }

    h2 {
        font-size: large;
        font-weight: 700;
    }
    #table-container {
        border: 1px solid lightgray;
        border-radius: 10px;
        margin-top: 20px;
       
    }
    #container-top {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        margin: 10px;
        
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
</style>