<script setup>
import { ref } from 'vue'
const count = ref(0)

/* */
</script>

<template>
	<div class="font-base">
		Introduction example:
		<button
			class="rounded bg-zinc-100 px-4 py-2 text-slate-700 border-2 border-slate-200 hover:bg-zinc-200 hover:border-slate-300 transition"
			@click="count++"
		>
			Count is: {{ count }}
		</button>
	</div>
</template>

<style></style>
