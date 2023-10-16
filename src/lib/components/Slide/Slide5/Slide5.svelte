<script lang="ts">
	import Image from "./hotpotato3pic.jpg"
	import Image2 from "./hotpotato4pic.jpg"
	import Image3 from "./hotpotato5pic.jpg"
</script>

<div class="grid-stack">
	<img src={Image} alt="presentationfirstpic" width="300px" />
	<img src={Image2} alt="presentationsecondpic" width="300px" />
	<img src={Image3} alt="hotpotato5pic" width="450px" />
</div>

<!-- FIVE
Sen hade han även en high fidelity skiss, där vi implementerade mer avancerade koncept inom Svelte för att få
den här Hot Potato grejen att funka, först gjorde vi den i TypeScript innan vi gjorde den i Svelte.
Här har ni några bilder från figma på designet, jag tog inte med alla eftersom att det hade varit för många men ja. 
-->

<style>
	div {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		max-width: 100vw;
		max-height: 100vw;
	}

	img:nth-child(1) {
		place-self: center start;
		margin-left: 60px;
	}
	img:nth-child(2) {
		place-self: center center;
		margin-right: 200px;
	}
	img:nth-child(3) {
		place-self: center end;
		margin-right: 60px;
	}
</style>
