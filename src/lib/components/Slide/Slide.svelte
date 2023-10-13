<script lang="ts">
	import Slide1 from "$lib/components/Slide/Slide1/Slide1.svelte"
	import Slide2 from "$lib/components/Slide/Slide2/Slide2.svelte"
	import Slide3 from "$lib/components/Slide/Slide3/Slide3.svelte"
	import Slide4 from "$lib/components/Slide/Slide4/Slide4.svelte"
	import Slide5 from "$lib/components/Slide/Slide5/Slide5.svelte"
	import Slide6 from "$lib/components/Slide/Slide6/Slide6.svelte"
	import Slide7 from "$lib/components/Slide/Slide7/Slide7.svelte"
	import Slide8 from "$lib/components/Slide/Slide8/Slide8.svelte"
	import Slide9 from "$lib/components/Slide/Slide9/Slide9.svelte"
	import Slide10 from "$lib/components/Slide/Slide10/Slide10.svelte"
	import Slide11 from "$lib/components/Slide/Slide11/Slide11.svelte"
	import Slide12 from "$lib/components/Slide/Slide12/Slide12.svelte"
	import Slide13 from "$lib/components/Slide/Slide13/Slide13.svelte"
	import Slide14 from "$lib/components/Slide/Slide14/Slide14.svelte"
	import Slide15 from "$lib/components/Slide/Slide15/Slide15.svelte"
	import Slide16 from "$lib/components/Slide/Slide16/Slide16.svelte"
	import Slide17 from "$lib/components/Slide/Slide17/Slide17.svelte"
	import Slide18 from "$lib/components/Slide/Slide18/Slide18.svelte"
	import Slide19 from "$lib/components/Slide/Slide19/Slide19.svelte"
	import Slide20 from "$lib/components/Slide/Slide20/Slide20.svelte"

	export let slideNumber: string

	function getSlideComponent(slideNumber: string) {
		switch (slideNumber) {
			case "1":
				return Slide1
			case "2":
				return Slide2
			case "3":
				return Slide3
			case "4":
				return Slide4
			case "5":
				return Slide5
			case "6":
				return Slide6
			case "7":
				return Slide7
			case "8":
				return Slide8
			case "9":
				return Slide9
			case "10":
				return Slide10
			case "11":
				return Slide11
			case "12":
				return Slide12
			case "13":
				return Slide13
			case "14":
				return Slide14
			case "15":
				return Slide15
			case "16":
				return Slide16
			case "17":
				return Slide17
			case "18":
				return Slide18
			case "19":
				return Slide19
			case "20":
				return Slide20
		}
	}
</script>

<svelte:component this={getSlideComponent(slideNumber)} />
