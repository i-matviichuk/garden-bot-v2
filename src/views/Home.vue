<template>
  <div class="home">
    <h1>Home</h1>
    <AddTimesheet/>
  </div>
</template>

<script>
import AddTimesheet from '@/components/AddTimesheet.vue'
export default {
  name: 'Home',

  components: {
    AddTimesheet
  }
}
</script>
