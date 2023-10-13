<script lang="ts">
	import Image from "./sveltereligion.jpg"
</script>

<div class="grid-stack">
	<img src={Image} alt="svelte-religion" width="250px" />
	<img src={Image} alt="svelte-religion" width="300px" />
	<img src={Image} alt="svelte-religion" width="250px" />
</div>

<style>
	div {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		max-width: 100vw;
		max-height: 100vw;
	}

	img:nth-child(1) {
		place-self: center start;
	}
	img:nth-child(2) {
		place-self: center center;
	}
	img:nth-child(3) {
		place-self: center end;
	}
</style>
