<template>
  <div>
    <nav class="navbar navbar-default">
      <div class="container-fluid">
        <div class="navbar-header">
          <a class="navbar-brand" href="#">BTPN Syariah</a>
        </div>
        <ul class="nav navbar-nav">
          <li>
            <a @click="dilihat = 'PostinganList'">Postingan</a>
          </li>
          <li>
            <a @click="dilihat = 'buat-postingan'">Buat Postingan</a>
          </li>
        </ul>
      </div>
    </nav>
    <input type="text" v-model="name" />
    <h4>Name: {{ name }}</h4>
    <div class="container">
      <component :is="dilihat"></component>
    </div>
  </div>
</template>

<script>
import PostinganList from "./components/Postingan.vue";

export default {
  name: "App",
  components: {
    PostinganList,
  },
  data() {
    return {
      name: "",
      dilihat: "PostinganList",
    };
  },
};
</script>
