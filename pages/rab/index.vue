<template>
	<div>
		<div class='judul'>
			<div class='at-judul'>
				<h1>RAB Design</h1>
				<p>rab/index.vue</p>
			</div>
		</div>
		<hr style="height:3px; background-color: lightblue;">
		<div class='at-container'>
			<div class='at-item'>
				<ul>
					<li>
						<nuxt-link to="/rab/kategori 1 gedung">kategori 1 gedung</nuxt-link>
					</li>
					<li>
						<nuxt-link to="/rab/kategori 2 jalan">kategori 2 jalan</nuxt-link>
					</li>
					<li>
						<nuxt-link to="/rab/kategori 3 kramik">kategori 3 kramik</nuxt-link>
					</li>
					<li>
						<nuxt-link to="/rab/kategori 4 gorong-gorong">kategori 4 gorong-gorong</nuxt-link>
					</li>
					<li>
						<nuxt-link to="/rab/kategori 5 jembatan titian">kategori 5 jembatan titian</nuxt-link>
					</li>
				</ul>
			</div>
		</div>
	</div>
</template>

<script setup>
definePageMeta({
	layout: 'rab'
})
</script>

<style scoped>
h {
	text-shadow: -5px 3px 4px #796be1;
}

p {
	font-size: small;
	color: blue;
}


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

/* Animasi untuk teks*/
div.judul {
	display: flex;
	align-items: center;
	justify-content: center;
	height: 100%;

}

.at-judul {
	color: #3079ed;
	font-weight: bold;
	font-size: 12px;

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