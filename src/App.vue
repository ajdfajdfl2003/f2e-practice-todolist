<template>
  <div id="app">
    <div class="bg-primary">
      <div class="container justify-content-between d-flex todo-nav">
        <a href="#" class="active">My Task</a>
        <a href="#">In Progress</a>
        <a href="#">Completed</a>
      </div>
    </div>
    <div class="container" style="padding-top: 1.5rem">
      <div class="add-todo position-relative">
        <i class="fas fa-plus fa-lg position-absolute" style="left: 1rem; top: 1.6rem"></i>
        <input type="text" class="form-control form-control-lg pl-5" placeholder="Add Task"/>
      </div>
      <div>
        <div class="todo-item">
          <div class="todo-header"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>
