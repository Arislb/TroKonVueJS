<template>
  <div class="home">
    <div class="bordure"></div>
    <div class="login-wrapper">
      <!-- Zone d'authentification static -->
      <div class="espace-log">
        <div class="column">
          <label for="email">E-mail :</label>
          <input id="email" v-model="email" placeholder="ici" />
        </div>
        <div class="column">
          <label for="password">Password :</label>
          <input id="password" v-model="email" placeholder="ici" />
        </div>
      </div>
      <!-- Zone d'inscription deroulante  -->
      <div class="espace-sub">
        <div class="column">
          <label for="create-email">E-mail :</label>
          <input id="create-email" v-model="email" placeholder="ici" />
        </div>
        <div class="column">
          <label for="create-password">Password :</label>
          <input id="create-password" v-model="email" placeholder="ici" />
        </div>
      </div>
    </div>
    <div class="bordure"></div>
  </div>
</template>

<script>
export default {
  setup() {},
};
</script>

<style lang="scss" scoped>
.home {
  height: 100vh;
  width: 100%;
  display: flex;
  .column {
    display: flex;
    flex-direction: column;
  }
  & .login-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    background-color: var(--primarycolor);
    height: auto;
    width: 40%;
    & .espace-log {
      background-color: rgb(87, 3, 3);
      height: 20%;
      width: 50%;
    }
  }
  & .bordure {
    border: solid 2px black;
    background-color: rgb(104, 95, 62);
    width: 30%;
    height: 100%;
  }
}
</style>

