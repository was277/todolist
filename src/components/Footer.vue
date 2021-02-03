<template>
<div class="todo-footer">
<label>
  <input type="checkbox" />
</label>
<span><span>已完成 0</span>／ 全部 2</span>
<button class="btn btn-danger">清除已完成任务</button>
</div>

</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Footer",
});
</script>

<style>
.todo-footer label{
  display: inline-block;
  margin-right: 20px;
  cursor: pointer;
}
.todo-footer label input{
  position: relative;
  top:-1px;
  vertical-align: middle;
  margin-right: 5px;
}
.todo-footer button{
  float:right;
  margin-top: 5px;
}
</style>