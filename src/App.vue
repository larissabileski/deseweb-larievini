<template>
  <header class="menu-superior">
    <div class="menu-esquerda">
      <span>Home</span>
      <span>|</span>
      <span>Jogadores</span>
      <span>|</span>
      <span>Times</span>
    </div>
    <div class="menu-direito">
      <span>Sair</span>
    </div>
  </header>
  <main>
    <RouterView />
  </main>
  <footer>Rodapé</footer>
</template>

<style>
@import "@/assets/base.css";

#app {
  max-width: 1280px;
  margin: 0 auto;
  font-weight: normal;
  height: 100vh;
}
header.menu-superior {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
header,
footer {
  background-color: rgb(78, 127, 50); 
  color: rgb(255, 255, 255);
  height: 15%;
  font-size: 1.3em;
  display: flex;
  align-items: center;
  padding-left: 2rem;
}

header span {
  padding: 0px 20px;
}

main {
  height: 70%;
}
</style>
