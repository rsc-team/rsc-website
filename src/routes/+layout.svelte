<script lang="ts">
	import './layout.css';
	import Navlink from '$lib/navlink.svelte';
	const { children } = $props();
</script>

<nav class="fixed select-none flex bg-red w-full h-20">
	<a href="/" class="ml-5 flex-1 flex justify-center items-center max-w-10">
		<img src="templogo.png" 
		alt="Rutgers Solar Car Icon">
	</a>

	<nav class="flex-1 flex justify-center">
		<Navlink label={"Team"} link={"/team"}></Navlink>
		<Navlink label={"Join"} link={"/join"}></Navlink>
		<Navlink label={"Sponsors"} link={"/sponsors"}></Navlink>
		<Navlink label={"Donate"} 
		link={"https://give.rutgersfoundation.org/rutgers-solar-car-team/20133.html"} 
		newtab={true}
		textcolor={"gold"}></Navlink>
	</nav>

</nav>


{@render children()}
