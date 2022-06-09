<script>
import { v4 as uuid } from "uuid";
export default {
  data() {
    return {
      novo_jogador: "",
      novo_time: "",
      jogadores: [
        { id: "bbf13e16-8a92-49da-b37b-9f1f218bc384", name: "Jogador 1" },
        { id: "46ec141f-f35b-4e50-b60d-3db9d6a6022a", name: "Jogador 2" },
        { id: "6392406d-6273-44fd-814b-c45f4c6aed9f", name: "Jogador 3" },
        { id: "978145ff-0026-475e-adc7-5029786bb6ce", name: "Jogador 4" },
      ],
      times: [
        { id: "bbf13e16-8a92-49da-b37b-9f1f218bc384", name: "Time 1" },
        { id: "46ec141f-f35b-4e50-b60d-3db9d6a6022a", name: "Time 2" },
        { id: "6392406d-6273-44fd-814b-c45f4c6aed9f", name: "Time 3" },
        { id: "978145ff-0026-475e-adc7-5029786bb6ce", name: "Time 4" },
      ],
    };
  },
  methods: {
    salvar() {
      const novo_id = uuid();
      this.jogadores.push({
        id: novo_id,
        name: this.novo_jogador,
      });
    },
  },
};
</script>

<template>
  <div class="container">
    <div class="title">
      <h2>Gerenciamento de jogadores</h2>
    </div>
    <div class="form-input">
      <input type="text" v-model="novo_time" placeholder="Times" />
      <input type="text" v-model="novo_jogador" placeholder="Jogadores" />
      <button @click="salvar">Salvar</button>
    </div>
  </div>
  <div class="list-items">
    <table>
      <thead>
        <tr>
          <td>ID</td>
          <td>Nome</td>
          <td>Ações</td>
          <td>Time</td>
        </tr>
      </thead>

      <tbody>
        <tr v-for="jogador in jogadores in jogadores" :key="jogador.id">
          <td>{{ jogador.id }}</td>
          <td>{{ jogador.name }}</td>
          <td>???</td>
          <td></td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<style scoped></style>
