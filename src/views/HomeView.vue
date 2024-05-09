<template>
  <div>
    <h2>HomeView</h2>
    <button class="btn btn-primary" @click="goAboutPage">about으로 가기</button>
  </div>
</template>

<script>
import { useRouter } from 'vue-router';

export default {
  setup() {
    const router = useRouter();

    const goAboutPage = () => {
      router.push('/about');
    };

    return {
      goAboutPage,
    };
  },
};
</script>

<style></style>
