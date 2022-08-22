<template>
  <main>
    <Characters>

    </Characters>

  </main>

</template>

<script>
import Characters from '@/components/Characters.vue';
export default {
  name: 'HomeView',
  components: {
    Characters
  }
}
</script>

<style scoped>
main {
  background-color: #202329;
  min-height: 100vh;
  display: flex;
  flex-direction: row;
  justify-content: center;
  padding: 3rem 0;
  gap: 2rem;
  flex-wrap: wrap;
}
</style>