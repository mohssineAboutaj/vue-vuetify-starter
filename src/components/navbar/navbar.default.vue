<template>
	<div class="navbar-component">
		<v-app-bar
			:clipped-left="clipped"
			:fixed="fixed"
			color="primary"
			dark
		>
			<v-app-bar-nav-icon>
				<v-icon>fa-globe</v-icon>
			</v-app-bar-nav-icon>
			<v-spacer />
			<v-toolbar-title v-text="title" />
			<v-spacer />
			<v-app-bar-nav-icon @click="switchTheme()">
				<v-icon>fa-toggle-{{ darkMode ? 'on': 'off' }}</v-icon>
			</v-app-bar-nav-icon>
		</v-app-bar>
	</div>
</template>

<script>
import { general } from '@/mixins/navbar.js'

export default {
	mixins: [
		general,
	],
}
</script>
