<script setup lang="ts">
const randomInts = Array.from({ length: 5 }, () =>
	Math.floor(Math.random() * 100)
);
</script>

<template>
	<main>
		<header class="flex w-full sticky top-0 px-4 py-2 inset-x-0 gap-2">
			<div class="w-full py-2">
				<NuxtLink to="/" class="text-2xl font-bold">
					Nuxt Jereko
				</NuxtLink>
			</div>
			<nav class="inset-0 flex w-full">
				<div class="flex gap-5 ml-auto py-2">
					<NuxtLink class="py-1 px-2 border-2" to="/">Home</NuxtLink>
					<NuxtLink class="py-1 px-2 border-2" to="/count"
						>Count</NuxtLink
					>
					<NuxtLink class="py-1 px-2 border-2" to="/count/1"
						>Count 1</NuxtLink
					>
					<NuxtLink class="py-1 px-2 border-2" to="/count/100"
						>Count 100</NuxtLink
					>
					<NuxtLink class="py-1 px-2 border-2" to="/count/250"
						>Count 250</NuxtLink
					>
					<NuxtLink class="py-1 px-2 border-2" to="/count/500"
						>Count 500</NuxtLink
					>
				</div>
			</nav>
		</header>
		<div class="p-4 relative">
			<slot />
		</div>
	</main>
</template>
