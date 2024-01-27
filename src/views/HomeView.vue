<template>
  <div class="container">
    <div>
      <div>Tasks</div>
    </div>
    <div>
      <div>In Progress</div>
    </div>
    <div>
      <div>Done</div>
    </div>
  </div>
</template>
<script setup></script>
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
</style>
