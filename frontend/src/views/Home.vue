<template>
  <div class="home">
    <div class="bordure"></div>
    <!-- Zone Login -->
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
        <p @click="unroll">S'inscrire</p>
      </div>
      <!-- Zone d'inscription deroulante  -->
      <div class="espace-sub">
        <div class="column">
          <label for="create-email">E-mail :</label>
          <input id="create-email" v-model="email" />
        </div>
        <div class="column">
          <label for="create-password">Password :</label>
          <input id="create-password" v-model="password" />
        </div>
        <div class="column">
          <label for="create-passwordconfirm"> Confirm Password :</label>
          <input id="create-passwordconfirm" v-model="passwordConfirm" />
        </div>
      </div>
    </div>
    <div class="bordure"></div>
  </div>
</template>

<script>
export default {
  setup() {},
  methods: {
    unroll() {
      let subActive = document.querySelector(".espace-sub");
      subActive.classList.toggle("espace-sub-active");
    },
  },
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
    //background-color: var(--primarycolor);
    height: auto;
    width: 40%;
    position: relative;

    & .espace-log {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      background-color: rgb(87, 3, 3);
      height: 20%;
      width: 50%;
      & p {
        text-align: end;
        cursor: pointer;
      }
    }
    & .espace-sub {
      background-color: rgba(3, 23, 87, 0.338);
      width: 50%;
      height: 20%;
      position: absolute;
      z-index: -1;
      transition: transform 0.8s ease-in-out;
      transform: translateY(0);
      //transition: display 0.8s ease-in-out;
    }
    & .espace-sub-active {
      //animation: active 1s ease-in-out both;
      transition: transform 0.8s ease-in-out;
      transform: translateY(100%);
      position: absolute;
      z-index: -1;
      width: 50%;
      height: 20%;
      background-color: rgba(3, 23, 87, 0.338);
    }
  }
  & .bordure {
    border: solid 2px black;
    background-color: rgb(104, 95, 62);
    width: 30%;
    height: 100%;
  }
}

@keyframes unroll {
  0% {
    height: 0%;
  }
  100% {
    height: 20%;
  }
}
</style>

