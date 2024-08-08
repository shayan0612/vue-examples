<!-- <script>
export default {
  data() {
    return {
      name: "Shayan Naveed",
      status: "inactive",
      tasks: ["task one", "task two", "task three"],
      link: "https://google.com",
    };
  },
  methods: {
    toogleStatus() {
      if (this.status === "active") {
        this.status = "pending";
      }  else {
        this.status = "active";
      }
    },
  },
};
</script>

<template>
  <h1>{{ name }}</h1>
  <p v-if="status === 'active'">User is active</p>
  <p v-else>user is inactive</p>
  <h3>Tasks</h3>
  <ul>
    <li v-for="task in tasks" :key="task">{{ task }}</li>
  </ul>
  <a v-bind:href="link">Click to go on google</a>

  <br />
  <button v-on:click="toogleStatus">Change status</button>
</template> -->
<!-- <script setup>
import { ref, onMounted } from "vue";

let name = ref("shayan naveed");
let status = ref("active");
let tasks = ref(["task one", "task two", "task three"]);
let newTask = ref("");
let toogleStatus = () => {
  if (status.value === "active") {
    status.value = "inactive";
  } else {
    status.value = "active";
  }
};
let addTask = () => {
  if (newTask.value.trim() !== "") {
    tasks.value.push(newTask.value);
    newTask.value = "";
  }
};
let delBtn = (index) => {
  tasks.value.splice(index, 1);
};
onMounted(async () => {
  try {
    let response = await fetch(
      "https://jsonplaceholder.typicode.com/todos?_limit=5"
    );
    let data = await response.json();
    tasks.value = data.map((task) => task.title);
  } catch (error) {
    console.log("erroe");
  }
});
</script>

<template>
  <h1>{{ name }}</h1>
  <p v-if="status === 'active'">User is active</p>
  <p v-else>user is inactive</p>
  <form @submit.prevent="addTask">
    <label>Add Task:</label>
    <input type="text" id="newTask" name="NewTask" v-model="newTask" />
    <button type="sumbit">Sumbit</button>
  </form>
  <h3>Tasks</h3>
  <ul>
    <li v-for="(task, index) in tasks" :key="task">
      <span>
        {{ task }}
      </span>
      <button @click="delBtn(index)">x</button>
    </li>
  </ul>
  <br />
  <button v-on:click="toogleStatus">Change status</button>
</template> -->
