<template>
    <div>
        <TheHeader />
        <div class="divEmConstrucao">
            <img src="../assets/emConstrucao.jpg" alt="">
        </div>
        <TheFooter />
    </div>
</template>

<script>
import TheHeader from '../components/TheHeader.vue'
import TheFooter from '../components/TheFooter.vue'

export default {
    name: 'LoandingPage',
    components: {
    TheHeader,
    TheFooter
  }
}
</script>

<style>
.divEmConstrucao {
    width: 100%;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>