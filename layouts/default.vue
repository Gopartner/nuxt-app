<template>
	<div>
		<header class="shadow-sm bg-white">

			<nav class="container mx-auto p-4 flex justify-between">
				<nuxt-link to="/" class="font-bold">Layouts/default.vue</nuxt-link>
				<ul>
					<li>
						<nuxt-link to="/">Home</nuxt-link>
					</li>
					<li>
						<nuxt-link to="/about">About</nuxt-link>
					</li>
					<li>
						<nuxt-link to="/products">RAB Design</nuxt-link>
					</li>
				</ul>
			</nav>

		</header>
		<hr>

		<!-- output the page content (tag slot ini content nya dinamis sesuai link yang di klik)-->

		<div class="container mx-auto p-4">
			<slot />
		</div>

	</div>
</template>


<style scoped>
.router-link-exact-active {
	color: rgb(0, 255, 55);
}


div.at-container {
	display: flex;
	align-items: center;
	justify-content: center;
	height: 100%;
}

.at-item {

	background-color: #2c2fe6;
	border-radius: 9px;
	-moz-border-radius: 9px;
	-webkit-border-radius: 9px;
	padding: 5px;
	animation-name: tilt-in-right-1;
	animation-duration: 1s;
	animation-timing-function: ease-out;
	animation-delay: 0.2s;
	animation-iteration-count: 1;
	animation-direction: normal;
	animation-fill-mode: both;

	/* shorthand
	animation: tilt-in-right-1 1s ease-out 0.2s 1 normal both;*/
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


