<template>
  <div>
    <input v-model="task.message" placeholder="nom de la tache" minlength="1"/>
    <button @click="emitQlqchose">Ajouter</button>
  </div>
</template>

<script>
export default {
  name: "InputList",
  data: () => ({
    task: { message: "", avancement: "" },
  }),
  methods: {
    emitQlqchose: function () {
      if(this.task.message) {
        this.task.avancement = "ToDo";
        this.$emit("event", this.task);
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