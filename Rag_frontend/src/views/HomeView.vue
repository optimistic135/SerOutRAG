<template>
  <NavHome />

  <div class="main-home-veiw">
    <img src="../assets/HomeImage/TranLine.png" alt="triangle-line">
    <div class="home-content">
      <ColorfulRound />
      <ManInHome />
    </div>
  </div>

  <div class="footer-background">
    <img src="../assets/HomeImage/Rectangle.png" alt="triangle-line">
  </div>

</template>

<script lang="ts">
import { defineComponent } from 'vue';
import ColorfulRound from '@/components/ColorfulRound.vue';
import NavHome from '@/components/NavHome.vue';
import ManInHome from '@/components/ManInHome.vue';

export default defineComponent({
  name: 'App',
  components: {
    NavHome,
    ColorfulRound,
    ManInHome
  },
});
</script>

<style scoped>
.main-home-veiw {
  display: flex;
  justify-content: center;
  align-items: center;
}

.home-content {
  display: flex;
  position: relative;
}

.footer-background img {
  width: 98%;
  position: absolute;
  bottom: 0;
  opacity: 1;
  background: rgb(238, 243, 255);
  filter: blur(50px);
  z-index: -1; 
}
</style>