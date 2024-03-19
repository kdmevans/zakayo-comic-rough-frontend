<script lang="ts">
	import type { Blog } from '$lib/types/Blog.interface';
	export let blog: Blog;

</script>

<div class="w-full col-span-3 my-28 md:my-10 md:px-4">
    <a href="/blogs/1">
<div class="mainCard group">
	<div class="top-section w-full xl:h-[50vh]" >
	 
	  <div class="absolute hidden lg:block rounded-2xl bg-clip-blogs -z-10 w-full h-[35vh] xl:h-[50vh] top-0 left-0 bg-cover bg-center" style="background-image: linear-gradient(rgba(255, 144, 96, 0.5),rgba(255,205,134,0.8)), url({blog.bgImage});"></div>
	 
	  <div class="xl:grid grid-cols-6  gap-6">

		<div class="w-full translate-y-[6%] rounded-2xl relative xl:h-[47vh] col-span-3 bg-cover bg-center" style="background-image:url({blog.bgImage});">
		
			<img class="xl:absolute mx-auto lg:mx-0 w-[80%] md:w-[70%] lg:w-[60%] xl:w-[100%] -translate-y-[28%] " src={blog.avatar} alt="" />


			</div>

			<div class="w-full relative col-span-3 ">
				<div class=" xl:relative absolute left-6 xl:left-0 bottom-10 xl:bottom-0 xl:pt-24 duration-500 group-hover:-skew-x-0 skew-x-6 group-hover:translate-x-2">
					<div class="group-hover:duration-400 relative rounded-2xl w-full  bg-zinc-800 text-gray-50 flex flex-col justify-center items-center gap-1 before:-skew-x-12  before:rounded-2xl  before:absolute before:content['']  before:bg-neutral-700 xl:before:right-[6%] before:right-[3%] before:top-0 before:w-full before:h-[90%] before:-z-10">

						<div class="-rotate-45 cursor-pointer">
							<svg
							  clip-rule="evenodd"
							  fill-rule="evenodd"
							  stroke-linejoin="round"
							  stroke-miterlimit="2"
							  viewBox="0 0 24 24"
							  xmlns="http://www.w3.org/2000/svg"
							  class="text-gray-600 font-semibold text-lg sm:text-xl transition-all duration-300 group-hover:transition-all group-hover:duration-300 group-hover:text-gray-200 fill-[#ffcd86] group-hover:bg-[#f4c480] group-hover:fill-white group-hover:rotate-45 p-px rounded-full w-10 group-hover:rounded-full group-hover:animate-pulse"
							>
							  <path
								d="m12.012 1.995c-5.518 0-9.998 4.48-9.998 9.998s4.48 9.998 9.998 9.998 9.997-4.48 9.997-9.998-4.479-9.998-9.997-9.998zm0 1.5c4.69 0 8.497 3.808 8.497 8.498s-3.807 8.498-8.497 8.498-8.498-3.808-8.498-8.498 3.808-8.498 8.498-8.498zm1.528 4.715s1.502 1.505 3.255 3.259c.146.147.219.339.219.531s-.073.383-.219.53c-1.753 1.754-3.254 3.258-3.254 3.258-.145.145-.336.217-.527.217-.191-.001-.383-.074-.53-.221-.293-.293-.295-.766-.004-1.057l1.978-1.977h-6.694c-.414 0-.75-.336-.75-.75s.336-.75.75-.75h6.694l-1.979-1.979c-.289-.289-.286-.762.006-1.054.147-.147.339-.221.531-.222.19 0 .38.071.524.215z"
								fill-rule="nonzero"
							  ></path>
							</svg>
						  </div>
						




						<div class="title text-center" >
							<h1 class="text-white golden-text text-4xl lg:text-6xl">{blog.title}</h1>
					
							<h1 class="text-white my-3 text-lg xl:text-2xl"><span class="text-gray-200 poppins">by ~ </span> {blog.author}</h1>
							
							
							</div>
		
					</div>
				  </div>
	

				 

				</div>
	

		</div>



	</div>
	
  </div>

</a>
</div>

    

