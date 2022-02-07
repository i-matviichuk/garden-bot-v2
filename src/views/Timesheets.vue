<template>
  <div class="timesheet-list">
    <div>
      <h1>Timesheets</h1>
    </div>
    <div class="timesheet-container">
      <Timesheet/>
    </div>
  </div>
</template>

<script>
import Timesheet from '@/components/Timesheet'

export default {
  name: 'Timesheets',
  components: {
    Timesheet
  }
}
</script>

<style>
  .timesheet-list {
    display: flex;
    flex-direction: column;
    align-self: center;
    /*text-align: center;*/
    padding: 0 15px 0 15px;
  }
  .timesheet-container {
    display: flex;
    flex-wrap: wrap;
    /*flex-direction: column;*/
    align-items: center;
  }
</style>
