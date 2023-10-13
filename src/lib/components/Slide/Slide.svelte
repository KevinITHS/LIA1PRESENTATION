<script lang="ts">
	import SvelteReligion from "$lib/components/Slide/SvelteReligion/Slide1.svelte"

	export let slideNumber: string

	function getSlideComponent(slideNumber: string) {
		switch (slideNumber) {
			case "1":
				return SvelteReligion
			case "2":
				return SvelteReligion
			case "3":
				return SvelteReligion
			case "4":
				return SvelteReligion
			case "5":
				return SvelteReligion
			case "6":
				return SvelteReligion
			case "7":
				return SvelteReligion
			case "8":
				return SvelteReligion
			case "9":
				return SvelteReligion
			case "10":
				return SvelteReligion
			case "11":
				return SvelteReligion
			case "12":
				return SvelteReligion
			case "13":
				return SvelteReligion
			case "14":
				return SvelteReligion
			case "15":
				return SvelteReligion
			case "16":
				return SvelteReligion
			case "17":
				return SvelteReligion
			case "18":
				return SvelteReligion
			case "19":
				return SvelteReligion
			case "20":
				return SvelteReligion
		}
	}
</script>

<svelte:component this={getSlideComponent(slideNumber)} />
