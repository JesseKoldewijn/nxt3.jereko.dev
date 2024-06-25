<script setup lang="ts">
const randomInts = Array.from({ length: 5 }, () =>
	Math.floor(Math.random() * 100)
);
</script>

<template>
	<header>
		<nav>
			<ul>
				<li><NuxtLink to="/count">Count</NuxtLink></li>
				<li v-for="num in randomInts" :key="num">
					<NuxtLink :to="`/count/${num}`">Count {{ num }}</NuxtLink>
				</li>
			</ul>
		</nav>
	</header>
	<slot />
</template>
