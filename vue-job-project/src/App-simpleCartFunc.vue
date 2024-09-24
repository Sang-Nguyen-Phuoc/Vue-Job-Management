<script setup>
import { ref, onMounted } from 'vue'

const name = ref('John Doe');
const status = ref('active');
const newTask = ref('');
const tasks = ref([
    { id: 1, title: 'Task One', completed: false },
    { id: 2, title: 'Task Two', completed: true },
    { id: 3, title: 'Task Three', completed: false }
]);

const toggleStatus = () => {
    if (status.value === 'active') {
        status.value = 'pending'
    } else if (status.value === 'pending') {
        status.value = 'inactive'
    } else {
        status.value = 'active'
    }
}

const addTask = () => {
    if (!newTask.value) return;
    tasks.value.push({
        id: tasks.value.length + 1,
        title: newTask.value,
        completed: false
    });
    newTask.value = '';
};

const deleteTask = (id) => {
    tasks.value = tasks.value.filter((task) => task.id !== id);
};

// Fetch data from API
onMounted(async () => {
    try {
        const res = await fetch('https://jsonplaceholder.typicode.com/todos');
        const data = await res.json();
        tasks.value = data;
    } catch (err) {
        console.log(err);
    }
});

</script>

<template>
    <h1>Vue creash course</h1>
    <p>{{ name }}</p>
    <!-- // Binding attributes
    -->
    <p v-if="status === 'active'">User is active</p>
    <p v-else-if="status === 'pending'">User is pending</p>
    <p v-else>User is not active</p>

    <!-- form submit -->
    <form @submit.prevent="addTask">
        <label for="newTask">add Task</label>
        <input type="text" id="newTask" v-model="newTask" />
        <button type="submit">submit</button>
    </form>
    <!-- // Looping through tasks -->
    <h3>Tasks: </h3>
    <ul>
        <li v-for="task in tasks" :key="task.id">
            <span>
                {{ task.title }}
            </span>
            <button @click="deleteTask(task.id)">X</button>
        </li>
    </ul>

    <!-- // Event handling -->
    <br />
    <button @click="toggleStatus()">Toggle</button>

</template>

<style scoped></style>
