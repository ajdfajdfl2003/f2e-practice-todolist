<template>
  <div id="app">
    <div class="bg-primary">
      <div class="container justify-content-between d-flex todo-nav">
        <a href="#" class="active">My Tasks</a>
        <a href="#">In Progress</a>
        <a href="#">Completed</a>
      </div>
    </div>
    <div class="container" style="margin-top: 1.5rem">
      <div class="add-todo position-relative">
        <i class="fas fa-plus fa-lg position-absolute" style="left: 1rem; top: 1.6rem"></i>
        <input type="text" class="form-control form-control-lg pl-5" placeholder="Add Task"/>
      </div>
      <div>
        <div class="todo-item">
          <div class="todo-header">
            <div class="todo-check">
              <input type="checkbox" id="defaultCheck1">
              <label for="defaultCheck1"></label>
            </div>
            <label class="todo-title" for="defaultCheck1">
              <span>Type Something Here…</span>
            </label>
          </div>
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
