<script lang="ts">
	import Image from "./svelte.jpg"
	import Image2 from "./sveltekit.jpg"
</script>

<div class="grid-stack">
	<img src={Image} alt="svelte" width="500px" />
	<img src={Image2} alt="sveltekit" width="500px" />
</div>

<!-- THREE
Istället så använde vi Svelte och SvelteKit på LIA:n. Dem är relativt nya, jag tror de kanske har existerat i 3-4 år 
mindre än React eller något om jag minns rätt. Iallafall så var det just dom ramverken som han valde för Erudize projektet,
dock så gick LIA 1 mest ut på att vi skulle lära oss basic och mer avancerade koncept i Svelte och SvelteKit.  
-->

<style>
	div {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		max-width: 100vw;
		max-height: 100vw;
	}

	img:nth-child(1) {
		place-self: start center;
		margin: 5rem;
	}
	img:nth-child(2) {
		place-self: center center;
		margin: 50px;
	}
</style>
