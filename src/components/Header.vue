<template>
  <header>
    <h1>{{ title }}</h1>
    <Button @toggle-form="$emit('toggle-form')" text="Add text" color="green"/>
    <!-- <Button text="Update text" color="orange"/>
    <Button text="Delete text" color="red"/> -->
  </header>
</template>

<script>
import Button from './Button.vue'

export default {
  name: 'Header',
  props: {
    title: {
      type: String,
      default: 'Task Tracker',
    }
  },
  components: {
    Button
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

