<template>
  <div>
    <input v-model="message" placeholder="nom de la tache" minlength="1"/>
    <button @click="add">Ajouter</button>
  </div>
</template>

<script>
export default {
  name: "AddTodo",
  data: () => ({
    message: ""
  }),
  methods: {
    add: function () {
      if(this.message) {
        this.$emit("addTodo", {message: this.message, done: false});
      }
      else{
          alert("La tache est vide.");
      }
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>