<script lang="ts">
	export let icon: string;
	export let style: string;
	export let text: string;

	function redirect() {
		window.open(`https://${text}.com/leonardobagi`);
	}
</script>

<button class="button is-{style} is-responsive is-large" on:click={redirect}
	>{@html icon} &nbsp; {text}</button
>

<style>
	button {
		transition: 0.2s;
		width: 10em;
	}
</style>
