<template>
  <div id="app">
    <div class="bg-primary">
      <div class="container justify-content-between d-flex todo-nav">
        <a href="#" class="active">My Task</a>
        <a href="#">In Progress</a>
        <a href="#">Completed</a>
      </div>
    </div>
    <div class="container mt-4">
      <div class="position-relative">
        <i class="add-todo fas fa-plus fa-lg position-absolute" style="left: 1rem; top: 1.15rem"></i>
        <input type="text" class="add-todo form-control form-control-lg pl-5" placeholder="Add Task"/>
      </div>

      <div class="mt-4">
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

<style lang="scss">
  $darn-primary: #00408B;
  $light-warning: #FFF2DC;

  body, ul {
    margin: 0;
    font-family: 'Roboto', 'Microsoft JhengHei', '微軟正黑體', sans-serif;
  }

  .todo-nav {
    a {
      color: $darn-primary;
      font-size: 1.5rem;
      text-decoration: none;
      display: block;
      padding-top: 20px;
      padding-bottom: 20px;
      flex: 1;
      text-align: center;
      &:active, &:hover, &.active {
        color: white;
        box-shadow: 0 -5px $darn-primary inset;
      }
    }
  }

  .add-todo {
    color: #C8C8C8;

    &::placeholder {
      color: #C8C8C8;
      text-align: left;
    }
  }

  .todo-item {
    display: flex;
    flex-direction: column;
    background-color: $light-warning;
    border-radius: 3px;
    padding: 24px;
    .todo-header {
      display: flex;
    }

    .todo-title {
      flex: 1;
      font-size: 1.5rem;
    }
  }
</style>
