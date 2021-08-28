<script context="module" lang="ts">
	export const prerender = true;
</script>

<script lang="ts">
	import { items } from './project/items';
	import Prometheus from '$lib/Prometheus.svelte';
	import IndexMeta from '$lib/IndexMeta.svelte';

	let title: string = 'SHIJIE ZHOU | Home';
	let newItem: any[] = items;

	newItem = newItem.slice(0, 9);

	function watchTitle() {
		title = 'SHIJIE ZHOU | PORTFOLIO';
	}

	$: watchTitle();
</script>

<svelte:head>
	<title>{title}</title>
	<IndexMeta />
</svelte:head>

<section>
	<Prometheus items={newItem} />
</section>
