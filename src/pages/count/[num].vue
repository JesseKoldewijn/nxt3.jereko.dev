<script setup lang="ts">
definePageMeta({
	validate: async (route: { params: { num: string } }) => {
		// Check if the id is made up of digits
		return (
			typeof route.params.num === "string" &&
			/^\d+$/.test(route.params.num)
		);
	},
});
</script>

<template>
	<title>Count {{ $route.params.num }} | Nuxt Jereko</title>
	<div>
		<h1>Count: {{ $route.params.num }}</h1>
	</div>
</template>
