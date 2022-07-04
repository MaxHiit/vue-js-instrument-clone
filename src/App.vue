<script setup>
import { RouterLink, RouterView } from 'vue-router';
</script>

<template>
	<header>
		<RouterLink to="/" class="logo">INSTRUMENT</RouterLink>
		<nav class="nav-items">
			<RouterLink to="/" class="nav-item">Wath we do</RouterLink>
			<RouterLink to="/about" class="nav-item">Who we are</RouterLink>
			<RouterLink to="/about" class="nav-item">Being here</RouterLink>
			<RouterLink to="/about" class="nav-item">Carrers</RouterLink>
		</nav>
	</header>

	<RouterView />
</template>

<style lang="scss">
#app {
	max-width: 1750px;
	margin: 0 auto;
	padding: 2rem;
	font-weight: normal;
}

header {
	display: flex;
	justify-content: space-between;
	align-items: center;
}

.logo {
	font-size: 1.7rem;
}

.nav {
	&-item {
		text-transform: uppercase;
		padding: 10px 20px;
		position: relative;

		&::before,
		&::after {
			position: absolute;
			top: calc(50% - 1px);
			transform: translateY(-50%);
			opacity: 0;
			transition: opacity 0.3s ease-in-out;
		}
		&::before {
			content: '[';
			left: 0;
		}

		&::after {
			content: ']';
			right: 0;
		}

		&:hover::before,
		&:hover::after {
			opacity: 0.5;
		}

		&s {
			display: flex;
			gap: 5rem;
		}
	}
}
</style>
