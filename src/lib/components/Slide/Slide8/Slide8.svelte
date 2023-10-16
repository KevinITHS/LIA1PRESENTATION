<script lang="ts">
	import Image from "./whysvelte.jpg"
</script>

<div class="image">
	<img src={Image} alt="whysvelte" width="600px" />
</div>

<!-- EIGHT
SvelteKit är känd för sin snabbhet. Ramverket optimerar koden så att den tar
mindre utrymme och körs snabbare, som ger en bättre användarupplevelse. Detta är särskilt bra för applikationer
som kräver mycket client-side scripting och rendering. Den är också lättare att lära sig jämfört med React, om man kommer in
som nybörjare och inte kan någon webbutveckling från innan. 
-->

<style>
	div {
		display: flex;
		place-self: center;
	}
</style>
