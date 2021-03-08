<svelte:options tag="hello-svelte" />

<script>
	function click(e) {
		e.preventDefault();
		history.pushState({}, 'Home', '/');
		document.dispatchEvent(new Event('url-changed'));
	}
</script>

<main>
	<p>Visit the <a href="/" on:click={click}>root</a>. </p>
</main>

