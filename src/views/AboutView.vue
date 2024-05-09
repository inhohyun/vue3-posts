<template>
  <div>
    <h2>AboutView</h2>
    <p>{{ $route.path }}</p>
    <button class="btn btn-primary" @click="$router.push('/')">
      Home으로 이동
    </button>
  </div>
</template>

<script>
import { useRoute } from 'vue-router';
const route = useRoute();
console.log(route);

export default {};
</script>

<style></style>
