<script>
	import { onMount } from 'svelte';
	import MapUSA from './charts/MapUSA.svelte'
	import GraphicTitle from './components/GraphicTitle.svelte'
	import GraphicFooter from './components/GraphicFooter.svelte'
	import * as dataset from '../public/datasets/laws.json'

	export let width = Math.min(
		document.getElementById('interactive').getBoundingClientRect().width,
		1000
	);
</script>

<style>

</style>

<GraphicTitle
	title={"Cannabis laws in the United States after the 2020 elections"}
	subhed={"A look at something etc"}
/>
<MapUSA
	width={width}
	data={dataset.default}
	maptype={"hex"}
/>
<!-- <MapUSA
	width={width}
	data={dataset.default}
	maptype={"geo"}
/> -->
<GraphicFooter
	source={"Marijuana Policy Project"}
	note={""}
/>
