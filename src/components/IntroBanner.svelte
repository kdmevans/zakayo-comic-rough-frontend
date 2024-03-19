
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
  



<section class="lg:pt-20 pt-2 overflow-hidden">
	<div class="container px-3 mx-auto lg:px-4">
		<div class=" lg:px-8 rounded-3xl">
			<div class="lg:max-w-8xl w-full mx-auto">
				<div class="lg:flex justify-center">
					<div data-aos="fade-right" data-aos-delay="100">
                        <div class="lg:mx-0 mx-auto w-[200px]" id="impact-container">
                            <img id="hammer" class="lg:mx-0 mx-auto w-[60%] lg:w-[80%]" src="hammer.png" alt="Hammer">
                        </div>
                    
                    </div>
					<div class="lg:text-7xl md:text-5xl sm:text-4xl text-2xl text-center">
						<h1 data-aos="fade-left" data-aos-delay="50"
							class="poppins my-1 whitespace-nowrap text-zinc-800 text-opacity-100 leading-none font-semibold"
						>
							Do you get headache
						</h1>
						<h1 data-aos="fade-left" data-aos-delay="100"
							class="poppins my-6 whitespace-nowrap text-zinc-800 text-opacity-100 leading-none font-semibold"
						>
							When Filing Returns
						</h1>
						<h1 data-aos="fade-left" data-aos-delay="150"
							class="poppins text-center my-1 whitespace-nowrap text-red-500 text-opacity-100 leading-none font-semibold"
						>
							in Kenya?
						</h1>
					</div>
				</div>
                <p data-aos="zoom-in" data-aos-delay="200"
                class="py-10 text-center md:text-lg md:w-[70%] w-full mx-auto  serif-4  tracking-widest"
                >Well, welcome to Zakayo, your go-to destination for tax education with a twist! Get ready
                to bid farewell to tax return headaches as our whimsical articles cover everything from
                   Individual Taxes, Business Taxes, to Corporate Taxes, making tax filing a breeze!</p
            >
</div>
</div>
</div>

<div class="categories-card relative mx-2 p-4 xl:p-20 lg:p-10  xl:mx-20 lg:mx-10">
	<img data-rellax-speed="-3" src="bg.png" alt="bg" class="rellax absolute -z-30 w-[90%] top-0   right-0" />
    <div   class=" bg-gradient-to-b from-[#ff9060] from-40% via-[#ff9060] via-0% to-[#ffcd86] absolute -z-20 w-[100%] h-[100%] top-0  right-0 opacity-90" ></div>
	

	<div class="md:flex  ">
		<div class=" md:w-2/6 xl:w-1/5 w-full mx-auto">
			<div class="card ">
				<img class="parallax-image"  on:mousemove={(event) => parallax(event, event.currentTarget)}
				on:mouseleave={(event) => resetParallax(event, event.currentTarget)} src="individual.png" alt="Individual Taxes">
				
				<div class="label">Individual Taxes</div>
	
			</div>
	
			<div class="card mt-12 md:mt-40">
				<img class="parallax-image"  on:mousemove={(event) => parallax(event, event.currentTarget)}
				on:mouseleave={(event) => resetParallax(event, event.currentTarget)} src="corporate.png" alt="Individual Taxes">
				
				<div class="label">Corporate Taxes</div>
	
			</div>
		
	
	
	
	</div>
	
	
	<div class="md:block hidden w-full relative md:w-2/6 xl:w-2/5  mx-auto">
		<img  src="zara2.png" class="xl:w-[80%] w-full mx-auto parallax-image " alt="kama"
                           on:mousemove={(event) => parallax(event, event.currentTarget)}
                           on:mouseleave={(event) => resetParallax(event, event.currentTarget)} />

						   <img  src="rotate.png" alt="kama" class="absolute top-[30%] -z-10 left-0 sm:block hidden  spinning" />
	</div>
	<div class=" md:w-2/6 xl:w-1/5 w-full mx-auto ">
		<div class="card md:mt-40 mt-12">
			<img class="parallax-image"  on:mousemove={(event) => parallax(event, event.currentTarget)}
			on:mouseleave={(event) => resetParallax(event, event.currentTarget)} src="omondi.png" alt="Individual Taxes">
			
			<div class="label">Business Taxes</div>
	
		</div>
	</div> 
	
			
		</div>
	
	</div>

</section>
