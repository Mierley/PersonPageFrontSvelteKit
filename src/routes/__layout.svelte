<script lang="ts">
	import Header from '$lib/header/Header.svelte';
	import '../app.css';

	import {onMount} from 'svelte';
	import UFO from "./UFO.svelte";


</script>

<Header />

<main>
	<UFO />
	<slot />
</main>

<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 1024px;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 40px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 40px 0;
		}
	}
	body
	{
		background-image: url(static/pexels-martin-banov-4753682.jpg);
		background-repeat: no-repeat;
		background-size: cover;
		background-color: black;
		margin: 0;
		padding: 0;
	}
</style>
