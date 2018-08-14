<template>
  <div>
    <p>{{name}} <button @click="deleteItem">X</button>
    </p>
  </div>
</template>

<script>
export default {
  props: ["name"],

  methods: {
    deleteItem() {
      this.$emit("delete", this.name);
    }
  }
};
</script>
