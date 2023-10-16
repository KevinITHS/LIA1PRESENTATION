<script lang="ts">
	import Image from "./formactions.jpg"
</script>

<div class="image">
	<img src={Image} alt="formactions" width="800px" />
</div>

<!-- SIX (STOP TIMER)
Efter att vi hade gjort high fidelity versionen av hot potato spelet så skulle vi använda ett koncept i Svelte som heter
form actions. Form actions går ut på att man gör en variant av sidan där alla funktioner ska funka även när man har
javascript disabled. Detta var relevant eftersom att det finns en chans att sidan inte laddar för 1% av alla användare.
Och då tänker man kanske "vem bryr sig om 1% av användare?" men som jag förstog det så är det slumpvist 1% av alla användare
varje gång, så en gång kan det vara jag och nästa gång kan det vara du.
-->

<style>
	div {
		display: flex;
		place-self: center;
	}
</style>
