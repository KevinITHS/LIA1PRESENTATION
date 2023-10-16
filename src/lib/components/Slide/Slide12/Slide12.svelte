<script lang="ts">
	import Image from "./struktur1.jpg"
	import Image2 from "./struktur2.jpg"
	import Image3 from "./struktur3.jpg"
</script>

<div class="grid-stack">
	<img src={Image} alt="struktur1" width="300px" />
	<img src={Image2} alt="struktur2" width="300px" />
	<img src={Image3} alt="struktur3" width="450px" />
</div>

<!-- 
Aa, här ser ni lite hur strukturen för storybook ser ut, första och andra bilden är varje "story" som kommer dyka upp i 
Storybooks integrerade sidebar. Och sen lägger man in ett namn under varje argument och i en separat .Svelte fil så gör man
en if statement med argument namnet och skriver koden som är relevant för just den storyn där.
Att använda Storybook ihop med Svelte känns typ lite flummigt, men jag tror att Storybook mest är gjord för att skapa 
komponenter med hjälp av React eller Vue.
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
