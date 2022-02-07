<template>
  <div class="sidebar">
    <div>
      <router-link to="/"><div class="router-link">Home</div></router-link>
    </div>
    <div>
      <router-link to="/timesheets"><div class="router-link">Timesheets</div></router-link>
    </div>
  </div>
</template>

<style>
  .sidebar {
    flex-direction: column;
    align-items: flex-start;
    justify-content: space-around;
  }
  .router-link {
    margin: 10px 0 10px 0;
    padding: 10px;
    border: 2px solid #44b984;
    border-radius: 5px;
  }
</style>
