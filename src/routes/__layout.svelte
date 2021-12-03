<script>
	import { pages } from '../pages.js';
	import Header from '../components/Header.svelte';
	import '../../static/global.css';
	import Icon from '../components/Icon.svelte';
	export let coverImage = 'cover-buildings';

	import { onMount } from 'svelte';
	import { page } from '$app/stores';
	let pagename;
	$: if ($page) {
		pagename = pages.filter((p) => p.path === $page.path)[0].pagename;
	}

	function getPath(p) {
		return p.path;
	}
	onMount(() => {});
</script>

<svelte:head>
	<title>Media Hack Data Viz Geek</title>
</svelte:head>
<Header />
<div class="cover">
	<img src="/images/{coverImage}.jpg" alt="buildings" />
	<div class="caption">
		Photo by <a href="https://www.pexels.com/@jonas" target="_blank">Jonas Ferlin</a> via
		<a href="https://pexels.com" target="_blank">Pexels</a>.
	</div>
</div>
<main>
	<div class="main-head">
		<h1>Svelte, D3.js & Data Visualisation</h1>
		<div>{pagename}</div>
		<h3>A 30-day experiment to create a set of component-based charts using Svelte and D3.js.</h3>
		<div class="subscribe">
			Want to know when new sections are added to this series? <a
				href="https://mediahack.co.za/datavizgeek/updates.html">Subscribe to updates</a
			>.
		</div>
	</div>
	<nav>
		<a href="/" class="icon-link"><Icon name="home" /></a>
	</nav>
	<div class="pager">
		<!-- <div class="content-label">Contents</div> -->
		<a href="/">Introduction</a>
		<a href="/setting-up">Setting Up</a>
		<a href="/day1">Day 1</a>
		<a href="/day2">Day 2</a>
		<div class="full-contents"><a href="/contents">Extended contents listing</a></div>
	</div>
	<slot />
</main>

<style>
	.main-head {
		width: 100%;
		text-align: center;
		font-weight: 700;
		padding-bottom: 10px;
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
	.subscribe {
		font-weight: 300;
	}
	.pager {
		width: 100%;
		/* padding: 10px; */

		/* border: dashed 1px lightgray; */
		/* background: rgb(247, 247, 247); */
		font-size: 1rem;
		/* font-weight: 300; */
		border-bottom: solid 1px lightgray;
		padding-bottom: 20px;
		margin-bottom: 30px;
		line-height: 1.5rem;
	}

	.pager a {
		margin: 0 3px;
	}

	@media only screen and (max-width: 800px) {
		.main-head {
		}
	}
</style>
