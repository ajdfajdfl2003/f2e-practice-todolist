<template>
  <div id="app">
    <div class="bg-primary">
      <div class="container justify-content-between d-flex todo-nav">
        <a href="#" :class="{active: currentTab === 'all'}" @click="currentTab = 'all'">My Tasks</a>
        <a href="#" :class="{active: currentTab === 'progress'}" @click="currentTab = 'progress'">In Progress</a>
        <a href="#" :class="{active: currentTab === 'done'}" @click="currentTab = 'done'">Completed</a>
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
                        @closeEditTodo="closeEdit"
                        @updateData="getData">
        </edit-todo-item>
      </transition>
      <div v-for="todo in todos" :key="todo.id">
        <todo-item
          :todo="todo"
          @updateData="getData"
        ></todo-item>
      </div>
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
      todos: [],
      isNewTodo: false,
      currentTab: 'all'
    }
  },
  components: {
    TodoItem,
    EditTodoItem
  },
  methods: {
    addNewTodo () {
      this.isNewTodo = true
      this.currentTab = {}
    },
    closeEdit () {
      this.isNewTodo = false
      this.currentTab = 'all'
    },
    getData () {
      const vm = this
      let todos = JSON.parse(vm.$localStorage.get('todos'))
      if (todos) {
        vm.todos = todos
      }
    }
  },
  created () {
    const vm = this
    vm.getData()
  }
}
</script>
