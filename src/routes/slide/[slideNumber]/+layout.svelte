<script lang="ts">
	import { goto } from "$app/navigation"
	import { page } from "$app/stores"
	import { slideTimer } from "$lib/utilities/stores/slideTimer"
	import { onDestroy, onMount } from "svelte"

	const MIN_SLIDE_NUMBER = 1
	const MAX_SLIDE_NUMBER = 20

	$: slideNumber = Number($page.params.slideNumber)
	$: allowPreviousSlide = !(slideNumber <= MIN_SLIDE_NUMBER)
	$: allowNextSlide = !(slideNumber >= MAX_SLIDE_NUMBER)
	$: previousSlideURL = `/slide/${slideNumber - 1}`
	$: nextSlideURL = `/slide/${slideNumber + 1}`

	$: if ($slideTimer === 0 && allowNextSlide) {
		goto(nextSlideURL)
		slideTimer.reset()
	}

	onMount(() => {
		slideTimer.start()
	})

	onDestroy(() => {
		slideTimer.stop()
		slideTimer.reset()
	})
</script>

{$slideTimer}

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

<div class="height-100p grid-stack">
	<slot />
	<div id="hover-container">
		<div>
			<button on:click={slideTimer.reset}>RESET</button>
			<button on:click={slideTimer.start}>START</button>
			<button on:click={slideTimer.stop}>STOP</button>
		</div>

		<div>
			{#if !(slideNumber <= MIN_SLIDE_NUMBER)}
				<a href={previousSlideURL}>Previous</a>
			{/if}

			{#if !(slideNumber >= MAX_SLIDE_NUMBER)}
				<a href={nextSlideURL}>Next</a>
			{/if}
		</div>
	</div>
</div>

<style>
	#hover-container {
		place-self: start center;
		gap: 1em;
	}

	#hover-container > div {
		display: flex;
		gap: 1em;
		place-content: center;
		scale: 0;
		transition: scale 0.2s ease-in-out;
	}

	#hover-container:hover > div {
		scale: 1;
	}
</style>
