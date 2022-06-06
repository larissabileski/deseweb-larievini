<template>
  <div class="container">
    <div class="title">
      <h2>Gerenciamento de times</h2>
    </div>
    <div class="form-input">
      <input type="text" />
      <button>Salvar</button>
    </div>
  </div>
  <div class="list-times">
    <table>
      <thead>
        <tr>
          <td>ID</td>
          <td>Nome</td>
          <td>Ações</td>
        </tr>
      </thead>

      <tbody>
        <tr>
          <td>1</td>
          <td>Time 1</td>
          <td>???</td>
        </tr>
        <tr>
          <td>2</td>
          <td>Time 2</td>
          <td>???</td>
        </tr>
        <tr>
          <td>3</td>
          <td>Time 3</td>
          <td>???</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<style>
.title {
  text-align: center;
  margin: 2rem 0;
}
.form-input {
  display: flex;
  justify-content: center;
}
.form-input input {
  width: 50%;
  border: 1px solid #ccc;
  border-radius: 10px;
  padding: 0 0.5rem;
  height: 40px;
}
.form-input button {
  height: 40px;
  margin-left: 1%;
  background-color: rgb(150, 194, 125);
  font-weight: bold;
  border: 1px solid rgb(0, 0, 0);
  border-radius: 10px;
  width: 15%;
}
.list-times {
  display: flex;
  justify-content: center;
  margin: 2rem 0;
}
table {
  width: 40%;
  border: 1px solid black;
  border-collapse: collapse;
  text-align: center;
}
table thead {
  background-color: rgb(78, 127, 50);
  color: rgb(255, 255, 255);
}
table thead th {
  font-weight: bolder;
}
table tbody tr:nth-child(odd) {
  background-color: rgb(150, 194, 125);
}
h2 {
  color: black;
}
</style>
