<script lang="ts">
	import { goto } from "$app/navigation"
	import { page } from "$app/stores"
	const MIN_SLIDE_NUMBER = 1
	const MAX_SLIDE_NUMBER = 20
	$: slideNumber = Number($page.params.slideNumber)
	$: allowPreviousSlide = !(slideNumber <= MIN_SLIDE_NUMBER)
	$: allowNextSlide = !(slideNumber >= MAX_SLIDE_NUMBER)
	$: previousSlideURL = `/slide/${slideNumber - 1}`
	$: nextSlideURL = `/slide/${slideNumber + 1}`
</script>

<svelte:body
	on:keydown={(event) => {
		const { key } = event
		switch (key) {
			case "ArrowLeft":
				if (allowPreviousSlide) return goto(previousSlideURL)
				break
			case "ArrowRight":
				if (allowNextSlide) return goto(nextSlideURL)
				break
		}
	}} />

<slot />

{#if !(slideNumber <= MIN_SLIDE_NUMBER)}
	<a href={previousSlideURL}>Previous</a>
{/if}

{#if !(slideNumber >= MAX_SLIDE_NUMBER)}
	<a href={nextSlideURL}>Next</a>
{/if}
