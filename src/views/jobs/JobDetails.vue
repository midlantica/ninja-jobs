<template>
  <h1>Job Details</h1>
  <div v-for="job in jobs" :key="job.id">
    <h2>{{ job.title }}</h2>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        jobs: [
          { title: 'Ninja UX Designer', id: 1, details: 'lorem 01' },
          { title: 'Ninja UI Engineer', id: 2, details: 'lorem 02' },
          { title: 'Ninja Front-End Dev', id: 3, details: 'lorem 03' },
        ]
      }
    }
  }
</script>

<style>

</style>
