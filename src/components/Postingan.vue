<template id="PostinganList">
  <div>
    <h1>Postingan</h1>
    <div class="list-group">
      <a
        href="#"
        class="list-group-item clearfix"
        v-for="(post, index) in posts"
        :key="index"
      >
        {{ post }}
        <span class="pull-right">
          <button class="btn btn-xs btn-info">
            <span class="fa fa-edit"></span>
          </button>
          <button class="btn btn-xs btn-warning">
            <span class="fa fa-trash"></span>
          </button>
        </span>
      </a>
    </div>
  </div>
</template>
<script>
export default {
  name: "PostinganList",
  data() {
    return {
      posts: [
        "Membuat Dynamic Component",
        "Api Laravel 5.5",
        "HTML Fundamental",
        "Otentikasi Dengan Laravel 5.5",
      ],
    };
  },
};
</script>
