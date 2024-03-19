            <script lang="ts">
     
                function parallax(event: MouseEvent, element: HTMLElement) {
                  const { width, height, top, left } = element.getBoundingClientRect();
                  const x = event.clientX - (left + width / 2);
                  const y = event.clientY - (top + height / 2);           
                  const intensity = 15;
              
                  element.style.transform = `translate(${x / intensity}px, ${y / intensity}px)`;
                }
              
                function resetParallax(event: MouseEvent, element: HTMLElement) {
                  element.style.transform = '';
                }
              </script>
              
  

<section class="pt-10 lg:pb-48 overflow-hidden relative">
    <img data-rellax-speed="-8" src="bg.png" alt="bg" class="rellax absolute -z-30 w-[80%] top-0   right-0" />
    <div   class=" bg-gradient-to-b from-[#ff9060] from-40% via-[#ff9060] via-0% to-[#ffcd86] absolute -z-20 w-[100%] h-[100%] top-0  right-0 opacity-90" ></div>
	<div class="container mx-auto ">
		<div class=" rounded-3xl">
              
              <div class="sm:grid grid-cols-6">
                  <div class="sm:block hidden col-span-2 relative parallax-container">
                      <img data-rellax-speed="5" src="zara.png" class="w-full parallax-image rellax" alt="zara"
                           on:mousemove={(event) => parallax(event, event.currentTarget)}
                           on:mouseleave={(event) => resetParallax(event, event.currentTarget)} />
                      <img src="zarahex.png" alt="zara" class="absolute top-[15%] -z-10 left-0 " />
                      <img src="za.png" alt="zara" class="absolute w-[30%] top-[10%] z-20 left-[27%] heartbeat-icon heartbeat-icon-1" />
                  </div>
                  <div class="col-span-2 relative parallax-container">
                      <img data-rellax-speed="-16" src="kamau.png" class="w-full parallax-image rellax sm:block hidden" alt="kama"
                           on:mousemove={(event) => parallax(event, event.currentTarget)}
                           on:mouseleave={(event) => resetParallax(event, event.currentTarget)} />
                      <img src="mobile.png" class="w-full sm:hidden block" alt="kama" />
                      <img data-rellax-speed="-12" src="kamauhex.png" alt="kama" class="absolute top-[3%] -z-10 left-0 sm:block hidden rellax" />
                      <img src="ka.png" alt="kama" class="absolute w-[30%] -top-[7%] z-20 left-[34%] sm:block hidden heartbeat-icon heartbeat-icon-2" />
                  </div>
                  <div class="sm:block hidden col-span-2 relative parallax-container">
                      <img data-rellax-speed="5" src="yosefu.png" class="w-full rellax parallax-image" alt="yosef"
                           on:mousemove={(event) => parallax(event, event.currentTarget)}
                           on:mouseleave={(event) => resetParallax(event, event.currentTarget)} />
                      <img  src="yosefhex.png" alt="yosef" class="absolute top-[15%] -z-10 left-0" />
                      <img  src="yo.png" alt="yosef" class=" absolute w-[30%] top-[10%] z-20 right-[27%] heartbeat-icon heartbeat-icon-3" />
                  </div>
              </div>

            </div>
        </div>


        
        </section>