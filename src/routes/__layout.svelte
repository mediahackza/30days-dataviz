<script>
	import Header from '../components/Header.svelte';
	import { onMount } from 'svelte';
	import '../../static/global.css';
	import Icon from '../components/Icon.svelte';
	import { addTargetsToLinks } from '../functions.js';

	onMount(() => {
		// addTargetsToLinks();
	});
</script>

<Header />
<div class="cover">
	<img src="/images/cover-buildings.jpg" alt="buildings" />
	<div class="caption">
		Photo by <a href="https://www.pexels.com/@jonas" target="_blank">Jonas Ferlin</a> via
		<a href="https://pexels.com" target="_blank">Pexels</a>.
	</div>
</div>
<main>
	<div class="main-head">
		<h1>Svelte, D3.js & Data Visualisation</h1>
		<h3>A 30-day experiment to create a set of component-based charts using Svelte and D3.js.</h3>
	</div>
	<nav>
		<a href="/" class="icon-link"><Icon name="home" /></a>
	</nav>
	<slot />
</main>

<style>
	.main-head {
		width: 100%;
		text-align: center;
		font-weight: 700;
		padding-bottom: 30px;
		/* border-bottom: solid 1px lightgray; */
		/* margin-bottom: 30px; */
	}
	.cover {
		width: 100%;
		margin: 0px;
		border: none;
	}
	.cover img {
		width: 100%;
	}

	@media only screen and (max-width: 800px) {
		.main-head {
		}
	}
</style>
