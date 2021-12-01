<script>
	import '../../static/global.css';
</script>

<main>
	<div class="main-head"><h1>30 Days of Svelte & D3.js</h1></div>
	<nav><a href="/">Home</a> | <a href="/day1">Day 1</a></nav>
	<slot />
</main>

<style>
	.main-head {
		width: 100%;
		text-align: center;
		font-weight: 700;
	}
</style>
