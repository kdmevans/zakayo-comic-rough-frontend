<script lang="ts">

	import type { Illustration } from '$lib/types/Illustration.interface';
	export let illustration: Illustration;
    
    import { 
        Lightbox,
    } from 'svelte-lightbox'
    
   
</script>


<div class="w-full col-span-3 my-10 md:px-4">
    <Lightbox description="illustration">
        <img src={illustration.bgImage} class="w-full transition ease-in-out duration-150 hover:scale-105 " alt="" />
    </Lightbox>

   

</div>