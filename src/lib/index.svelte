<script lang="ts">
	import { onMount } from 'svelte';
	import './animations.css';

	onMount(() => {
		const elementsToLoadIn = new Set([...document.querySelectorAll('[data-aoe]')]);
		const observerOptions = {
			root: null,
			rootMargin: '0px',
			threshold: 0.3
		};
		function observerCallback(entries: IntersectionObserverEntry[]) {
			entries.forEach((entry) => {
				if (entry.isIntersecting) {
					entry.target.classList.add('aoe');
				}
			});
		}
		const observer = new IntersectionObserver(observerCallback, observerOptions);
		elementsToLoadIn.forEach((el) => observer.observe(el));
	});
</script>
