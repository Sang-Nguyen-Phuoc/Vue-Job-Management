<script>
export default {
  data() {
    return {
      name: 'John Doe',
      status: 'pending',
      tasks: [
        { id: 1, title: 'Task One', completed: false },
        { id: 2, title: 'Task Two', completed: true },
        { id: 3, title: 'Task Three', completed: false }
      ],
      link: 'https://www.google.com'
    }
  },
  methods: {
    toggleStatus() {
      if (this.status === 'active') {
        this.status = 'pending'
      } else if (this.status === 'pending') {
        this.status = 'inactive'
      } else {
        this.status = 'active'
      }
    }
  },
}
</script>

<template>
  <h1>Vue creash course</h1>
  <p>{{ name }}</p>
  <!-- // Binding attributes
    -->
  <p v-if="status === 'active'">User is active</p>
  <p v-else-if="status === 'pending'">User is pending</p>
  <p v-else>User is not active</p>

  <!-- // Looping through tasks -->
  <h3>Tasks: </h3>
  <ul>
    <li v-for="task in tasks" :key="task.id">
      {{ task.title }}
    </li>
  </ul>

  <!-- // Link binding -->
  <a :href="link">Google</a>

  <!-- // Event handling -->
  <br />
  <button @click="toggleStatus()">Toggle</button>

</template>

<style scoped></style>
