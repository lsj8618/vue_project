<template>
  <img class="img-asd" src="@/assets/13.png" alt="" />
  <headerView class="header" />
  <router-view />
</template>
<script>
import HeaderView from "./components/HeaderView.vue";
export default {
  components: { HeaderView },
};
</script>

<style>
.header {
  position: fixed; /* 헤더를 고정 */
  top: 0; /* 상단에 위치 */
  /* width: 100%; */
  opacity: 0.9;
}
#app {
  max-width: 100vw;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

.img-asd {
  width: 1920px;
  height: 1009px;
}

body {
  margin: 0 !important;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
