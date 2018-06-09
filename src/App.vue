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
      <div class="add-todo position-relative" v-if="this.isNewTodo === false">
        <i class="fas fa-plus fa-lg position-absolute" style="left: 1rem; top: 1.6rem"></i>
        <input type="text" class="form-control form-control-lg pl-5"
               placeholder="Add Task" @focus="addNewTodo"/>
      </div>
      <transition name="slide">
        <edit-todo-item v-if="isNewTodo"
                        @closeEditTodo="closeEdit">
        </edit-todo-item>
      </transition>
      <todo-item />
    </div>
  </div>
</template>

<script>
import TodoItem from './components/TodoItem'
import EditTodoItem from './components/EditTodoItem'

export default {
  name: 'App',
  data () {
    return {
      isNewTodo: false
    }
  },
  components: {
    TodoItem,
    EditTodoItem
  },
  methods: {
    addNewTodo () {
      this.isNewTodo = true
    },
    closeEdit () {
      this.isNewTodo = false
    }
  }
}
</script>
