<script>
	import Nav from '../components/Nav.svelte';

	export let segment;
</script>

<!-- Main wrapper -->
<div class="wrapper" id="wrapper">
	<Nav {segment}/>

	<main>
		<slot></slot>
	</main>
</div>