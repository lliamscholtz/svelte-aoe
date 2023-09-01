<script lang="ts">
	import AnimateOnEnter from '$lib/index.svelte';
	import Card from '../components/Card.svelte';
	import Pill from '../components/Pill.svelte';

	let directions = ['up', 'right', 'down', 'left'];
	let fades = ['fade', 'fade-up', 'fade-right', 'fade-down', 'fade-left'];
</script>

<AnimateOnEnter />

<main>
	<section class="text-gray-600 body-font">
		<div class="container px-5 pt-28 mx-auto">
			<div class="flex flex-wrap w-full mb-2">
				<div class="lg:w-1/2 w-full mb-2 lg:mb-0">
					<h1 class="sm:text-3xl text-2xl font-medium title-font mb-2 text-gray-900">Directions</h1>
					<div class="h-1 w-20 bg-yellow-300 rounded" />
				</div>
				<div class="lg:w-1/2 w-full leading-relaxed text-gray-500">
					{#each directions as direction}
						<Pill label={direction} />
					{/each}
				</div>
			</div>
		</div>
	</section>
	{#each directions as direction}
		<Card aoe={direction} />
	{/each}

	<section class="text-gray-600 body-font">
		<div class="container px-5 pt-28 mx-auto">
			<div class="flex flex-wrap w-full mb-2">
				<div class="lg:w-1/2 w-full mb-2 lg:mb-0">
					<h1 class="sm:text-3xl text-2xl font-medium title-font mb-2 text-gray-900">Fades</h1>
					<div class="h-1 w-20 bg-yellow-300 rounded" />
				</div>
				<div class="lg:w-1/2 w-full leading-relaxed text-gray-500">
					{#each fades as fade}
						<Pill label={fade} />
					{/each}
				</div>
			</div>
		</div>
	</section>
	{#each fades as fade}
		<Card aoe={fade} />
	{/each}
</main>
