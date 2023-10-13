<script lang="ts">
	import Slide1 from "./Slide1.svelte"

	export let slideNumber: string

	function getSlideCOmponent(slideNumber: string) {
		switch (slideNumber) {
			case "1":
				return Slide1
			default:
				return Slide1
		}
	}
</script>

<svelte:component this={getSlideCOmponent(slideNumber)} />
