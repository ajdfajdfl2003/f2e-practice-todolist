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
        <div class="todo-item stared">
          <div class="todo-header">
            <div class="todo-check">
              <input type="checkbox" id="defaultCheck1">
              <label for="defaultCheck1"></label>
            </div>
            <label class="todo-title" for="defaultCheck1">
              <span>Type Something Here…</span>
            </label>
            <div class="todo-control">
              <a href="#" class="text-muted">
                <i class="fas fa-star todo-star stared"></i>
              </a>
              <a href="#" class="text-muted">
                <i class="fas fa-pencil-alt todo-pencil"></i>
              </a>
            </div>
          </div>
          <div class="todo-footer">
            <i class="far fa-calendar-alt"></i>
            <span>5/14</span>
            <i class="far fa-file ml-3"></i>
            <i class="fas fa-comment-dots ml-3"></i>
          </div>
        </div>
        <div class="todo-item">
          <div class="todo-header">
            <div class="todo-check">
              <input type="checkbox" id="defaultCheck2">
              <label for="defaultCheck2"></label>
            </div>
            <label class="todo-title" for="defaultCheck2">
              <span>Type Something Here…</span>
            </label>
            <div class="todo-control">
              <a href="#" class="text-muted">
                <i class="far fa-star todo-star"></i>
              </a>
              <a href="#" class="text-muted">
                <i class="fas fa-pencil-alt todo-pencil"></i>
              </a>
            </div>
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
