<script lang="ts">
	import './layout.css';

	const { children } = $props();
</script>

<nav>
    <a href="/">Home</a>
    <a href="/team">Team</a>
	<a href ="/join">Join</a>
	<a href="/sponsors">Sponsors</a>
	<a href="https://give.rutgersfoundation.org/rutgers-solar-car-team/20133.html"
	   target="_blank"
	   rel="noopener noreferrer">Donate</a>
</nav>

{@render children()}
