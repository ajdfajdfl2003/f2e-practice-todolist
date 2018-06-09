<template>
  <div class="mb-4">
    <div class="todo-item active">
      <div class="d-flex todo-header">
        <div class="todo-check">
          <input type="checkbox" id="add-todo-check">
          <label for="add-todo-check"></label>
        </div>
        <label class="todo-title" for="add-todo-check">
          <input type="text" placeholder="Type Something Here…" class="">
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
            <div class="todo-icon">
              <i class="far fa-calendar-alt"></i>
            </div>
            <!--<div>
              <label for="">Deadline</label>
              <div class="form-inline todo-form-control">
                <input type="date" class="form-control border-0">
                <input type="date" class="form-control border-0 ml-2">
              </div>
            </div>-->
          </div>
        </div>
        <div class="d-flex todo-btn-group">
          <button class="btn text-danger w-50 btn-lg" @click="closeEdit">
            <i class="fas fa-times"></i> Cancel
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'EditTodo',
  methods: {
    closeEdit () {
      this.$emit('closeEditTodo')
    }
  }
}
</script>
