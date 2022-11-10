<template>
    <div>
        <button>
            <nuxt-link to="/">Home</nuxt-link>
        </button>
        <h1>Products details</h1>

        <ul>
            <li>
                <nuxt-link to="/products/Jalan rabat beton trasier">Jalan rabat beton trasier</nuxt-link>
            </li>
            <li>
                <nuxt-link to="/products/Jalan rabat beton wiremes">Jalan rabat beton wiremes</nuxt-link>
            </li>
            <li>
                <nuxt-link to="/products/Jalan rabat beton molen">Jalan rabat beton molen</nuxt-link>
            </li>
            <li>
                <nuxt-link to="/products/Jalan rabat beton manual">Jalan rabat beton manual</nuxt-link>
            </li>
            <li>
                <nuxt-link to="/products/Jalan rabat beton">Jalan rabat beton</nuxt-link>
            </li>
        </ul>
        <div class='at-container'>
            <div class='at-item'>
                <span>{{ id }}</span>
            </div>
        </div>
        <hr>
    </div>
</template>

<!-- script -->
<script setup>
const { id } = useRoute().params

definePageMeta({
    // layout: 'products' (gak pakai s)
    layouts: 'products'
})
</script>

<!-- style -->
<style scoped>
h1 {
    display: flex;
    font-size: 50px;
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