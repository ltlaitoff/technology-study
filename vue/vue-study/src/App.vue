<script setup>
import { RouterLink, RouterView, useRoute } from 'vue-router'
import { routes } from './router'

const route = useRoute()
</script>

<template>
	<header>
		<div class="mb-4">
			<nav class="flex gap-4">
				<RouterLink
					:class="[
						`text-sky-500 hover:text-sky-600 transition `,
						{ 'text-amber-400': route.path === currentRoute.path }
					]"
					v-for="currentRoute in routes"
					:key="currentRoute.path"
					:to="currentRoute.path"
				>
					{{ currentRoute.name }}
				</RouterLink>
			</nav>
		</div>
	</header>

	<RouterView />
</template>

<style></style>
