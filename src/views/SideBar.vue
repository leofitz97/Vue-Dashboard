<script setup>
  import { RouterLink } from 'vue-router'
</script>

<template>
  <div id="sidebar">
    <div id="sidebar-top">
      <nav>
        <img src="../components/icons/dashboard24.png" alt="dashboard icon"/>
        <RouterLink to="/ui/dashboard">Dashboard</RouterLink>
      </nav>
      <nav>
        <img src="../components/icons/charts24.png" alt="statistics icon"/>
        <RouterLink to="/statistics">Statistics</RouterLink>
      </nav>
      <nav>
        <RouterLink to="/payment">Payment</RouterLink>
      </nav>
      <nav>
        <RouterLink to="/transaction">Transactions</RouterLink>
      </nav>
      <nav>
        <RouterLink to="/product">Products</RouterLink>
      </nav>
      <nav>
        <RouterLink to="/customer">Customer</RouterLink>
      </nav>
      <nav>
        <RouterLink to="/messages">Messages</RouterLink>
      </nav>
    </div>
    <div id="sidebar-bottom">
      <nav>
        <RouterLink to="/settings">Settings</RouterLink>
      </nav>
      <nav>
        <RouterLink to="/logout">Logout</RouterLink>
      </nav>
    </div>
  </div>
</template>


<style scoped>
  #sidebar {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    padding:10px
  }

  #sidebar-top nav{
    margin-bottom: 1rem;
    font-size: large;
  }

  #sidebar-top nav a {
    padding: 10px;
    text-decoration: none;
    width: 180px; 
    color: gray;
  }

  #sidebar-top nav img {
    vertical-align: middle;
  }

  #sidebar-top nav:hover {
    background-color: blue;
    /* color: red; */
    border-radius: 10px;
  }

  #sidebar-top a {
    width: 180px;
  }

  /* #sidebar-top a:hover {
    background-color: blue;
    color: white;
    border-radius: 10px;
  } */

  #sidebar-top img {
    color: white;
  }

  @media (min-width: 1024px) {
    #sidebar-top nav {
      width: 180px;
    }

    #sidebar-top nav a {
      width: 180px;  
    }
  }
</style>