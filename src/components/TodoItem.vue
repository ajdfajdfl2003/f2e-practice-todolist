<template>
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
    <div class="todo-item stared">
      <div class="todo-header">
        <div class="todo-check">
          <input type="checkbox" id="defaultCheck3">
          <label for="defaultCheck3"></label>
        </div>
        <label class="todo-title" for="defaultCheck3">
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
        <i class="far fa-file"></i>
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
      <div class="todo-footer">
        <i class="far fa-calendar-alt"></i>
        <span>5/14</span>
      </div>
    </div>
    <div class="todo-item">
      <div class="todo-header">
        <div class="todo-check">
          <input type="checkbox" id="defaultCheck4">
          <label for="defaultCheck4"></label>
        </div>
        <label class="todo-title" for="defaultCheck4">
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
      <div class="todo-footer">
        <i class="far fa-file"></i>
      </div>
    </div>
    <div class="todo-item todo-done">
      <div class="todo-header">
        <div class="todo-check">
          <input type="checkbox" id="defaultCheck5" checked="checked">
          <label for="defaultCheck5"></label>
        </div>
        <label class="todo-title" for="defaultCheck5">
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
      <div class="todo-footer d-none">
        <i class="far fa-calendar-alt"></i>
        <span>5/14</span>
        <i class="far fa-file ml-3"></i>
        <i class="fas fa-comment-dots ml-3"></i>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Todo'
}
</script>
