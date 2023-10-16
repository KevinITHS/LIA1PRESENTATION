<script lang="ts">
	import Image from "./hotpotato1pic.jpg"
	import Image2 from "./hotpotato2pic.jpg"
</script>

<div class="grid-stack">
	<img src={Image} alt="hotpotato1pic" width="800px" />
	<img src={Image2} alt="hotpotato2pic" width="1000px" />
</div>

<!-- FOUR
Vi fick hålla på med olika prototyper och mindre individuella projekt byggda i dessa ramverk. Som var en stor utmaning då
vi inte hade så lång tid på att lära oss ramverket innan vi fick sätta igång. Det vi gjorde i början var att implementera
en enkel prototyp från figma av Hot Potato spelet som ni ser här, som vi sen utvecklade mer och mer för varje vecka. 
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
		margin-top: 60px;
		margin-bottom: 100px;
	}
	img:nth-child(2) {
		margin-top: 125px;
		place-self: center center;
	}
</style>
