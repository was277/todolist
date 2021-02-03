<template>
  <div class="todo_container">
    <div class="todo_warp">
      <Header />
      <List :todos="todos"/>
      <Footer />
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent, reactive } from "vue";
import Header from "./components/Header.vue";
import List from "./components/List.vue";
import Footer from "./components/Footer.vue";
import { Todo } from "./types/todo";

export default defineComponent({
  name: "App",
  components: {
    Header,
    List,
    Footer,
  },
  setup() {
    const state = reactive<{ todos: Todo[] }>({
      todos: [
        { id: 1, title: "aaa", isCompleted: false },
        { id: 2, title: "bbb", isCompleted: true },
        { id: 3, title: "ccc", isCompleted: false },
      ],
    });
    return {
      ...state,
    };
  },
});
</script>

<style>
.todo_container {
  width: 600px;
  margin: 0 auto;
}
.todo_container .todo_warp {
  padding: 10px;
  border: 1px solid #ddd;
  border-radius: 5px;
}
</style>
