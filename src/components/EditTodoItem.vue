<template>
  <div class="mb-4">
    <div class="todo-item active">
      <div class="d-flex todo-header">
        <div class="todo-check">
          <input type="checkbox">
          <label></label>
        </div>
        <label class="todo-title">
          <input type="text" placeholder="Type Something Here…" v-model="cacheTodo.message">
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
      <div class="todo-body">
        <div class="todo-content">
          <div class="todo-row">
            <div class="todo-icon d-inline">
              <i class="far fa-calendar-alt"></i>
              <label>Deadline</label>
            </div>
            <div>
              <div class="form-inline todo-form-control">
                <input type="date" class="form-control border-0">
                <input type="date" class="form-control border-0 ml-2">
              </div>
            </div>
          </div>
          <div class="todo-row">
            <div class="todo-icon d-inline">
              <i class="far fa-file"></i>
              <label>File</label>
            </div>
            <div>
              <div class="todo-form-control">
                <i class="fas fa-plus-square" style="font-size: 36px"></i>
              </div>
            </div>
          </div>
          <div class="todo-row">
            <div class="todo-icon d-inline">
              <i class="far fa-comment-dots"></i>
              <label>Comment</label>
            </div>
            <div>
              <div class="todo-form-control">
                <textarea name="" class="form-control w-100 border-0" placeholder="Type your memo here"
                          ></textarea>
              </div>
            </div>
          </div>
        </div>
        <div class="d-flex todo-btn-group">
          <button class="btn btn-white text-danger w-50 btn-lg" @click="closeEdit">
            <i class="fas fa-times"></i> Cancel
          </button>
          <button class="btn btn-primary w-50 btn-lg" @click="saveTodo">
            <i class="fas fa-plus"></i> Save
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['todo'],
  name: 'EditTodo',
  data () {
    return {
      cacheTodo: {},
      comment: '',
      isNew: false
    }
  },
  methods: {
    closeEdit () {
      this.$emit('closeEditTodo')
    },
    saveTodo () {
      this.$emit('closeEditTodo')
    }
  }
}
</script>
<style lang="scss">
  .btn-white {
    background-color: white;
    border-color: white;
  }
</style>
