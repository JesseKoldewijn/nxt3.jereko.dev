<script setup lang="ts">
const randomInts = Array.from({ length: 5 }, () =>
	Math.floor(Math.random() * 100)
);
</script>

<template>
	<main>
		<header>
			<nav>
				<ul>
					<li><NuxtLink to="/">Home</NuxtLink></li>
					<li><NuxtLink to="/count">Count</NuxtLink></li>
					<li>
						<NuxtLink to="/count/1">Count 1</NuxtLink>
					</li>
					<li><NuxtLink to="/count/100">Count 100</NuxtLink></li>
					<li><NuxtLink to="/count/250">Count 250</NuxtLink></li>
					<li><NuxtLink to="/count/500">Count 500</NuxtLink></li>
				</ul>
			</nav>
		</header>
		<slot />
	</main>
</template>
