<script lang="ts">
	let { audioBind=$bindable(), audioSrc, buttonClick, buttonText } = $props();
</script>

<audio bind:this={audioBind} src={audioSrc}></audio>
<button onclick={() => { setTimeout(buttonClick, 10); speechSynthesis.speak(new SpeechSynthesisUtterance(buttonText)); }}>
	{buttonText}
</button>

<style>
	button {
		font-size: 1.4em;
		width: 5em;
		height: 5em;
		border-radius: 75%;
		background: radial-gradient(circle at 25% 25%, hsl(0, 100%, 50%) 0, hsl(0, 100%, 40%) 100%);
		box-shadow: 0 8px 0 hsl(0, 100%, 30%), 2px 12px 10px rgba(0,0,0,.35);
		color: hsl(0, 100%, 30%);
		text-shadow: -1px -1px 2px rgba(0,0,0,0.3), 1px 1px 2px rgba(255,255,255,0.4);
		text-transform: uppercase;
		letter-spacing: 0.05em;
		transform: translate(0, -8px);
		transition: all 0.2s;
		text-align: center;
	}

	button:active {
		transform: translate(0, -2px);
		box-shadow: 0 2px 0 hsl(0, 100%, 30%), 2px 6px 10px rgba(0,0,0,.35);
	}
</style>