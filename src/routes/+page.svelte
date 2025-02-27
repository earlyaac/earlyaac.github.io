<script lang="ts">
	import Button from '$lib/Button.svelte';

	let audio:HTMLAudioElement;

	function honk() {
		audio.volume = 0.4;
		audio.load();
		audio.play();
	}
</script>

<div class="grid grid-cols-3 p-5 justify-items-center content-around items-center h-dvh w-full">
	<Button bind:audioBind={audio} audioSrc="https://cdn.freesound.org/previews/61/61847_142047-lq.mp3" buttonClick={honk} buttonText="Head"/>
	<Button bind:audioBind={audio} audioSrc="https://cdn.freesound.org/previews/61/61847_142047-lq.mp3" buttonClick={honk} buttonText="Shoulder"/>
	<Button bind:audioBind={audio} audioSrc="https://cdn.freesound.org/previews/61/61847_142047-lq.mp3" buttonClick={honk} buttonText="Knees"/>
	<div class="col-span-3">
		JUST A TEST OF <em>EARLY AAC</em>. WORK IN PROGRESS!
	</div>
	<Button bind:audioBind={audio} audioSrc="https://cdn.freesound.org/previews/61/61847_142047-lq.mp3" buttonClick={honk} buttonText="Toes"/>
	<Button bind:audioBind={audio} audioSrc="https://cdn.freesound.org/previews/61/61847_142047-lq.mp3" buttonClick={honk} buttonText="This is"/>
	<Button bind:audioBind={audio} audioSrc="https://cdn.freesound.org/previews/61/61847_142047-lq.mp3" buttonClick={honk} buttonText="EarlyAAC"/>
</div>