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
    </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "TableToDo"
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