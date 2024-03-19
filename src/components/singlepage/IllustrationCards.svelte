<script lang="ts">

	import type { Illustration } from '$lib/types/Illustration.interface';
	export let illustration: Illustration;

</script>


<div class="cards" id={illustration.cardType}>

<img src={illustration.bgImage} class="w-full " alt="" />
</div>