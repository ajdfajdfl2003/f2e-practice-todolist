<template>
  <div id="app">
    <div class="d-flex bg-primary py-3">
      <div class="container justify-content-between d-flex todo-nav">
        <a href="#" class="active">My Task</a>
        <a href="#">In Progress</a>
        <a href="#">Completed</a>
      </div>
    </div>
    <div class="container mt-4">
      <div>
        <input type="text" class="form-control form-control-lg"/>
      </div>

      <div class="mt-4">
        <div  class="todo-item">
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
.todo-nav {
  a {
    color: $darn-primary;
    font-size: 1.5rem;
    text-decoration: none;
    display: block;
    padding-top: 24px;
    padding-bottom: 24px;
    flex: 1;
    text-align: center;
    &:active, &:hover, &.active{
      box-shadow: 0 -5px $darn-primary inset;
    }
    &.active {
      color: white;
    }
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
