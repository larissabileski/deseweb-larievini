<script>
export default {
  data() {
    return {
      times: [
        { id: 1, name: "Time 1" },
        { id: 2, name: "Time 2" },
        { id: 3, name: "Time 3" },
        { id: 4, name: "Time 4" },
      ],
    };
  },
};
</script>

<template>
  <div class="container">
    <div class="title">
      <h2>Gerenciamento de jogadores</h2>
    </div>
    <div class="form-input">
      <input type="text" placeholder="Times" />
      <input type="text" placeholder="Jogadores" />
      <button>Salvar</button>
    </div>
  </div>
  <div class="list-items">
    <table>
      <thead>
        <tr>
          <td>ID</td>
          <td>Nome</td>
          <td>Ações</td>
          <td>Times</td>
        </tr>
      </thead>

      <tbody>
        <tr v-for="time in times" :key="time.id">
          <td>{{ time.id }}</td>
          <td>{{ time.name }}</td>
          <td>???</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<style scoped></style>
