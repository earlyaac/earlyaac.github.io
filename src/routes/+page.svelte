<script lang="ts">
	import Button from '$lib/Button.svelte';
	import slip from '$lib/slip.mp3';

	let audio:HTMLAudioElement;

	function honk() {
		audio.load();
		audio.play();
	}
</script>

<audio src={slip} bind:this={audio}></audio>
<Button onclick={honk} />