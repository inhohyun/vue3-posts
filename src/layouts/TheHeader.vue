<template>
  <header>
    <nav class="navbar navbar-expand-sm navbar-dark bg-primary">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">Vue 너무 어렵다</a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto">
            <li class="nav-item">
              <router-link class="nav-link active" to="/">Home</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/about">About</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/posts">게시글</router-link>
            </li>
          </ul>
          <div class="d-flex" role="search">
            <button
              class="btn btn-outline-success .btn-dark"
              type="submit"
              @click="goPage"
            >
              글쓰기
            </button>
          </div>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
import { useRouter } from 'vue-router';
export default {
  data() {
    return {
      router: useRouter(),
    };
  },
  methods: {
    goPage() {
      this.router.push({
        name: 'PostCreate',
      });
    },
  },
};
</script>

<style></style>
