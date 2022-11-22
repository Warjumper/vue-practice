<template>
  <header>
    <h1>{{ title }}</h1>
    <TrackerButton text="Add Task" color="green" />
  </header>
</template>


<script>
import TrackerButton from './TrackerButton.vue'

export default {
  name: 'TrackerHeader',
  props: {
    title: String,
  },

  components: {
  TrackerButton
  }
}
</script>

<style scoped>
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
  }
</style>