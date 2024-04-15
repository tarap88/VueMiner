<script setup>
import { computed, ref } from 'vue'
import { AppState } from './AppState'

const appState = computed(() => AppState)

const cheese = ref(0)


function countUp() {
  console.log('counting');
  cheese.value++ // the access counter in the script, you need to access the VALUE of counter
}

</script>




// HTML
<template>
  <header class="text-center m-3">
    <h1> Cheez Clickz </h1>
  </header>

  <main class="container-fluid">
    <section class="row">
      <div class="col-12 d-flex justify-content-center">
        <img @click="countUp()" src="https://img.freepik.com/premium-vector/pixel-art-cheese_565656-3.jpg" alt="">
      </div>
      <div class="text-center fw-bold mt-3">
        Cheese Clicks: {{ cheese }}
      </div>
    </section>
  </main>
</template>







// styles
<style lang="scss">
@import "./assets/scss/main.scss";
</style>
