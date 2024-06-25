<script setup lang="ts">
definePageMeta({
	validate: async (route) => {
		// Check if the id is made up of digits
		return (
			typeof route.params.num === "string" &&
			/^\d+$/.test(route.params.num)
		);
	},
});
</script>

<template>
	<div>
		<h1>Count: {{ $route.params.num }}</h1>
	</div>
</template>
