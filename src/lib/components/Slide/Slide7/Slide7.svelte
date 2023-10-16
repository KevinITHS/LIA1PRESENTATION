<script lang="ts">
	import Image from "./presentationfirstpic.jpg"
	import Image2 from "./presentationsecondpic.jpg"
</script>

<div class="grid-stack">
	<img src={Image} alt="presentationfirstpic" width="400px" />
	<img src={Image2} alt="presentationsecondpic" width="500px" />
</div>

<!-- SEVEN (RESUME TIMER)
Som ni ser här och kanske också har märkt så är även denna presentationen byggt i Svelte, självklart med hjälp av
handledaren då. Det finns olika funktioner som att starta, stoppa och restarta timern, toggla elevator music, och canvas
och sånt. Och att gå fram och tillbaka med knappar och pil tangenter. 
-->

<p>Varför Svelte?</p>

<style>
	div {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		max-width: 100vw;
		max-height: 100vw;
	}

	img:nth-child(1) {
		place-self: center start;
		margin-left: 200px;
	}
	img:nth-child(2) {
		place-self: center end;
		margin-right: 200px;
	}
</style>
