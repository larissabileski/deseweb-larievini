<script>
import { v4 as uuid } from "uuid";
export default {
  data() {
    return {
      novo_jogador: "",
      novo_time: "",
      jogadores: [
        {
          id: "bbf13e16-8a92-49da-b37b-9f1f218bc384",
          name: "Jogador 1",
          time: "Time 1",
        },
        {
          id: "46ec141f-f35b-4e50-b60d-3db9d6a6022a",
          name: "Jogador 2",
          time: "Time 2",
        },
        {
          id: "6392406d-6273-44fd-814b-c45f4c6aed9f",
          name: "Jogador 3",
          time: "Time 3",
        },
        {
          id: "978145ff-0026-475e-adc7-5029786bb6ce",
          name: "Jogador 4",
          time: "Time 4",
        },
      ],
    };
  },
  methods: {
    salvar() {
      if (this.novo_jogador !== ""){
        const novo_id = uuid();
      this.jogadores.push({
        id: novo_id,
        name: this.novo_jogador,
      });
      this.novo_jogador = ""
      }
    },
    excluir(jogador){
      const indice = this.jogadores.indexOf(jogador)
      this.jogadores.splice (indice,1);
    }
  },
};
</script>

<template>
  <div class="container">
    <div class="title">
      <h2>Gerenciamento de jogadores</h2>
    </div>
    <div class="form-input">
      <input type="text" v-model="novo_time" @keyup.enter="salvar" placeholder="Times" />
      <input type="text" v-model="novo_jogador" @keyup.enter="salvar" placeholder="Jogadores" />
      <button @click="salvar">Salvar</button>
    </div>
  </div>
  <div class="list-items">
    <table>
      <thead>
        <tr>
          <td>ID</td>
          <td>Nome</td>
          <td>Time</td>
          <td>Ações</td>
        </tr>
      </thead>

      <tbody>
        <tr v-for="jogador in jogadores" :key="jogador.id">
          <td>{{ jogador.id }}</td>
          <td>{{ jogador.name }}</td>
          <td>{{ jogador.time }}</td>
          <td>
            <button>Editar</button>
            <button @click="excluir(time)">Apagar</button>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<style scoped></style>
