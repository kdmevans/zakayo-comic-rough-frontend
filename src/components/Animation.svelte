<script lang="ts">

    import { onMount } from 'svelte';
      import Rellax from 'rellax';

      import AOS from 'aos';
    import 'aos/dist/aos.css'; 
    
      onMount(() => {
        new Rellax('.rellax', {
          speed: -2,
          center: false,
        });

        AOS.init({
      
      duration: 1200, 
    });
    
      });
        
      </script>