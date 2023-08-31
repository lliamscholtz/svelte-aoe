# Svelte AnimateOnEnter

Create captivating web experiences with the `svelte-aoe` package.

`svelte-aoe` utilizes the [Intersection Observer API](https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API) to detect when an element enters the viewport. When the element is detected as being in the viewport, `svelte-aoe` applies a class that triggers a CSS animation.

## Installation

```
npm i svelte-aoe --save-dev
```

## Setup

- Import the package

```
import AnimateOnEnter from 'svelte-aoe';
```

- Add the component to your layout/page.

```
<AnimateOnEnter />
```

- Apply a `data-aoe` attribute to the element that you want to animate and define an animation.

```
<img data-aoe="fade-up" src="https://dummyimage.com/500x300"/>
```

## Example: SvelteKit Global Setup

File: `src/routes/+layout.svelte`

```
<script>
	import AnimateOnEnter from 'aoe.svelte';
</script>

<AppShell>
	<AnimateOnEnter />
	<slot />
</AppShell>
```

## Animations

- `fade-up`
- `fade-left`
- `fade-right`

---

❤️ Inspired by [Animate on Scroll](https://michalsnik.github.io/aos/)
