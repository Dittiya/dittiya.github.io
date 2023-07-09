<script setup>
import { RouterLink } from 'vue-router';
</script>

<template>
	<header class="position-relative top-0 start-0 end-0">
		<nav class="navbar navbar-expand-lg border-bottom border-bottom-dark">
			<div class="container-fluid nav nav-underline justify-content-end">
				<RouterLink to="/" active-class="text-white" class="nav-item link-underline link-underline-opacity-0">Home
				</RouterLink>
				<RouterLink to="/about" active-class="text-white" class="nav-item link-underline link-underline-opacity-0">
					About
				</RouterLink>
				<RouterLink to="/projects" active-class="text-white"
					class="nav-item link-underline link-underline-opacity-0">
					Projects</RouterLink>
			</div>
		</nav>
	</header>
</template>

<style>
.nav-item {
	color: #9DB2BF;
}

/* Hax
 * if someone knows how to do this elegantly pls tell me
 */
.nav-item:hover {
	background: #121212;
	color: #bfd0db;
}</style>