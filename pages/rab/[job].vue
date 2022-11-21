<template>
  <div>
      <div class='at-container'>
          <div class='at-item'>
              <span>{{ job }}</span>
          </div>
      </div>
      <p class="job">ini [job].vue</p>
  </div>
</template>

<!-- script -->
<script setup>
const { job } = useRoute().params

definePageMeta({
  layout: 'rab'
})
</script>




<!-- style -->
<style scoped>
/* my style */
.job {
  width: 100%;
  height: 40px;
  background-color: green;
  opacity: 0.7;
  color: white;
  text-align: center;
  align-items: 50px;
}
h1 {
  display: flex;
  font-size: 12px;
  justify-content: center;
  text-shadow: -5px 3px 4px #796be1;
}

span {
  text-shadow: -5px 3px 4px #796be1;
  display: flex;
  font-size: 60px;
  justify-content: center;
}

button {
  font-size: 15px;
  width: 100px;
  background-color: rgb(87, 45, 240);
  padding: 5px;
  border-radius: 8px;
  color: rgb(237, 241, 243) !important;
}

button a {
  text-decoration: none;
}

/* ====== Animasi =====*/
div.at-container {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 200px;

}

.at-item {
  width: 600px;
  height: 100px;
  background-color: #ffe672;
  border-radius: 9px;
  -moz-border-radius: 9px;
  -webkit-border-radius: 9px;
  padding: 5px;
  animation-name: tilt-in-right-1;
  animation-duration: 1.2s;
  animation-timing-function: ease-out;
  animation-delay: 0s;
  animation-iteration-count: 1;
  animation-direction: alternate;
  animation-fill-mode: backwards;

  /* shorthand
  animation: tilt-in-right-1 1.2s ease-out 0s 1 alternate backwards;*/
}

@keyframes tilt-in-right-1 {

  0% {
      transform: rotateX(-30deg) translateX(300px) skewX(30deg);
      opacity: 0;
  }

  100% {
      transform: rotateX(0deg) translateX(0) skewX(0deg);
      opacity: 1;
  }
}
</style>