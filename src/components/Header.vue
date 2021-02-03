<template>
  <div class="todo-header">
    <input type="input" placeholder="Please input todo" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Header",
});
</script>

<style>
.todo-header input {
  width: 560px;
  height: 26px;
  font-size: 14px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

.todo-header input:focus{
  outline:none;
  border-color:rgba(82, 168, 236, 0.8);
  box-shadow: inset 0 1px 1px  rgba(255, 255, 255, 1), 0 0 8px rgba(82, 168, 236, 0.6);
}
</style>