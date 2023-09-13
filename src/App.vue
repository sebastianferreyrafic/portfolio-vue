
<script setup>
 
</script>

<template >
  <div id="app">
    <!-- <video id="background-video" autoplay loop muted poster="poster.jpg">
  <source src="./media/matrix.mp4" type="video/mp4">
</video> -->
    <Navbar />
    <router-view />
  </div>
</template>

<script>


import Navbar from "@/components/Navbar.vue"
export default {
  components: {
    Navbar,
    

  }
};
</script>





