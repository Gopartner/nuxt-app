<template>
	<div>
		<header>

			<nav>
				<nuxt-link to="/rab">RAB Design</nuxt-link>
			</nav>

		</header>
		<hr>

		<div>
			<div>
				<slot />
			</div>
		</div>

	</div>
</template>


<style scoped>
header nav {
	width: 100%;
	height: 40px;
	padding: 4px;
	background-color: lightblue;
	opacity: 0.5;
	font-size: 30px;
	font-weight: bold;
	text-align: center;
	padding: 5px;
	color: #3079ed;
}
</style>


