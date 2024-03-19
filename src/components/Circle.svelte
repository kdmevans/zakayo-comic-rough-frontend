

<script lang="ts">

import { onMount } from 'svelte';

    onMount(() => {
        const circle: HTMLElement | null = document.getElementById('floating-circle');

        function moveCircle(e: MouseEvent): void {
            if (circle) {
                const mouseX: number = e.clientX;
                const mouseY: number = e.clientY;
                circle.style.transform = `translate(${mouseX - 25}px, ${mouseY - 25}px)`;
            }
        }


        function onMouseDown(): void {
            if (circle) {
        
                circle.style.transform += ' scale(0.4)';
             
            }
        }

        function onMouseUp(): void {
            if (circle) {
                
                const originalTransform = circle.style.transform.replace(' scale(0.4)', '');
                circle.style.transform = originalTransform;
               
            }
        }

        window.addEventListener('mousemove', moveCircle);
        window.addEventListener('mousedown', onMouseDown);
        window.addEventListener('mouseup', onMouseUp);

        return () => {
            window.removeEventListener('mousemove', moveCircle);
            window.removeEventListener('mousedown', onMouseDown);
            window.removeEventListener('mouseup', onMouseUp);
        };
    });

  </script>



<div id="floating-circle"></div>


  







  
 
  
