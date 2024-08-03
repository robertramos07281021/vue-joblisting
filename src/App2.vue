<!--------------------------------------------------- FIRST LESSON -->

<!-- <script>
export default {
  data() {
    return {
      name: 'Robert',
      status: 'active',
      tasks: ['Task 1', 'Task 2', 'Task 3'],
      link: 'https://google.com',
    };
  },
  methods: {
    toggleStatus() {
      if(this.status === 'active') {
        this.status = 'pending';
      } else if (this.status === 'pending') {
        this.status = 'inactive';
      } else {
        this.status = 'active'
      }
    }
  }
}
</script>

<template>
  <h1>Hello {{ name }}</h1>
  <p v-if="status === 'active'"> User is active</p>
  <p v-else-if="status === 'pending'">User is pending</p>
  <p v-else>User is inactive</p>

  <h3>Tasks: </h3>
  <ul>
    <li v-for="task in tasks" :key="task">{{ task }}</li>
  </ul>
  Same only
  <a v-bind:href="link">Click for Google 1</a>
   <br>
  <a :href="link">Click for Google 2</a>
  <br>
  
  Same only
  <button v-on:click="toggleStatus">Change Status 1</button>
  <br>
  <button @click="toggleStatus">Change Status 2</button>

</template>

style format
<style scoped>
  h1 {
    color: red;
  }
</style>
 -->


<!---------------------------------------------- SECOND LESSON -->
 <!-- <script setup>
import { onMounted, ref } from 'vue';
const name = ref('Robert Ramos');
const status = ref('active');
const tasks = ref(['Task 1', 'Task 2', 'Task 3'])
const newTask = ref('');
const toggleStatus = () => {
  if(status.value === 'active') {
    status.value = 'pending';
  } else if (status.value === 'pending') {
    status.value = 'inactive';
  } else {
    status.value = 'active'
  }
}

const addTask = ()=> {
  if(newTask.value.trim() !== '') {
    tasks.value.push(newTask.value);
    newTask.value = ''
  }

}
const deleteTasks = (index) => {
  tasks.value.splice(index, 1)
}

onMounted(async() => {
  try {
    const response = await fetch('https://jsonplaceholder.typicode.com/todos')
    const data = await response.json();
    tasks.value = data.map((task) => task.title)
  } catch (error) {
    console.log('Error')
  }
});
</script>

<template>
  <h1>Hello {{ name }}</h1>
  <p v-if="status === 'active'"> User is active</p>
  <p v-else-if="status === 'pending'">User is pending</p>
  <p v-else>User is inactive</p>

  <form @submit.prevent="addTask">
    <label for="newTask">
      Add Tasks
      <input type="text" id="newTask" name="newTask" v-model="newTask" />
    </label>
    <br>
    <button type="submit">Submit</button>
  </form>

  <h3>Tasks: </h3>
  <ul>
    <li v-for="(task, index) in tasks" :key="task">{{ task }}
      <button @click="deleteTasks(index)"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-trash" viewBox="0 0 16 16">
  <path d="M5.5 5.5A.5.5 0 0 1 6 6v6a.5.5 0 0 1-1 0V6a.5.5 0 0 1 .5-.5m2.5 0a.5.5 0 0 1 .5.5v6a.5.5 0 0 1-1 0V6a.5.5 0 0 1 .5-.5m3 .5a.5.5 0 0 0-1 0v6a.5.5 0 0 0 1 0z"/>
  <path d="M14.5 3a1 1 0 0 1-1 1H13v9a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V4h-.5a1 1 0 0 1-1-1V2a1 1 0 0 1 1-1H6a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1h3.5a1 1 0 0 1 1 1zM4.118 4 4 4.059V13a1 1 0 0 0 1 1h6a1 1 0 0 0 1-1V4.059L11.882 4zM2.5 3h11V2h-11z"/>
</svg></button>
    </li>
  </ul>
  Same only
  <a v-bind:href="link">Click for Google 1</a>
   <br>
  <a :href="link">Click for Google 2</a>
  <br>
  
  Same only
  <button v-on:click="toggleStatus">Change Status 1</button>
  <br>
  <button @click="toggleStatus">Change Status 2</button>

</template>

style format
<style scoped>
  h1 {
    color: red;
  }
</style> -->

