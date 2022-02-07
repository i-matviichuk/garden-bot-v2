<template>
  <div>
    <div v-for="(timesheet, id) in timesheets" :key="id" class="timesheet">
      <div class="date-row">
        <div class="date">{{ timesheet.date }}</div>
        <div class="date">Day</div>
      </div>
      <!--    <v-card>rgigig</v-card>-->
      <div class="address"><h4>{{ timesheet.address }}</h4></div>
      <div class="crew-hours">
        <table id="employees">
          <tr>
            <th>Name</th>
            <th>Start time</th>
            <th>End time</th>
            <th>Total hours</th>
          </tr>
          <tr>
            <td>John Doe</td>
            <td>8:00am</td>
            <td>10:00am</td>
            <td>2 hours</td>
          </tr>
          <tr>
            <td>Johanna Doe</td>
            <td>8:00am</td>
            <td>10:00am</td>
            <td>2 hours</td>
          </tr>
          <tr>
            <td>John Doe</td>
            <td>8:00am</td>
            <td>10:00am</td>
            <td>2 hours</td>
          </tr>
        </table>
        <!--      <div>Crew Hours</div>-->
        <!--      <div class="crew-member">-->
        <!--        <div>John Doe</div>-->
        <!--        <div>8:00am</div>-->
        <!--        <div>10:00am</div>-->
        <!--        <div>2 hours</div>-->
        <!--      </div>-->
      </div>
      <div class="info-row">
        <table>
          <tr>
            <th>Notes</th>
            <th>Materials</th>
          </tr>
          <tr>
            <td class="note">{{ timesheet.note }}</td>
            <td class="materials">{{ timesheet.note }}</td>
          </tr>
        </table>
        <!--      <div class="note">{{ timesheet.note }}</div>-->
        <!--      <div class="materials">{{ timesheet.note }}</div>-->
      </div>
    </div>
  </div>
</template>

<script>
import timesheetsData from '../data.json'

export default {
  data () {
    return {
      timesheets: timesheetsData.timesheets
    }
  }
}
</script>

<style>
  .timesheet {
    display: flex;
    flex-direction: column;
    /*min-width: 30%;*/
    max-width: 40%;
    margin: 0 5px 15px 5px;
    padding: 10px;
    border: 2px solid #44b984;;
    border-radius: 5px;
  }
  .date-row {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  /*.date {*/
  /*  text-align: right;*/
  /*}*/
  .address {
    /*text-align: left;*/
    font-size: 16pt;
    /*margin-left: 10px;*/
    /*margin-bottom: 22px;*/
  }
  .crew-hours {
    display: flex;
    flex-direction: column;
  }
  #employees {
    font-family: Arial, Helvetica, sans-serif;
    border-collapse: collapse;
    width: 100%;
  }
  #employees td, #employees th {
    border: 1px solid #ddd;
    padding: 8px;
  }
  #employees tr:nth-child(even){background-color: #f2f2f2;}
  #employees tr:hover {background-color: #ddd;}
  #employees th {
    padding-top: 12px;
    padding-bottom: 12px;
    text-align: left;
    background-color: #04AA6D;
    color: white;
  }
  .crew-member {
    display: flex;
    justify-content: space-between;
  }
  .info-row {
    display: flex;
    justify-content: space-between;
  }
  .note {
    width: 50%;
    margin-right: 10px;
  }
  .materials {
    width: 50%;
    margin-left: 10px;
  }
</style>
