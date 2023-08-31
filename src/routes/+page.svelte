<script lang="ts">
	import AnimateOnEnter from '$lib/index.svelte';
</script>

<AnimateOnEnter />

<h1 data-aoe="fade-up">Svelte AnimateOnEnter</h1>
<p data-aoe="fade-left">
	<strong>svelte-aoe</strong> utilizes the Intersection Observer API to detect when an element enters
	the viewport. When the element is detected as being in the viewport, svelte-aoe applies a class that
	triggers a CSS animation.
</p>

<img data-aoe="fade-right" alt="Dummy" src="https://dummyimage.com/500x300" />
