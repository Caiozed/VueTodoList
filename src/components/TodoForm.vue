<template>
  <form @submit.prevent="onSubmit"> 
    <input required v-model="todo"/>
    <button>Add</button>
  </form>
</template>

<script>
export default {
  methods: {
    onSubmit(e, todo) {
      this.$emit("onsubmit", this.todo);
      this.todo = "";
      e.target.reset();
    }
  },

  data() {
    return {
      todo: ""
    };
  }
};
</script>
