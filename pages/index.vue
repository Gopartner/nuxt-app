<template>
  <div>
    <div class='at-container'>
      <div class='at-item'>
        <h2>Home</h2>
        <main>
          <h3>ini main</h3>
          <p>Lorem ipsum dolor sit amet, voluptates ipsam iste eaque vitae ullam
            consectetur adipisicing elit. Maxime libero
            veritatis sit et doloribus. Nemo quia denetur magnam rerum ipsa.</p>
        </main>
      </div>
    </div>

  </div>
</template>

<script setup>

</script>

<style scoped>
main {
  width: 800px;
  font-size: 20px;
  color: rgb(64, 59, 114);
  border: 1px solid rgb(22, 221, 49);
  padding: 3px;
}

h3 {
  border: 1px solid red;
  text-shadow: -5px 3px 4px #796be1;
}


/*Animasi*/
div.at-container {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}

.at-item {
  width: 800px;
  height: 300px;
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