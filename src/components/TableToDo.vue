<template>
  <div>
    <table>
      <thead>
        <tr>
          <th colspan="4">TodoList</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Nom de la tache</td>
          <td>Avancement</td>
          <td>Avancer la tache</td>
          <td>Supprimer</td>
        </tr>
        <tr v-for="task in tasks" :key="task.message">
          <td>{{ task.message }}</td>
          <td><input type="checkbox" :checked="task.done" /></td>
          <td></td>
          <td><button>delete</button></td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "TableToDo",
  props: ["tasks"]
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
table,
td {
  border: 1px solid #333;
}

thead,
tfoot {
  background-color: #333;
  color: #fff;
}
</style>