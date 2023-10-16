<script lang="ts">
	import Image from "./storybook1.jpg"
	import Image2 from "./storybook2.jpg"
</script>

<div class="grid-stack">
	<img src={Image} alt="storybook1" width="750px" />
	<img src={Image2} alt="storybook2" width="800px" />
</div>

<!-- ELEVEN 
När vi gjorde high fidelity versionen av hot potato spelet så använde vi oss även av Storybook. 
Storybook är typ att man bygger något större fast i mindra bitar, det är lite svårt att förklara utan att visa det,
men det tillåter utvecklare att skapa och testa komponenter isolerat. Den körs även utanför applikationen också, så det du
skriver i ditt projekt eller det som renderas genom npm run dev till exempel, renderas inte i Storybook och vice versa. 
Man kör npm run storybook istället.
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
		margin-top: 100px;
	}
	img:nth-child(2) {
		place-self: end center;
		margin-bottom: 100px;
	}
</style>
