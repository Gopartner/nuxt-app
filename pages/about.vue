<template>
	<div>
		<div class='at-container'>
			<div class='at-item'>
				<h2>About</h2>
			</div>
		</div>
		<div class="angry-animate">
			<p>Lorem ipsum dolor sit amet, voluptates ipsam iste eaque vitae ullam </p>
			<p>consectetur adipisicing elit. Maxime libero </p>
			<p> veritatis sit et doloribus. Nemo quia denetur magnam rerum ipsa.</p>
		</div>
	</div>
</template>

<script setup>

</script>

<style scoped>
h {
	color: green;
}

p {
	font-size: small;
	color: blue;
}

/*Animasi untuk kotak (awal baris)*/
.angry-animate {
	-webkit-animation: bounce-in 0.7s ease-out 0.2s 1 normal;
	-moz-animation: bounce-in 0.7s ease-out 0.2s 1 normal;
	-ms-animation: bounce-in 0.7s ease-out 0.2s 1 normal;
	animation: bounce-in 0.7s ease-out 0.2s 1 normal;
}

@-webkit-keyframes bounce-in {
	0% {
		opacity: 0;
		-webkit-transform: scale(.3);
		transform: scale(.3);
	}

	50% {
		opacity: 1;
		-webkit-transform: scale(1.0);
		transform: scale(1.0);
	}

	70% {
		-webkit-transform: scale(0.9);
		transform: scale(0.9);
	}

	100% {
		-webkit-transform: scale(1);
		transform: scale(1);
	}
}

@keyframes bounce-in {
	0% {
		opacity: 0;
		transform: scale(.3);
	}

	50% {
		opacity: 1;
		transform: scale(1.0);
	}

	70% {
		transform: scale(0.9);
	}

	100% {
		transform: scale(1);
	}
}

/*Animasi untuk kotak (akhir baris)*/

/* Animasi untuk teks*/
div.at-container {
	display: flex;
	align-items: center;
	justify-content: center;
	height: 100%;

}

.at-item {
	color: #3079ed;
	font-weight: bold;
	font-size: 3em;

	animation-name: focus-in-contract;
	animation-duration: 1.2s;
	animation-timing-function: ease-out;
	animation-delay: 0s;
	animation-iteration-count: 1;
	animation-direction: normal;
	animation-fill-mode: both;



	animation: focus-in-contract 1.2s ease-out 0s 1 normal both;
}

@keyframes focus-in-contract {

	0% {
		letter-spacing: 1em;
		filter: blur(12px);
		opacity: 0;
	}

	100% {
		filter: blur(0);
		opacity: 1;
	}
}
</style>