<script lang="ts">
	import './layout.css';
	import Navlink from '$lib/navlink.svelte';
	const { children } = $props();
</script>

<nav class="z-100 fixed select-none flex w-full h-20">
	<a href="/" class="absolute ml-5 flex-1 flex justify-center items-center h-full max-w-15">
		<img src="assets/rscicon.png" 
		alt="Rutgers Solar Car Icon">
	</a>

	<nav class="flex-1 justify-center flex">
		<Navlink label={"Team"} link={"/team"}></Navlink>
		<Navlink label={"Join"} link={"/join"}></Navlink>
		<Navlink label={"Sponsors"} link={"/sponsors"}></Navlink>
		<Navlink label={"Donate"} 
		link={"https://give.rutgersfoundation.org/rutgers-solar-car-team/20133.html"} 
		newtab={true}
		textclass={"text-gold"}
		></Navlink>
	</nav>

</nav>


{@render children()}
