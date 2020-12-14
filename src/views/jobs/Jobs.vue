<template>
  <h1>Jobs</h1>
  <div v-for="job in jobs" :key="job.id" class="job">
    <router-link :to="{ name: 'JobDetails', params: { id: job.id } }">
      <h4>{{ job.title }}</h4>
    </router-link>
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
  .job h4 {
    background: #f4f4f4;
    padding: 20px;
    border-radius: 10px;
    margin: 10px auto;
    max-width: 400px;
    cursor: pointer;
    color: #444;
  }

  .job h4:hover {
    background: #ddd;
  }

  .job a {
    text-decoration: none;
  }
</style>
