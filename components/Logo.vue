<template>
  <div class="VueToNuxtLogo">
    <img src="/back1.png" aspect-ratio="1" class="back1-img" />
    <v-img src="/yadab2.jpg" aspect-ratio="1" class="main-img" />
  </div>
</template>

<style>
.VueToNuxtLogo {
  display: inline-block;
  position: relative;
  width: 100%;
  padding: 30%;
}
.main-img {
  border-radius: 50%;
  overflow: hidden;
}
.back1-img {
  position: absolute;
  width: 100%;
  height: 100%;
  left: 0;
  top: 0;
  transform: rotateZ(360deg);
  animation: turn 30s linear infinite;
  z-index: 1;
}

@keyframes turn {
  100% {
    transform: rotateZ(0deg);
  }
}
</style>
