<template>
  <div class="container">
    <div>
      <div>Tasks</div>
      <div class="items-box">
        <draggable v-model="tasks" tag="ul" group="todo">
          <template #item="{ element: task }">
            <li>{{ task }}</li>
          </template>
        </draggable>
      </div>
    </div>
    <div>
      <div>In Progress</div>
      <div class="items-box">
        <draggable v-model="inProgress" tag="ul" group="todo">
          <template #item="{ element: task }">
            <li>{{ task + ' ⏱' }}</li>
          </template>
        </draggable>
      </div>
    </div>
    <div>
      <div>Done</div>
      <div class="items-box">
        <draggable v-model="done" tag="ul" group="todo">
          <template #item="{ element: task }">
            <li>{{ task + ' ✅' }}</li>
          </template>
        </draggable>
      </div>
    </div>
  </div>
</template>
<script setup>
import { ref } from 'vue'
import draggable from 'vuedraggable'
const tasks = ref(['Programming', 'Trading', 'UI/UX design', 'FrontEnd', 'BackEnd'])
const inProgress = ref(['HomeWork'])
const done = ref(['practicing test'])
</script>
<style scoped>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: row;
  width: 100%;
  height: 100vh;
  column-gap: 15px;
}
.container > div {
  width: 150px;
  height: 350px;
  background-color: white;
  color: black;
  padding-bottom: 5px;
}
.container > div > div {
  width: 100%;
  height: 40px;
  box-sizing: border-box;
  padding: 5px 15px;
  font-weight: bold;
  border-bottom: 1px solid black;
  margin-bottom: 5px;
}

.container > div > .items-box {
  width: 100%;
  height: calc(100% - 40px);
  padding: 3px;
}
.container > div > .items-box > ul {
  list-style: none;
  padding: 0;
}
.container > div > .items-box > ul > li {
  box-sizing: border-box;
  padding: 0 3px;
  min-height: 24px;
  margin-bottom: 3px;
  background-color: white;
}
</style>
